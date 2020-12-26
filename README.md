# ModerJavaScript
(javscript)If you go alone, you go fast, if you go together, you go far

## 모던 자바스크립트가 다루는 개념

[1. 자바스크립트란?](#1-자바스크립트란)

[2.1 Hello, World!](#21-hello-world)

[2.2 코드 구조](#22-코드-구조)

[2.3 엄격 모드](23-엄격-모드)

# Let Declaration
## 1. 자바스크립트란?

## 정의

*자바스크립트*는 ‘웹페이지에 생동감을 불어넣기 위해’ 만들어진 프로그래밍 언어입니다.

자바스크립트로 작성한 프로그램을 *스크립트(script)* 라고 부릅니다. 스크립트는 웹페이지의 HTML 안에 작성할 수 있는데, 웹페이지를 불러올 때 스크립트가 자동으로 실행됩니다.

스크립트는 특별한 준비나 컴파일 없이 보통의 문자 형태로 작성할 수 있고, 실행도 할 수 있습니다.

이런 관점에서 보면 자바스크립트는 [자바(Java)](https://en.wikipedia.org/wiki/Java_(programming_language))와는 매우 다른 언어라고 할 수 있습니다.

ℹ️ **왜 자바스크립트인가요?**

처음 자바스크립트가 만들어졌을 때는 LiveScript’라는 이름으로 불렸습니다. 그런데, 당시 자바의 인기가 아주 높은 상황이었습니다. 관련인들은 자바스크립트를 자바의 ‘동생’ 격인 언어로 홍보하면 도움이 될 것이라는 의사결정을 내리고 이름을 바꿨습니다.

이름은 자바에서 차용해 왔지만, 자바스크립트는 자바와는 독자적인 언어입니다. 꾸준히 발전을 거듭하면서 [ECMAScript](http://en.wikipedia.org/wiki/ECMAScript)라는 고유한 명세를 갖춘 독립적인 언어가 되었죠. 자바스크립트는 자바와 아무런 연관이 없습니다.

브라우저엔 '자바스크립트 가상 머신’이라 불리는 엔진이 내장되어 있습니다.

## 브라우저에서 할 수 있는 일

- 페이지에 새로운 HTML을 추가하거나 기존 HTML, 혹은 스타일 수정하기
- 마우스 클릭이나 포인터의 움직임, 키보드 키 눌림 등과 같은 사용자 행동에 반응하기
- 네트워크를 통해 원격 서버에 요청을 보내거나, 파일 다운로드, 업로드하기([AJAX](https://en.wikipedia.org/wiki/Ajax_(programming))나 [COMET](https://en.wikipedia.org/wiki/Comet_(programming))과 같은 기술 사용)
- 쿠키를 가져오거나 설정하기. 사용자에게 질문을 건네거나 메시지 보여주기
- 클라이언트 측에 데이터 저장하기(로컬 스토리지)

## 브라우저에서 할 수 없는 일

- 접근 제한, 확실한 보안
- 브라우저 내 탭과 창은 대개 서로의 정보를 알 수 없다, '동일 출처 정책'에 의해 동의와 관련된 특수한 자바스크립트 코드가 없다면 데이터 교환 X
- 서버와 쉽게 정보를 교환 가능, 타사이트나 도메인에서는 X

## 자바스크립트만의 강점

- HTML/CSS와 완전히 통합할 수 있음
- 간단한 일은 간단하게 처리할 수 있게 해줌
- 모든 주요 브라우저에서 지원하고, 기본 언어로 사용됨

## 자바스크립트 ‘너머의’ 언어들

- [CoffeeScript](http://coffeescript.org/)는 자바스크립트를 위한 'syntactic sugar’입니다. 짧은 문법을 도입하여 명료하고 이해하기 쉬운 코드를 작성할 수 있습니다. Ruby 개발자들이 좋아합니다.
- [TypeScript](http://www.typescriptlang.org/)는 개발을 단순화 하고 복잡한 시스템을 지원하려는 목적으로 '자료형의 명시화(strict data typing)'에 집중해 만든 언어입니다. Microsoft가 개발하였습니다.
- [Flow](http://flow.org/) 역시 자료형을 강제하는데, TypeScript와는 다른 방식을 사용합니다. Facebook이 개발하였습니다.
- [Dart](https://www.dartlang.org/)는 모바일 앱과 같이 브라우저가 아닌 환경에서 동작하는 고유의 엔진을 가진 독자적 언어입니다. Google이 개발하였습니다.

### 요약

- 자바스크립트는 브라우저에서만 쓸 목적으로 고안된 언어이지만, 지금은 다양한 환경에서 쓰이고 있습니다.
- 오늘날 자바스크립트는 브라우저 환경에서 가장 널리 사용되는 언어로 자리매김하였습니다. HTML/CSS와 완전한 통합이 가능합니다.
- 자바스크립트로 '트랜스파일’할 수 있는 언어는 많습니다. 각 언어마다 고유한 기능을 제공하죠. 자바스크립트에 숙달한 뒤에 이 언어들을 살펴볼 것을 추천드립니다.

## 2.1 Hello, World!

## 'script' 태그

```jsx
<!DOCTYPE HTML>
<html>

<body>

  <p>스크립트 전</p>

  <script>
    alert( 'Hello, world!' );
  </script>

  <p>스크립트 후</p>

</body>

</html>
```

<script> 태그엔 자바스크립트 코드가 들어갑니다. 브라우저는 이 태그를 만나면 안의 코드를 자동으로 처리합니다.

## 모던 마크업

<script> 태그엔 몇 가지 속성(attribute)이 있습니다.

- type 속성: <script type=…>
- language 속성: <script language=…>

## 외부 스크립트

자바스크립트 코드의 양이 많은 경우엔, 파일로 소분하여 저장할 수 있습니다.

이렇게 분해해 놓은 각 파일은 `src` 속성을 사용해 HTML에 삽입합니다.

```jsx
<script src="/path/to/script.js"></script>
```

물론 아래와 같이 URL 전체를 속성으로 사용할 수도 있습니다.

```jsx
<script src="https://cdnjs.cloudflare.com/ajax/libs/lodash.js/4.17.11/lodash.js"></script>
```

복수의 스크립트를 HTML에 삽입하고 싶다면 스크립트 태그를 여러 개 사용하면 됩니다.

```jsx
<script src="/js/script1.js"></script>
<script src="/js/script2.js"></script>
…
```

**`src` 속성이 있으면 태그 내부의 코드는 무시됩니다.**

`<script>` 태그는 `src` 속성과 내부 코드를 동시에 가지지 못합니다.

다음 코드는 실행되지 않습니다.

```jsx
<script *src*="file.js">
  alert(1); // src 속성이 사용되었으므로 이 코드는 무시됩니다.
</script>
```

따라서 `<script src="…">`로 외부 파일을 연결할지 아니면 `<script>` 태그 내에 코드를 작성할지를 선택해야 합니다.

위의 예시는 스크립트 두 개로 분리하면 정상적으로 실행됩니다.

```jsx
<script src="file.js"></script>
<script>
  alert(1);
</script>
```

### 요약

- 웹 페이지에 자바스크립트 코드를 추가하기 위해 `<script>` 태그를 사용합니다.
- `type` 과 `language` 속성은 필수가 아닙니다.
- 외부 스크립트 파일은 `<script src="path/to/script.js"></script>`와 같이 삽입합니다.

## 2.2 코드 구조

## 문

아래 코드는 'Hello World’를 두 개의 alert 문으로 나눈 예시입니다.

```jsx
alert('Hello'); alert('World');
```

코드의 가독성을 높이기 위해 각 문은 서로 다른 줄에 작성하는 것이 일반적입니다.

```jsx
alert('Hello');
alert('World');
```

## 세미콜론

줄 바꿈이 있다면 세미콜론(semicolon)을 생략할 수 있습니다.

아래 코드는 에러 없이 동작합니다.

```jsx
alert('Hello')
alert('World')
```

자바스크립트는 줄 바꿈이 있으면 이를 ‘암시적’ 세미콜론으로 해석합니다. 이런 동작 방식을 [세미콜론 자동 삽입(automatic semicolon insertion)](https://tc39.github.io/ecma262/#sec-automatic-semicolon-insertion)이라 부릅니다.

**대부분의 경우, 줄 바꿈은 세미콜론을 의미합니다. 하지만 '대부분의 경우’가 '항상’을 의미하진 않습니다.**

아래와 같이 줄 바꿈이 세미콜론을 의미하지 않는 경우도 있습니다.

```jsx
alert(3 +
1
+ 2);
```

세미콜론 자동 삽입이 일어나지 않았기 때문에 `6`이 출력됩니다. 어떤 줄이 `"+"` 로 끝나면, 그 줄은 '불완전한 표현식’이므로 세미콜론이 필요하지 않다는 걸 직감하실 겁니다. 위 코드도 이런 의도로 동작합니다.

대괄호`[...]`앞에는 세미콜론이 없을 시 세미콜론이 있다고 가정하지 않음.

```jsx
alert("에러가 발생합니다.")
[1, 2].forEach(alert)

alert("에러가 발생합니다.")[1, 2].forEach(alert)
```

## 주석

한줄 `//` 여러줄 `/* */`

## 2.3 엄격 모드

자바스크립트는 꽤 오랫동안 호환성 이슈 없이 발전해왔습니다. 기존의 기능을 변경하지 않으면서 새로운 기능이 추가되었죠.

덕분에 기존에 작성한 코드는 절대 망가지지 않는다는 장점이 있었습니다. 하지만 자바스크립트 창시자들이 했던 실수나 불완전한 결정이 언어 안에 영원히 박제된다는 단점도 생겼습니다.

이런 상황은 ECMAScript5(ES5)가 등장하기 전인 2009년까지 지속되었습니다. 그런데 새롭게 제정된 ES5에서는 새로운 기능이 추가되고 기존 기능 중 일부가 변경되었습니다. 기존 기능을 변경하였기 때문에 하위 호환성 문제가 생길 수 있겠죠? 그래서 변경사항 대부분은 ES5의 기본 모드에선 활성화되지 않도록 설계되었습니다. 대신 `use strict`라는 특별한 지시자를 사용해 엄격 모드(strict mode)를 활성화 했을 때만 이 변경사항이 활성화되게 해놓았습니다.

## use strict

지시자 `"use strict"`, 혹은 `'use strict'`는 단순한 문자열처럼 생겼습니다. 하지만 이 지시자가 스크립트 최상단에 오면 스크립트 전체가 “모던한” 방식으로 동작합니다.

예시:

```jsx
"use strict";

// 이 코드는 모던한 방식으로 실행됩니다.
...
```

명령어를 그룹화하는 방식인 함수에 대해선 곧 학습하도록 하겠습니다. 함수에 대해 학습하기 전에, `"use strict"`는 스크립트 최상단이 아닌 함수 본문 맨 앞에 올 수도 있다는 점을 알아두시기 바랍니다. 이렇게 하면 오직 해당 함수만 엄격 모드로 실행됩니다. 엄격 모드는 대개 스크립트 전체에 적용하지만 말이죠.

**`use strict`를 취소할 방법은 없습니다.**

자바스크립트 엔진을 이전 방식으로 되돌리는 `"no use strict"`같은 지시자는 존재하지 않습니다.

일단 엄격 모드가 적용되면 돌이킬 방법은 없습니다.

# 브라우저 콘솔

개발한 기능을 테스트하기 위해 [브라우저 콘솔](https://ko.javascript.info/devtools)을 사용하는 경우, 기본적으로 `use strict`가 적용되어있지 않는다는 점에 주의하셔야 합니다.

`use strict`에 영향을 받는 경우라면 개발자는 기대하지 않았던 결과를 얻을 수 있기 때문입니다.

그렇다면 어떻게 해야 콘솔에서 `use strict`를 사용할 수 있을까요?

'use strict’를 입력한 후, `Shift+Enter키`를 눌러 줄 바꿈 해 원하는 스크립트를 입력하면 됩니다. 아래와 같이 말이죠.

```jsx
'use strict'; <Shift+Enter를 눌러 줄 바꿈 함>
//  ...테스트하려는 코드 입력
<Enter를 눌러 실행>
```

이 기능은 Firefox와 Chrome 같은 유명한 브라우저에서 대부분 사용 가능합니다.

브라우저가 오래 되어서 콘솔 창에 `use strict`를 입력하는 게 불가능하다면, `use strict`를 적용하는 가장 확실한 방법은 아래와 같이 코드를 래퍼로 감싸면 됩니다.

```jsx
(function() {
  'use strict';

  // ...테스트하려는 코드...
})()
```

## 'use strict’를 꼭 사용해야 하나요

"당연히 사용해야 하는 거 아니야?"라는 생각이 드시겠지만, 꼭 그렇지만은 않습니다.

누군가는 스크립트 맨 윗줄엔 `"use strict"`를 넣는 게 좋다고 권유할 수 있습니다. 그런데 그거 아세요?

모던 자바스크립트는 '클래스’와 '모듈’이라 불리는 진일보한 구조를 제공합니다(클래스와 모듈에 대해선 당연히 뒤에서 학습할 예정입니다). 이 둘을 사용하면 `use strict`가 자동으로 적용되죠. 따라서 이 둘을 사용하고 있다면 스크립트에 `"use strict"`를 붙일 필요가 없습니다.

결론은 이렇습니다. **코드를 클래스와 모듈을 사용해 구성한다면 `"use strict"`를 생략해도 됩니다. 그런데 아직은 이 둘을 배우지 않았으니 `"use strict"`를 귀한 손님처럼 모시도록 하겠습니다.**

지금까지는 `use strict`의 일반적인 특징에 대해 알아보았습니다.

다음 챕터부터는 자바스크립트 언어가 제공하는 기능들을 하나씩 학습하면서 이 기능들이 엄격 모드와 비 엄격 모드에서 어떤 차이점을 보이는지 알아보겠습니다. 희소식을 알려드리자면 두 모드에서 차이를 보이는 기능이 많지 않다는 점과 엄격 모드를 사용하면 개발자의 삶의 질이 조금 더 높아진다는 점입니다.

그리고 특별한 언급이 없는 한 이 튜토리얼에 등장하는 모든 예시엔 엄격 모드를 적용할 예정입니다.
