# defer, async

## Concept

- defer - 브라우저는 defer 속성이 있는 스크립트(이하 defer 스크립트 또는 지연 스크립트)를 '백그라운드’에서 다운로드 합니다. 따라서 defer 스크립트를 다운로드 하는 도중에도 HTML 파싱이 멈추지 않습니다. 그리고 defer 스크립트 실행은 페이지 구성이 끝날 때까지 지연 됩니다.
- async - async 속성이 붙은 스크립트(이하 async 스크립트 또는 비동기 스크립트)는 페이지와 완전히 독립적으로 동작합니다. async 스크립트는 defer 스크립트와 마찬가지로 백그라운드에서 다운로드됩니다. 따라서 HTML 페이지는 async 스크립트 다운이 완료되길 기다리지 않고 페이지 내 콘텐츠를 처리, 출력합니다(하지만 async 스크립트 실행중에는 HTML 파싱이 멈춥니다

## Flow

브라우저는 HTML을 읽다가 \<script\> 태그를 만나면 DOM 생성을 멈춘 후 스크립트를 다운밥고 실행한 후에야 남은 페이지를 처리한다. 이러면 스크립트 파일이 너무 크다면 유저가 페이지를 보는데 많은 시간이 필요할 것이다. 이에 대한 대책으로 스크립트 파일을 페이지의 맨 아래에 위치 시킬 수 있는데 이는 HTML문서가 아주 큰 경우 문제가 생길 수 있다. 이 문제를 해결할 수 있는 것이 defer, async 이다.

[ko.javascript.info/script-defer-async](https://ko.javascript.info/script-async-defer)

## Detail

- defer와 async의 공통점, 차이점은 무엇일까?

```
공통점 : 다운로드 시 페이지 렌더링을 막지 않는다.
차이점 : 스크립트 파일 실행이 defer은 문서 다운로드와 파싱이 완료된 후에 실행되고, async는 스크립트 파일이 다운로드 되는 동안은 문서 다운로드와 파싱이 진행되다가 스크립트 파일이 실행되면 파싱을 멈춘다.
```

![defer, async 차이](/images/async%2Cdefer.png)
