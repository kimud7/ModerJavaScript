# ModerJavaScript
*본 문서는 <a href=https://ko.javascript.info/intro>모던자바스크립트</a>를 보고 정리한 문서입니다.*

## Javascript란?
웹을 구성하는 요소(HTML,CSS) 중 하나로 웹 브라우저에서 동작하는 프로그래밍 언어입니다.

또한 자바스크립트는 인터프리터 언어로 개발작 별도으 컴파일을 하지 않아도 되는 언어입니다. 

이러한 인터프린터의 단점은 속도가 느리다라는점이 있었지만,모던 자바스크립트 에서는 인터프리터와 컴파일러의 장점으 결합하여 단점을 극복했습니다.

자바스크립트의 특징은 명령형, 함수형, 프로토타입 기반의 객체지햐 언어라는 점이 있습니다. 


## javascirpt가 브라우저에서 할수있는일

- 페이지에 새로운 HTML을 추가하거나 기존 HTML, 혹은 스타일 수정하기

- 마우스 클릭이나 포인터의 움직임, 키보드 키 눌림 등과 같은 사용자 행동에 반응하기

- 네트워크를 통해 원격 서버에 요청을 보내거나, 파일 다운로드, 업로드하기(AJAX나 COMET과 같은 기술 사용)

- 쿠키를 가져오거나 설정하기. 사용자에게 질문을 건네거나 메시지 보여주기

- 클라이언트 측에 데이터 저장하기(로컬 스토리지)

## javascirpt가 브라우저에서 할수없는일

- 웹페이지 내 스크립트는 디스크에 저장된 임의의 파일을 읽거나 쓰고, 복사하거나 실행할 때 제약을 받을 수 있습니다. 운영체제가 지원하는 기능을 브라우저가 직접 쓰지 못하게 막혀있기 때문입니다.

- 브라우저 내 탭과 창은 대개 서로의 정보를 알 수 없습니다. 그런데 자바스크립트를 사용해 한 창에서 다른 창을 열 때는 예외가 적용됩니다. 하지만 이 경우에도 도메인이나 프로토콜, 포트가 다르다면 페이지에 접근할 수 없습니다.

- 자바스크립트를 이용하면 페이지를 생성한 서버와 쉽게 정보를 주고받을 수 있습니다. 하지만 타 사이트나 도메인에서 데이터를 받아오는 건 불가능합니다. 
