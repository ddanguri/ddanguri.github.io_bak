---
layout: post
title:  "npm,git,bower proxy setting"
date:   2016-04-06 01:07:49
categories:
- setting
comments: true
---

보통 프록시 정보를 확인하려면

1. 인터넷 정보 > 연결 tab > LAN 설정 > 자동 구성 스크립트 사용 부분의 주소값의 정보를 보거나,

2. command Line에서 ``` netsh winhttp show proxy ```

3. 아예 [.exe 실행파일](https://github.com/xmedeko/WinProxyViewer/releases)로 만든 사람도 있다.


### npm

```command
$ npm config set proxy [proxyAddress]:[port]
$ npm config set https-proxy [proxyAddress]:[port]
$ npm config set strict-ssl false
```

### git

```command
$ git config --global http.proxy http://[proxyAddress]:[port]
$ git config --global https.proxy http://[proxyAddress]:[port]
```

### bower
bower는 .bowerrc 파일에 정보를 입력한다. 파일이 없으면 사용자 폴더에 생성한다.

```json
{
    "directory": "bower_components",
	"proxy":"http://[proxyAddress]:[port]",
	"https-proxy":"http://[proxyAddress]:[port]",
    "strict-ssl": false
}
```

### Windows Command prompt (cmd)

```Command
> set http_proxy=[proxyAddress]:[port]
> set https_proxy=[proxyAddress]:[port]
```

### Bash shell

```Command
export http_proxy=[proxyAddress]:[port]
export https_proxy=[proxyAddress]:[port]
```
