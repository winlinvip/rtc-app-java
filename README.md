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

6. Verify AppServer by [here](http://localhost:8080/app/v1/login?room=5678&user=nvivy&passwd=12345678).

> Remark: You can setup client native SDK by `http://30.2.228.19:8080/app/v1`.

> Remark: Please use your AppServer IP instead by `ifconfig eth0`.

## History

* [4c85f2e](https://github.com/winlinvip/rtc-app-java/commit/4c85f2e025c448f1cadd524ee67ddfbf984722b3), Set auto retry and timeout.
* [cb3eb09](https://github.com/winlinvip/rtc-app-java/commit/cb3eb0924d6b97eec13b270bda236b622f88e1a5), Support recover for some OpenAPI error.
* Support create channel and sign user token.
