# 원티드 프리온보딩 프론트엔드 챌린지 4월 사전과제

### 해당 깃헙 레포의 issue에 본인의 답변을 추가해주세요!

1. React Lifecycle에 대해 간단히 설명해주세요
# React Lifecycle

- 한국어로 생명주기 메서드
- 컴포넌트가 브라우저상에 나타나고, 업데이트되고, 사라질 때 호출되는 메서드들이다
- 클래스형 컴포넌트에서만 사용 가능하다

### 단계 별 보기

**마운트 - 발생 시점**

- `constructor`
    - 컴포넌트의 생성자 메서드, 만들어지면 가장 먼저 실행된다
- `getDerivedStateFromProps`
    - `props`로 받아온 것을 `state`에 넣어주고 싶을 때 사용한다
- `render`
    - 컴포넌트를 렌더링하는 메서드
- `componentDidMount`
    - 컴포넌트의 첫번째 렌더링 이후 호출되는 메서드
    - 이 시점에 우리가 만든 컴포넌트가 화면에 나타남

**업데이트 - 컴포넌트의 업데이트 시점**

- `getDerivedStateFromProps`
    - 마운트에서 나왔던 메서드
    - `props`나 `state`가 바뀌었을때에도 호출된다
- `shouldComponentUpdate`
    - 컴포넌트가 리렌더링 할 지 말 지 결정하는 메서드이다
    - 최적화할 때 사용한다(React.memo)와 역할이 비슷하다
- `render`
    - 컴포넌트를 렌더링한다
- `getSnapshotBeforeUpdate`
    - 컴포넌트에 변화가 일어나기 직전의 DOM 상태를 가져와서 특정 값을 반환하면 그 다음 발생하게 되는 `componentDidUpdate` 함수에서 받아와서 사용할 수 있다
- `componentDidUpdate`
    - 리렌더링을 마치고 화면에 원하는 변화가 모두 반영되고 난 후 호출되는 메서드

**언마운트 - 컴포넌트가 화면에서 사라지는 시점**

- `componentWillUnmount`
    - 컴포넌트가 화면에서 사라지기 직전에 호출된다

### 정리

클래스형 컴포넌트보다 함수형 컴포넌트를 사용하는 것이 권장되고 있는 지금 시기에 많이 사용되지 않을 것이라고 본다

---

생성 → constructor → getDerivedStateFromProps(생성, 업데이트) → shouldComponentUpdate(업데이트) → render(생성, 업데이트) → getSnapshotBeforeUpdate(업데이트) → React DOM 및 refs 업데이트(생성, 업데이트) → componentDidMount(생성), componentDidUpdate(업데이트)

삭제 → componentWillUnMount


### References

[https://react.vlpt.us/basic/25-lifecycle.html](https://react.vlpt.us/basic/25-lifecycle.html)
2. React18에서 업데이트 된 기능에 대해 설명해주세요
3. React18에서 추가된 hook들에 대해 설명해주세요
4. 요즘 관심있는 주제가 있다면 알려주세요
