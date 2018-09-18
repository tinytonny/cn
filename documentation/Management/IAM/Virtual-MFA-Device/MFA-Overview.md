# 什么是MFA？
MFA (Multi-Factor Authentication) 是一种简单有效的最佳安全实践，它能够在用户名和密码之外再额外增加一层安全保护，并且在京东云进行敏感操作时，进行身份验证防止误删。

虚拟 MFA 设备是一种基于软件，产生动态验证码的应用程序，它遵循基于时间的一次性密码 (TOTP) 标准 (RFC 6238)，可以将虚拟 MFA 设备安装在不同的移动设备上，如智能手机。启用 MFA 后，用户登录京东云时，系统将要求输入用户名和密码，然后要求输入来自其 MFA 设备的6位动态验证码，即使他人盗取您的密码，也无法登陆您的账号，双因素的安全认证将最大限度地保障您的账户安全。

# 京东云助手
京东云助手（微信小程序）是京东云为方便用户提供统一的虚拟MFA设备，我们建议您通过此应用程序绑定您的用户信息，生成动态验证码。

<div align=center><img width = "250" height = "250" src=https://github.com/jdcloudcom/cn/blob/edit/image/IAM/Virtual%20MFA%20device/%E4%BA%8C%E7%BB%B4%E7%A0%81.jpg/></div>
