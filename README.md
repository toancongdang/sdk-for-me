<body bgcolor="red">
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Thanks again! Now go create something AMAZING! :D
-->

<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
![The San Juan Mountains are beautiful!](/assets/logo_momo.png "San Juan Mountains")


<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://developers.momo.vn/#/docs/aiov2/">
    <img src="assets/logo_momo.png" alt="Logo" width="80" height="80">
  </a>

<h3 align="center">SDK MOMO FOR ME</h3>

  <p align="center">
    Hướng dẫn tốt nhất dành cho bạn
    <br />
    <a href="https://developers.momo.vn/#/docs/aiov2/"><strong>Tài liệu gốc »</strong></a>
    <br />
    <br />
    <a href="https://test-payment.momo.vn/demo/#/">View Demo</a>
    ·
    <a href="https://developers.momo.vn/#/docs/feedback">Report Bug</a>
    ·
    <a href="https://business.momo.vn/login">Request Feature</a>
  </p>




<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Mục lục</summary>
  <ol>
    <li>
      <a href="#i-gi%E1%BB%9Bi-thi%E1%BB%87u">Giới thiệu</a>
      <ul>
        <li><a href="#built-with">Mục tiêu</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT -->
# I. Giới thiệu
Nhầm hỗ trợ các đối tác tích hợp các giải pháp thanh toán của MoMo. Tài liệu này sẽ hướng dẫn các bạn cách tích hợp tối ưu nhất.

* Giải pháp toàn vẹn - Cổng thanh toán [ALL IN ONE](https://developers.momo.vn/#/docs/aiov2/) version 2 (AIOv2).
  <br>
  AIOv2 là giải pháp thanh toán của MoMo áp dụng trên nhiều nền tảng khác nhau chỉ trong một API duy nhất.

### Mục tiêu

* Nhầm giúp đối tác lựa chọn giải pháp thanh toán phù hợp
* Tích hợp nhanh chóng, chính xác, hiệu quả
* Hạn chế rủi ro trong quá trình tích hợp


<!-- GETTING STARTED -->
# II. Lựa chọn giải pháp

[AIOv2](https://developers.momo.vn/#/docs/aiov2/) là giải pháp thanh toán của MoMo áp dụng trên nhiều nền tảng khác nhau chỉ trong một API duy nhất.



[comment]: <> (```bigquery)

[comment]: <> (Trên môi trường thật &#40;production&#41;: )

[comment]: <> (Bạn phải yêu cầu Bộ phận kinh doanh của MoMo, để được cung cấp quyền truy cập:)

[comment]: <> (qrCodeUrl, deeplink, deeplinkWebInApp, deeplinkMiniApp, Refund)

[comment]: <> (```)

## Sơ đồ xử lý
Sơ đồ thanh toán đơn hàng trên website desktop/mobile
<p align="left">
  <a href="https://developers.momo.vn/#/docs/aiov2/?id=s%c6%a1-%c4%91%e1%bb%93-x%e1%bb%ad-l%c3%bd">
    <img src="https://developers.momo.vn/images/payment-flow.jpg" alt="flow" width="100%">
  </a>
</p>

Thanh toán trên Smart Tivi
<p align="left">
  <a href="https://developers.momo.vn/#/docs/aiov2/?id=s%c6%a1-%c4%91%e1%bb%93-x%e1%bb%ad-l%c3%bd">
    <img src="https://s3.amazonaws.com/heroku-jinzdev/payment-smart-flow.jpg" alt="flow" width="100%">
  </a>
</p>

## Mô hình thanh toán
Tham khảo hướng dẫn sau để áp dụng MoMo vào trang mua hàng của bạn

* Bước 1: Khách hàng kiểm tra đơn hàng và chọn MoMo là phương thức thanh toán
* Bước 2: Server của bạn tạo session thanh toán và gửi yêu cầu thanh toán qua MoMo
* Bước 3: Chuyển trang mua hàng sang trang thanh toán của MoMo.
* Bước 4: Khách hàng sử dụng ứng dụng MoMo để quét mã QR hoặc đăng nhập app MoMo để thanh toán
* Bước 5: Sau khi thanh toán xong MoMo sẽ chuyển khách hàng về trang mua hàng
* Bước 6: Server của bạn xác thực giao dịch và cập nhật dịch vụ cho khách hàng

# III. Thông tin chung
* <b>Domain</b>

| Environment | Domain |
| --- | ----------- |
| Production | https://payment.momo.vn |
| Test | https://test-payment.momo.vn |

* <b>IP Address</b>

| Environment | Incoming    | Outcoming  |
| ---         | ----------- |----------- |
| Production  | 210.245.113.71 |118.69.210.244|
| Test        | 118.69.212.158 |118.69.210.244|

* <b>HTTP Request</b>

| Key | Value |
| --- | ----------- |
| Content-Type | application/json; charset=UTF-8 |
| Method | POST |
| HTTP Status Code | 200 |

* <b>List API SDK MOMO</b>

| API Name | Path | Docs |
| --- | ----------- |--- |
| Create Transaction v2 | /v2/gateway/api/create | [[link]](https://developers.momo.vn/#/docs/aiov2/?id=l%e1%ba%a5y-ph%c6%b0%c6%a1ng-th%e1%bb%a9c-thanh-to%c3%a1n) |
| Query Transaction v2 | /v2/gateway/api/query | [[link]](https://developers.momo.vn/#/docs/aiov2/?id=ki%e1%bb%83m-tra-tr%e1%ba%a1ng-th%c3%a1i-giao-d%e1%bb%8bch) |
| Refund Transaction v2| /v2/gateway/api/refund | [[link]](https://developers.momo.vn/#/docs/aiov2/?id=ho%c3%a0n-ti%e1%bb%81n-giao-d%e1%bb%8bch) |

* <b>List API listen reesult-transaction from MoMo (Partner must-have)</b>

| API Name | Url | Docs |
| --- | ----------- |--- |
| redirectUrl | http(s)://domain.partner.vn/redirect/ | [[link]](https://developers.momo.vn/#/docs/aiov2/?id=giao-di%e1%bb%87n-redirect) |
| ipnUrl | http(s)://domain.partner.vn/ipn/ | [[link]](https://developers.momo.vn/#/docs/aiov2/?id=ipn-instant-payment-notification) |

Tool Debug [API redirectUrl & ipnUrl](https://developers.momo.vn/#/docs/aio/?id=debug) hỗ trợ trong quá trình dev

# IV. Create Account
> Warning! Vui lòng không chia sẻ KEY Production cho bất cứ ai, chúng tôi
sẽ không xử lý những trường hợp KEY Production bị phát tán ra ngoài.

Đăng ký [Create Account Test](https://test-business.momo.vn/signup)
<br>
Đăng ký [Create Account Production](https://business.momo.vn/signup)
<details><summary>CLICK ME !!! Account Test tạo sẵn</summary>
<p>

| Key Test | Value |
| --- | ----------- |
| partnerCode | MOMONPMB20210629|
| partnerName | Tên doanh nghiệp SDK4ME|
| accessKey | Q2XhhSdgpKUlQ4Ky|
| secretKey | k6B53GQKSjktZGJBK2MyrDa7w9S6RyCf|
| userwame | sdk_4_me |
| password | sdk_4_me! |
</p>
</details>

# V. Call Api
## 1. Create Transaction (Lấy phương thức thanh toán [link](https://developers.momo.vn/#/docs/aiov2/?id=l%e1%ba%a5y-ph%c6%b0%c6%a1ng-th%e1%bb%a9c-thanh-to%c3%a1n))
>POST <span style="color:orange">/v2/gateway/api/create</span>

* HTTP Request

|Attribute	|Type	|Required	|Description|
|---|---|---|---|
|partnerCode	|String|	√|	<a href="#iv-create-account">Thông tin tích hợp</a> |
|partnerName	|String|	|	Tên đối tác|
|storeId	|String|		|Thông tin cửa hàng|
|requestId	|String|	√|	Định danh mỗi yêu cầu|
|amount	|Long|	√|	Số tiền cần thanh toán. tối thiểu 1.000 VND tối đa 20.000.000 VND. Tiền tệ: VND|
|orderId	|String|	√|	Mã đơn hàng thanh toán của đối tác (duy nhất không trùng lập)|
|orderInfo	|String|	√|	Thông tin đơn hàng|
|redirectUrl	|String|	√|	Một URL của đối tác. URL này được sử dụng để chuyển trang (redirect) từ MoMo về trang mua hàng của đối tác sau khi khách hàng thanh toán. Hỗ trợ: AppLink và WebLink|
|ipnUrl	|String|	√|	API của đối tác. Được MoMo sử dụng để gửi kết quả thanh toán theo phương thức IPN (server-to-server)|
|requestType	|String|	√|	<span style="color:orange">captureWallet</span>|
|extraData	|String|	√|	Mặc định là trống "", Encode base64 theo định dạng Json: {"key":"value"}. VD với dữ liệu: {"username": "SDK4ME"} thì data của extraData là eyJ1c2VybmFtZSI6ICJTREs0TUUifQ==|
|lang	|String|	√|	Ngôn ngữ của message được trả về (vi hoặc en)|
|signature	|String|	√|	Chữ ký. Sử dụng thuật toán Hmac_SHA256 với các key-value được sắp xếp theo thứ tự A-Z |

>signature = HMAC_SHA256(accessKey=$accessKey&amount=$amount&extraData=$extraData&ipnUrl=$ipnUrl&orderId=$orderId&orderInfo=$orderInfo&partnerCode=$partnerCode&redirectUrl=$redirectUrl&requestId=$requestId&requestType=$requestType,secretKey)
<details><summary>SAMPLE</summary>
Request Body

```json
{
  "partnerCode": "MOMONPMB20210629",
  "partnerName": "Tên doanh nghiệp SDK4ME",
  "storeId": "MOMONPMB20210629_1",
  "requestId": "requestId_1624943052612",
  "amount": 1100,
  "orderId": "orderId_1624943052612",
  "orderInfo": "Demo tích hợp SDK MOMO",
  "redirectUrl": "http(s)://domain.partner.vn/redirect/",
  "ipnUrl": "http(s)://domain.partner.vn/ipn/",
  "requestType": "captureWallet",
  "extraData": "eyJ1c2VybmFtZSI6ICJtb21vIn0=",
  "lang": "vn",
  "signature": "3084afbc257bc556d60efbffab14b4358874572a30d9e3ed7676b9d96dd27c91"
}
```
Response Body
```json
{
  "partnerCode": "MOMONPMB20210629",
  "requestId": "requestId_1624943052612",
  "orderId": "orderId_1624943052612",
  "amount": 1100,
  "responseTime": 1624945082867,
  "message": "Thành công",
  "resultCode": 0,
  "payUrl": "https://test-payment.momo.vn/v2/gateway/pay?t=TU9NT05QTUIyMDIxMDYyOXwxNjI0OTQ1MDgyMTU3TS5PLk0uTw==",
  "deeplink": "momo://?action=payWithAppToken&amount=1100&cashInId=&cashInIdPay=&createdAt=1624945082867&deeplinkCallback=&description=DANG_CONG_TOAN_TEST&extra=&extraData=&extras=&gatewayMerchantCode=MOMONPMB20210629&gatewaySessionId=TU9NT05QTUIyMDIxMDYyOXwxNjI0OTQ1MDgyMTU3TS5PLk0uTw==&gatewayVersion=3.0&giftIds=&isScanQR=false&language=vi&merchantcode=MOMONPMB20210629&merchantname=T%C3%AAn+doanh+nghi%E1%BB%87p+SDK4ME&merchantnamelabel=Nh%C3%A0+cung+c%E1%BA%A5p&orderId=1624945082157M.O.M.O&orderLabel=M%C3%A3+%C4%91%C6%A1n+h%C3%A0ng&partnerCode=MOMONPMB20210629&partnerName=T%C3%AAn+doanh+nghi%E1%BB%87p+SDK4ME&prepaidIds=&requestId=1624945082157M.O.M.O&requestType=payment&serviceType=deeplink&signature=d0cd686b15471f7cb3eed3bf8ab52941ebcbbf6c8a932b1dfc13b77640516a1a&storeId=MOMONPMB20210629&storeName=T%C3%AAn+doanh+nghi%E1%BB%87p+SDK4ME&type=&urlSubmitToken=https%3A%2F%2Fmomo.vn",
  "qrCodeUrl": "https://test-payment.momo.vn/v2/gateway/app?isScanQr=true&t=TU9NT05QTUIyMDIxMDYyOXwxNjI0OTQ1MDgyMTU3TS5PLk0uTw==",
  "deeplinkMiniApp": "momo://?action=payWithAppToken&amount=1100&cashInId=&cashInIdPay=&createdAt=1624945082867&deeplinkCallback=&description=DANG_CONG_TOAN_TEST&extra=&extraData=&extras=&gatewayMerchantCode=MOMONPMB20210629&gatewaySessionId=TU9NT05QTUIyMDIxMDYyOXwxNjI0OTQ1MDgyMTU3TS5PLk0uTw==&gatewayVersion=3.0&giftIds=&isScanQR=false&language=vi&merchantcode=MOMONPMB20210629&merchantname=T%C3%AAn+doanh+nghi%E1%BB%87p+SDK4ME&merchantnamelabel=Nh%C3%A0+cung+c%E1%BA%A5p&orderId=1624945082157M.O.M.O&orderLabel=M%C3%A3+%C4%91%C6%A1n+h%C3%A0ng&partnerCode=MOMONPMB20210629&partnerName=T%C3%AAn+doanh+nghi%E1%BB%87p+SDK4ME&prepaidIds=&requestId=1624945082157M.O.M.O&requestType=payment&serviceType=miniapp&signature=d0cd686b15471f7cb3eed3bf8ab52941ebcbbf6c8a932b1dfc13b77640516a1a&storeId=MOMONPMB20210629&storeName=T%C3%AAn+doanh+nghi%E1%BB%87p+SDK4ME&type=&urlSubmitToken=https%3A%2F%2Fmomo.vn"
}
```
</details>







=======================================================================
This is an example of how to list things you need to use the software and how to install them.
=======================================================================
* npm
  ```sh
  npm install npm@latest -g
  ```

### Installation

1. Get a free API Key at [https://example.com](https://example.com)
2. Clone the repo
   ```sh
   git clone https://github.com/your_username_/Project-Name.git
   ```
3. Install NPM packages
   ```sh
   npm install
   ```
4. Enter your API in `config.js`
   ```JS
   const API_KEY = 'ENTER YOUR API';
   ```



<!-- USAGE EXAMPLES -->
## Usage

Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

_For more examples, please refer to the [Documentation](https://example.com)_



<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/othneildrew/Best-README-Template/issues) for a list of proposed features (and known issues).



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.



<!-- CONTACT -->
## Contact

Your Name - [@your_twitter](https://twitter.com/your_username) - email@example.com

Project Link: [https://github.com/your_username/repo_name](https://github.com/your_username/repo_name)



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [GitHub Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet)
* [Img Shields](https://shields.io)
* [Choose an Open Source License](https://choosealicense.com)
* [GitHub Pages](https://pages.github.com)
* [Animate.css](https://daneden.github.io/animate.css)
* [Loaders.css](https://connoratherton.com/loaders)
* [Slick Carousel](https://kenwheeler.github.io/slick)
* [Smooth Scroll](https://github.com/cferdinandi/smooth-scroll)
* [Sticky Kit](http://leafo.net/sticky-kit)
* [JVectorMap](http://jvectormap.com)
* [Font Awesome](https://fontawesome.com)





<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: images/screenshot.png


| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |


| Syntax | Description |
| --- | ----------- |
| Header | Title |
| Paragraph | Text |
</body>