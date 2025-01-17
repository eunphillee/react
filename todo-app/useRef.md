useRef 훅은 React에서 DOM 요소나 값의 변경을 추적하거나 유지하기 위해 사용되는 훅입니다. 

1. DOM 접근 할때 사용 합니다. (document.getElementById()와 같음.)

 - reference (참고) 

useRef는 컴포넌트 내 특정 DOM 요소에 직접 접근할 때 유용합니다. 
일반적으로 DOM 요소에 접근해야 할 때 ref 속성을 사용해 DOM 노드에 연결합니다.
useRef로 반환되는 객체는 단 하나의 프로퍼티 current 를 가집니다:
    
    + current
    현재 참조하고 있는 값 또는 DOM 요소를 저장합니다.
    ref.current는 읽기/쓰기 모두 가능합니다. (ref는 current 속성이 없으면 쓸수없다. )
    React에서는 렌더링 주기와 관계없이 값을 유지합니다.
    [CalculateRef.js 참고]


2. 값 저장 (렌더링에 영향을 주지 않음)

useRef는 렌더링 사이에 값을 유지하지만 값이 변경되어도 컴포넌트가 다시 렌더링되지 않습니다.
이를 통해 렌더링과 무관한 값을 추적하거나 관리할 수 있습니다.


3. 변수처럼 사용 가능

useRef는 변경 가능한 current 속성을 가진 객체를 반환합니다. 
따라서 상태 관리가 필요 없거나 값이 자주 변경되더라도 렌더링이 필요하지 않은 경우 적합합니다.


4. useEffect와 결합

useRef를 useEffect와 함께 사용하여 컴포넌트가 마운트되거나 
언마운트될 때 특정 작업을 수행할 수 있습니다.

5. useRef는 값 변경 시 렌더링을 트리거하지 않습니다. 
값이 렌더링과 연관되어 있다면 상태(useState)를 사용하는 것이 적합합니다.
DOM 조작은 React의 선언적 접근 방식과는 다소 어긋날 수 있으므로 최소화하는 것이 좋습니다.

useRef는 값을 유지, DOM 접근, 상태 관리 대체 등 다양한 용도로 활용되며, 효율적인 리액트 컴포넌트 개발에 중요한 도구입니다.


