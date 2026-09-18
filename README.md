# shengpay-debug

盛付通支付接口在线调试台（单文件静态页面，托管于 GitHub Pages）。

## 功能

- 4 个接口在线联调：
  - `pay.unifiedorderOffline`（下单）
  - `pay.queryOrder`（支付订单查询）
  - `refund.orderRefund`（退款）
  - `refund.queryRefundOrder`（退款订单查询）
- 签名算法：SHA1WithRSA（PKCS#8 Base64 私钥，浏览器内 Web Crypto 完成，私钥不离开本地）
- 调用成功后一键生成多语言示例代码（Node.js / Java / C# / PHP）
- 内置 shengpay-codegen 技能包下载（zip 以 base64 内嵌，离线可用）

## 本地使用

直接双击 `index.html` 用浏览器打开即可（Web Crypto 签名需要 `https://` 或 `localhost` 环境；`file://` 下调用功能受限，纯静态托管访问无此问题）。

## 更新页面

替换仓库根目录的 `index.html` 后提交推送，GitHub Pages 约 1 分钟内自动生效。
