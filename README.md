# Bright Data Web Unlocker Nodejs project
[![Bright Data Promo](https://github.com/bright-kr/LinkedIn-Scraper/raw/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner.png)](https://brightdata.co.kr/)

[StackBlitz editor ⚡️에서 편집](https://stackblitz.com/~/github.com/bright-kr/bright-data-web-unlocker-nodejs-project?file=index.js)

## Bright Data Web Unlocker API Example

이 프로젝트는 Bright Data의 [Unlocker API](https://brightdata.co.kr/products/web-unlocker)를 사용하여 Bright Data [Unlocker API](https://brightdata.co.kr/products/web-unlocker)를 통해 웹사이트에 액세스하는 방법을 보여줍니다.

## Overview

이 스크립트는 Bright Data의 Web Unlocker를 사용하여 이러한 장애물을 자동으로 우회함으로써 앤チボット 보호 또는 CAPTCHA가 있는 웹사이트에 액세스하는 데 도움을 줍니다.


### Using environment variables in StackBlitz

1. `.env` 파일을 선택합니다
2. 다음 변수를 추가합니다:
   - `BRIGHT_DATA_API_TOKEN`: Bright Data [API Token](https://docs.brightdata.com/general/account/api-token)
   - `BRIGHT_DATA_ZONE`: Bright Data [Zone](https://brightdata.co.kr/cp/zones) 이름(예: `web_unlocker1`)

### Direct configuration

또는 스크립트에서 CONFIG 객체를 직접 편집합니다:

```javascript
const CONFIG = {
  apiToken: process.env.BRIGHT_DATA_API_TOKEN || 'YOUR_API_TOKEN', // Replace with your actual token
  zone: process.env.BRIGHT_DATA_ZONE || 'web_unlocker1',           // Replace with your zone
  targetUrl: 'https://geo.brdtest.com/welcome.txt'                 // Replace with your target URL
};
```

## Running the example

1. `API token`과 `zone`을 구성했는지 확인합니다
2. 터미널에서 `node index.js`를 실행합니다
3. 결과는 콘솔 출력에서 확인합니다

## How it works?

1. 스크립트가 Bright Data의 Unlocker API エンドポイント로 POST リクエスト를 보냅니다
2. 認証 토큰과 대상 URL을 포함합니다
3. Bright Data의 Web Unlocker가 대상 URL에 액세스합니다
4. レスポンス가 스크립트로 반환되며 콘솔에 표시됩니다

## Troubleshooting

오류가 발생하는 경우:

- API 토큰이 올바른지 확인합니다
- zone 이름이 유효한지 확인합니다
- 대상 URL 형식이 올바른지 확인합니다

## Modifying the example

다른 URL을 요청하려면:
1. CONFIG 객체의 `targetUrl`을 업데이트합니다
2. 스크립트를 다시 실행합니다

## Additional resources

- [Bright Data Web Unlocker API](https://docs.brightdata.com/scraping-automation/web-unlocker/introduction)
- [Get an API Token](https://docs.brightdata.com/general/account/api-token)
- [Manage Zones](https://brightdata.co.kr/cp/zones)

**Note:** 이는 교육 목적의 예시 구현입니다. 프로덕션 환경에서 사용하려면 추가적인 오류 처리, 로깅 및 보안 조치를 추가하는 것을 고려하시기 바랍니다.