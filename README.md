# 10장 List&Key

## List

리스트는 같은 아이템을 순서대로 모아둔 것으로, 배열(array)로 이루어져 있으며, 배열은 변수나 객체들을 하나의 변수로 묶어둔 것을 의미합니다. React에서는 이러한 배열을 활용하여 엘리먼트들을 리스트 형태로 렌더링할 수 있다.

## Key

key는 각 객체나 아이탬을 구분할 수 있는 고유한 값을 의미한다.

리액트에서는 리스트에 존재하는 아이탬들을 구분하기 위한 고유한 문자열을 의미한다. 그렇기에 List내에서 고유한 값을 가져야 하며 보통 id를 Key 값으로 사용하거나 index값을 Key 값으로 사용한다. 만약 index 값을 key값으로 사용하는 경우에는 List 내부의 값이 변경되면 index값이 바뀌기 때문에 오류가 생길 수 있다.

리액트에서는 Key를 명시적으로 넣어주지 않으면 기본값으로 Index값을 키값으로 넣어준다.

## 다수의 Component를 렌더링 하기

화면에 반복적으로 나타나는 컴포너트를 효율적으로 나타내기 위해 **map()**함수를 이용한다.

사용법

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/882faac6-85d4-401a-8eaa-9fa718c0f761/fdbe3a17-2f3c-4d54-9082-2178c17ef120/image.png)

map()을 활용하면 첫 번째 요소부터 순서대로 어떠한 연산을 수행한 뒤 배열에 순서대로 넣는 것이 가능하다.

React에서 map()사용해 엘리먼트를 랜더링 하는 코드

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/882faac6-85d4-401a-8eaa-9fa718c0f761/efc9c6ff-c2f8-440e-bc74-99657cb572c7/image.png)

numbers 배열의 1부터 5까지의 요소들을 map() 함수를 사용하여 각 요소를 <li> 태그로 감싼 뒤, 그 결과를 listItems에 저장 하고 ReactDOM.render()에서 <ul> 태그로 listItems를 감싸 화면에 렌더링하는 코드이다.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/882faac6-85d4-401a-8eaa-9fa718c0f761/50c891d8-c8d5-49e2-8bc5-32d16cd9d745/image.png)

위 코드와 같이 map()를 사용할때 key값을 지정해주지 않고 map()함수를 사용해 list배열을 만들면 key값이 없다는 오류가 뜬다.
