# first-vue

This is my first vue project.

> 📝 궁금한 모든 것을 기록합니다.
> 😎 기록에서 멈추지 않고 나의 것으로 만듭니다.
> 🙈 잘못된 정보가 있다면 언제든지 댓글에 남겨주세요 :D

> 저는 언제나 리액트를 사용합니다. 그런데 어쩌다 Vue를 공부할 기회가 있어서 공부한 기록을 남깁니다.

![](https://images.velog.io/images/gunwooko/post/d2f2d536-2590-4a87-8180-1465606b8552/vue1.png)

# 🤔 VUE.JS?

공식문서에서 뷰는 사용자 인터페이스(UI)를 만들기 위한 프로그레시브 프레임워크라고 소개하고 있다.

## 🧐 특징

### 1. 유연하고 가볍다.

### 2. 기존의 웹앱의 일부 UI만 적용하는 것도 가능하다.

### 3. SPA를 위해 필요한 라우터기능도 지원한다.

### 4. 리액트처럼 가상DOM을 지원해서 빠른 UI 렌더링이 가능하다.

### 5. 컴포넌트 기반의 프레임워크이다.

### 6. 앵귤러처럼 양방향 데이터 바인딩이 가능하다.

화면에 표시되는 값과 모델 데이터 값이 동기화되어 한쪽이 변경되면 다른 한쪽 또한 자동으로 변경된다.

### 7. 리액트처험 단방향 데이터 흐름을 가지고 있다.

컴포넌트끼리 데이터를 전달할 때 항상 상위컴포넌트에서 하위컴포넌트 방향으로 데이터가 전달된다.

### 8. MVVM 패턴이다.

![](https://images.velog.io/images/gunwooko/post/34ea0ccf-2980-4a5c-9a9d-2c626467df8d/MVVMPattern.png)
Model - View - ViewModel 구조로 개발하는 방식이다. 화면의 요소를 제어하는 코드와 데이터 로직처리하는 코드를 분리하여 코드의 이해도를 높이고 유지 보수를 편리하게 해준다.
**View**는 사용자에게 보이는 화면이다.
**ViewModel**은 View와 Model의 중간 영역이고, _DOM 리스너_ 와 _데이터 바인딩_ 을 제공하는 곳이다.
**Model**은 데이터를 담는 위치로, 보통 서버에서 가져온 데이터를 JS 객체 형태로 저장한다.
**DOM Listener**는 DOM의 변경 상황에 즉각 반응해서 특정 로직을 수행하는 장치이다.
**Data Binding**은 View의 내용과 Model의 데이터를 동기화해주는 장치이다.

## 🔧 설치방법

페이지에 [CDN package](https://v3.ko.vuejs.org/guide/installation.html#cdn)로 import하는 방법도 있지만, npm을 이용해 설치하는 것을 권장한다.

```
// vue 설치하기
$ npm install vue@next

// vue cli 설치하기
yarn global add @vue/cli
// 아니면
npm install -g @vue/cli
```

```
// vue cli를 통한 프로젝트 생성 방법
vue create my-project
// 혹은 아래 명령어를 통해 ui로 프로젝트를 생성할 수 도 있다.
vue ui
```

## 📌 Vue 개발에 도움되는 툴 & 라이브러리

- #### [Vue Devtools](https://github.com/vuejs/vue-devtools#vue-devtools)

  Vue 앱을 보다 사용자 친화적인 인터페이스에서 검사하고 디버깅할 수있게 도와준다.

- #### [Vue-cli](https://cli.vuejs.org/)

  빠르게 애플리케이션을 구축하도록 도와준다.

- #### [Vue Router](https://router.vuejs.org/installation.html#direct-download-cdn)
  뷰를 이용하여 SPA을 제작할 때 유용한 라우팅 라이브러리이다. npm으로 설치하거나 CDN 방식으로 사용할 수 있다.

## 👀 References

- [Vue 공식문서](https://v3.ko.vuejs.org/guide/introduction.html)
- [MDN - Vue 시작하기](https://developer.mozilla.org/ko/docs/Learn/Tools_and_testing/Client-side_JavaScript_frameworks/Vue_getting_started)
- [Vue.js 입문서 - 프론트엔드 개발자를 위한](https://joshua1988.github.io/web-development/vuejs/vuejs-tutorial-for-beginner/#vue-components)
- [한시간만에 끝내는 Vue.js 입문](https://www.youtube.com/watch?v=sqH0u8wN4Rs)
- [Vue JS Crash Course 2021](https://www.youtube.com/watch?v=qZXt1Aom3Cs)
