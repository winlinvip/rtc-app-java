# rtc-app-java

Java AppServer for RTC.

You could also write AppServer by following languages:

* Golang: https://github.com/winlinvip/rtc-app-golang
* Java: https://github.com/winlinvip/rtc-app-java
* Python: https://github.com/winlinvip/rtc-app-python
* C#: https://github.com/winlinvip/rtc-app-csharp
* Nodejs: https://github.com/winlinvip/rtc-app-nodejs
* PHP: https://github.com/winlinvip/rtc-app-php

For RTC deverloper:

* RTC [workflow](https://help.aliyun.com/document_detail/74889.html).
* RTC [token generation](https://help.aliyun.com/document_detail/74890.html).

Use OpenAPI to create channel:

* Golang: https://help.aliyun.com/document_detail/74890.html#channel-golang
* Java: https://help.aliyun.com/document_detail/74890.html#channel-java
* Python: https://help.aliyun.com/document_detail/74890.html#channel-python
* C#: https://help.aliyun.com/document_detail/74890.html#channel-csharp
* Nodejs: https://help.aliyun.com/document_detail/74890.html#channel-nodejs
* PHP: https://help.aliyun.com/document_detail/74890.html#channel-php

Token generation algorithm:

* Golang: https://help.aliyun.com/document_detail/74890.html#token-golang
* Java: https://help.aliyun.com/document_detail/74890.html#token-java
* Python: https://help.aliyun.com/document_detail/74890.html#token-python
* C#: https://help.aliyun.com/document_detail/74890.html#token-csharp
* Nodejs: https://help.aliyun.com/document_detail/74890.html#token-nodejs
* PHP: https://help.aliyun.com/document_detail/74890.html#token-php

## Usage

1. Generate AK from [here](https://usercenter.console.aliyun.com/#/manage/ak):

```
AccessKeyID: OGAEkdiL62AkwSgs
AccessKeySecret: 4JaIs4SG4dLwPsQSwGAHzeOQKxO6iw
```

2. Create APP from [here](https://rtc.console.aliyun.com/#/manage):

```
AppID: iwo5l81k
```

3. Build project with maven, for example, [JetBrains IDEA](https://www.jetbrains.com/idea/download/#section=mac).

4. Run project with args(replace access key and appid with yours):

```
--listen=8080 --access-key-id=OGAEkdiL62AkwSgs
	--access-key-secret=4JaIs4SG4dLwPsQSwGAHzeOQKxO6iw --appid=iwo5l81k
	--gslb=https://rgslb.rtc.aliyuncs.com
```

5. Verify  your AppServer by [here](http://ossrs.net/talks/ng_index.html#/rtc-check?schema=http&host=127.0.0.1&port=8080&path=/app/v1/login&room=1237&user=jzufp&password=12345678) or [verify token](http://ossrs.net/talks/ng_index.html#/token-check).

![AppServer Success](https://github.com/winlinvip/rtc-app-golang/raw/master/images/app-ok.png)

![AppServer Failed](https://github.com/winlinvip/rtc-app-golang/raw/master/images/app-failed.png)

![AppServer Error Recovered](https://github.com/winlinvip/rtc-app-golang/raw/master/images/app-recovered.png)

> Remark: You can setup client native SDK by `http://30.2.228.19:8080/app/v1`.

> Remark: Please use your AppServer IP instead by `ifconfig eth0`.

## History

* [4cbf084](https://github.com/winlinvip/rtc-app-java/commit/4cbf084731bf3ee7233f3e0beb678ba47e32d5a2), [ef64f0b](https://github.com/winlinvip/rtc-app-java/commit/ef64f0b772e337b46e2a95d74896430f4a45f159), Update SessionID generation algorithm.
* [b68830b](https://github.com/winlinvip/rtc-app-java/commit/b68830b794613bd29ac403596df2745ff4af3b66), Use HTTP, x3 times faster than HTTPS.
* [ef62e80](https://github.com/winlinvip/rtc-app-java/commit/ef62e80531a4e65eb2f69fc05822ca22e244a1a1), Log the request id and cost in ms.
* [8b088f1](https://github.com/winlinvip/rtc-app-java/commit/8b088f1f89bbc1666723656c62a5285d20880077), [e726b19](https://github.com/winlinvip/rtc-app-java/commit/e726b19f53fb85308e0166676779efb32e655db5), Set endpoint to get correct exception.
* [4c85f2e](https://github.com/winlinvip/rtc-app-java/commit/4c85f2e025c448f1cadd524ee67ddfbf984722b3), Set auto retry and timeout.
* [cb3eb09](https://github.com/winlinvip/rtc-app-java/commit/cb3eb0924d6b97eec13b270bda236b622f88e1a5), Support recover for some OpenAPI error.
* Support create channel and sign user token.
