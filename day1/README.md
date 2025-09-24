# Vue.js 1일차 학습 정리

## 🎉 학습 완료!

오늘 Vue.js의 핵심 개념들을 모두 학습하고 완전히 작동하는 앱을 만들었습니다!

## 📚 학습한 내용들

- Vue.js 기본 개념 (MVVM 패턴, 선언적 렌더링)
- Vue 설치 및 연결 (CDN 방식)
- createApp() 함수와 인스턴스 생성
- 머스타치 문법 ({{ }}) - 텍스트 표시
- v-bind 디렉티브 - HTML 속성 바인딩
- v-model 디렉티브 - 양방향 데이터 바인딩
- methods - 함수 정의 및 이벤트 처리
- v-text, v-html 디렉티브 - 텍스트 및 HTML 렌더링
- 반응성 시스템 - 데이터 변경 시 자동 화면 업데이트

## 🔑 핵심 개념 정리

### 1. 머스타치 문법 ({{ }})
```html
<h1>{{message}}</h1>
<p>이름: {{profile.이름}}</p>
```
- 텍스트 내용을 Vue 데이터로 표시
- 가장 기본적인 데이터 바인딩 방법

### 2. v-bind 디렉티브
```html
<img v-bind:src="imageUrl" v-bind:alt="imageAlt">
<a v-bind:href="linkUrl">{{linkText}}</a>
```
- HTML 속성에 Vue 데이터를 연결
- 줄임 표현: :src="imageUrl" (v-bind:src의 줄임)
- API 데이터나 동적 이미지/링크에 유용

### 3. v-model 디렉티브 (양방향 바인딩)
```html
<input type="text" v-model="userInput" placeholder="입력해보세요">
<p>입력한 내용: {{userInput}}</p>
```
- 입력 필드와 Vue 데이터를 양방향으로 연결
- 사용자 입력 → 데이터 업데이트 → 화면 자동 반영
- React의 useState + onChange보다 훨씬 간단!

### 4. methods (메서드)
```javascript
methods: {
    changeMessage() {
        this.message = '메시지가 변경되었습니다'
        this.clickCount++
    },
    increaseAge() {
        this.profile.나이++
        this.clickCount++
    }
}
```
- Vue 인스턴스에서 사용할 함수들을 정의
- this로 Vue 인스턴스의 데이터에 접근 가능
- 이벤트 핸들러로 사용: @click="changeMessage"

## 🏆 학습 성과

- 완전히 작동하는 Vue 앱 구현 완료
- Vue의 핵심 디렉티브 5개 모두 실습
- 반응성 시스템 체험 및 이해
- React와의 차이점 파악 (v-model의 편리함)

## 🚀 다음 학습 계획 (2일차)

- 조건부 렌더링: v-if, v-show
- 리스트 렌더링: v-for
- 이벤트 처리: v-on, 이벤트 수식어
- 계산된 속성: computed
- 감시자: watch

## 💡 핵심 포인트

- Vue는 직관적이고 HTML 기반으로 쉽게 시작할 수 있음
- 반응성 시스템으로 데이터 변경 시 자동 화면 업데이트
- v-model은 React보다 훨씬 간단한 양방향 바인딩 제공
- 디렉티브 시스템(v-)으로 다양한 기능을 쉽게 구현

## 📁 파일 구조

```
day1/
├── day1.html          # 완성된 Vue.js 1일차 실습 파일
└── README.md          # 학습 정리 문서
```

## 🎯 실행 방법

1. `day1.html` 파일을 브라우저에서 열기
2. 모든 기능이 정상 작동하는지 확인
3. 개발자 도구(F12)로 Vue 데이터 변화 관찰

---

**축하합니다! Vue.js 1일차 학습을 성공적으로 완료하셨습니다!** 🎉