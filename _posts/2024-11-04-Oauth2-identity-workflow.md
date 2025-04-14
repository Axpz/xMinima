---  
layout: home  
title: "OAuth 2.0 授权码模式"  
date: 2024-11-04 14:43:43 +0800  
lastupdated: 2024-11-04 15:30:00 +0800  
categories: k8s  
tags: [oauth,ai]
---

![auth2](/assets/images/auth-overall.png)


# 注册客户端(第三方应用)信息
  
在使用 OAuth 2.0 授权码模式之前，客户端(第三方应用)（通常是你的应用）需要在授权服务器上进行注册。注册后，你会获得以下信息：

- **client_id**：客户端(第三方应用)的唯一标识符，由授权服务器分配。
- **client_secret**：客户端(第三方应用)的密钥，用于验证客户端(第三方应用)的身份（但仅在安全环境下使用，比如服务端，不建议在前端公开）。

## 填写回调 URL（Redirect URI）
  
在注册过程中，你需要提供一个 **回调地址**，即授权完成后授权服务器会重定向用户的地址。

- **Redirect URI（回调地址）** 是授权服务器将授权码发送到客户端(第三方应用)的地方，它必须与你注册时填写的地址完全匹配。
- 回调地址通常是一个 HTTPS URL，例如：https://your-app.com/callback

- 如果你有多个环境（如开发环境、生产环境），需要为每个环境分别注册对应的回调 URL。

## 用途

- 授权服务器会在用户授权后，通过这个回调地址将 **授权码（Authorization Code）** 发送回客户端(第三方应用)。
- 之后，客户端(第三方应用)再通过授权码和客户端(第三方应用)密钥，向授权服务器请求 **访问令牌（Access Token）**。



# 流程细化解释

![auth2](/assets/images/auth-exchange.png)

## 客户端(第三方应用)生成授权请求并包含 CSRF 随机字符串

- 客户端(第三方应用)（第三方应用）在发起授权请求时，会生成一个随机字符串（`state`）作为防止 CSRF 攻击的标志。
- 客户端(第三方应用)通过 **302 重定向** 请求用户访问授权服务器（`auth server`），并在 URL 中携带以下重要参数：

```http  
GET /authorize?      response_type=code&client_id=CLIENT_ID&redirect_uri=https://your-app.com/callback&scope=SCOPE&state=RANDOM_STRING HTTP/1.1  
Host: auth-server.com
```  
参数说明：
- **response_type=code**：请求授权码。
- **client_id**：客户端(第三方应用)标识。
- **redirect_uri**：用户授权完成后，授权服务器会将用户重定向到此地址。
- **scope**：客户端(第三方应用)请求的权限范围。
- **state**：由客户端(第三方应用)生成的随机字符串，用于防止 CSRF 攻击。

## 授权服务器显示登录/授权页面

- 用户被 **302 重定向** 到授权服务器，授权服务器会弹出认证页面，让用户登录并选择是否授权第三方应用。
- 如果用户未登录，会先引导用户登录。如果用户已经登录，则直接显示授权页面。

## 用户认证成功后，授权服务器生成授权码并重定向

- 用户在授权页面上点击“允许”后，授权服务器会生成一个 **授权码（authorization code）**。
- 授权服务器通过 **302 重定向** 将用户带回客户端(第三方应用)的回调地址（`redirect_uri`），并在 URL 中附加授权码和原始的 `state`：

```http  
HTTP/1.1 302 Found  
Location: https://your-app.com/callback?      code=AUTH_CODE&state=RANDOM_STRING
```
 参数说明：
- **code**：授权码。
- **state**：原始客户端(第三方应用)发送的 `state` 值，用于验证请求完整性。

## 客户端(第三方应用)验证 state

- 客户端(第三方应用)在收到授权服务器的回调时，必须验证返回的 `state` 是否与初始发送的值一致。
- 如果 `state` 不匹配，则可能存在 CSRF 攻击或请求被篡改，客户端(第三方应用)应拒绝处理该回调。

## 客户端(第三方应用)交换授权码获取访问令牌

- 如果 `state` 验证通过，客户端(第三方应用)使用授权码（`code`）向授权服务器发起 **POST 请求**，交换访问令牌（`access token`）：

```bash  
POST /token HTTP/1.1  
Content-Type: application/x-www-form-urlencoded
  
grant_type=authorization_code&code=AUTH_CODE&redirect_uri=https://your-app.com/callback&client_id=CLIENT_ID&client_secret=CLIENT_SECRET
```

# 核心点总结

- 客户端(第三方应用)生成授权 URL，并携带 `state` 和其他参数，使用 **302 重定向** 将用户引导到授权服务器。
- 授权服务器处理用户登录并授权后，通过 **302 重定向** 将用户带回客户端(第三方应用)的 `redirect_uri`，同时携带 `auth_code` 和原始的 `state`。
- 客户端(第三方应用)收到回调后验证 `state`，确保请求未被篡改。
- 验证通过后，客户端(第三方应用)使用授权码换取访问令牌。
