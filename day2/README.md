# Vue.js Day 2 학습 내용

## 🎯 학습 목표
- Vue 디렉티브 활용하기
- 이벤트 처리 방법 익히기

## 📚 학습한 내용

### 1. 조건부 렌더링
- **v-if**: 조건에 따라 DOM 요소를 완전히 추가/제거
- **v-else-if, v-else**: 연쇄적인 조건부 렌더링
- **v-show**: 조건에 따라 요소의 표시/숨김만 제어 (display: none)

### 2. 리스트 렌더링
- **v-for**: 배열, 객체, 숫자 범위 반복
- **:key**: 각 항목을 고유하게 식별하기 위한 필수 속성

### 3. 이벤트 처리
- **v-on (@)**: 이벤트 핸들러 연결
- **이벤트 수식어**: .prevent, .stop, .once, .enter 등

## 🏆 실습 프로젝트

### TodoList 앱
- 할 일 추가/삭제 기능
- 체크박스로 완료 상태 토글
- 실시간 통계 표시 (전체/완료/미완료)

## 🔑 핵심 개념

### v-if vs v-show
| 특징 | v-if | v-show |
|------|------|--------|
| DOM 조작 | 요소 추가/제거 | display 토글 |
| 성능 | 초기 렌더링 비용 높음 | 토글 비용 높음 |
| 사용 시기 | 자주 변경되지 않는 경우 | 자주 토글되는 경우 |

### v-for 사용법
```html
<!-- 배열 렌더링 -->
<div v-for="item in items" :key="item.id">
    {{item.name}}
</div>

<!-- 객체 렌더링 -->
<div v-for="(value, key) in object" :key="key">
    {{key}}: {{value}}
</div>
```

### 이벤트 처리
```html
<!-- 기본 이벤트 -->
<button @click="handleClick">클릭</button>

<!-- 이벤트 수식어 -->
<form @submit.prevent="onSubmit">
    <button @click.stop="doThis">클릭</button>
</form>

<!-- 키 이벤트 -->
<input @keyup.enter="submit">
```

## 💡 학습 포인트

- Vue의 디렉티브 시스템이 매우 직관적이고 강력함
- v-if와 v-show의 차이점을 명확히 이해하는 것이 중요
- v-for에서 :key는 성능과 정확성을 위해 반드시 필요
- 이벤트 수식어로 복잡한 이벤트 처리를 간단하게 해결
- 실제 프로젝트(TodoList)를 통해 모든 개념을 통합적으로 학습

## 🚀 다음 학습 계획 (Day 3)
- 계산된 속성: computed
- 감시자: watch
- 컴포넌트 기초
- Props와 Emits
- 슬롯(Slot) 개념