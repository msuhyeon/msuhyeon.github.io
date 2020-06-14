---
title: "React-The complete guide"
date: 2020-06-14 10:46:00 -0400
categories: jekyll update
---

본 포스팅은 Udemy 강의 내용을 정리한 내용들 입니다.

Spread & Rest Operators


Spread 연산자는 점 3개이며, Array elements 혹은 Object elements를 분할하는데 사용된다.

const newArray = [...oldArray, 1, 2];
const newObject = {...oldObject, newProp: 5}

예를 들어 이전 배열이 있고 이전 배열의 모든 요소를 새 배열에 추가하고 1과 2 요소를 추가하려면 이 첫 번째 구문은 이전에 세 점 앞에 사용된다. array는 단순히 모든 요소를 꺼내고 대괄호로 만든 새 배열에 추가한다. 
물론 더 많은 요소를 추가 할 수 있다. 
따라서 대괄호와 함께 일반 구문을 사용하여 객체와 동일한 배열을 만든다.
새로운 prop으로 중괄호를 사용하여 새 객체를 만드는 ... 도 있다. 
이전 객체-기존 객체의 모든 속성과 해당 값을 가져와서 
키-값 쌍으로 기존 객체 인 경우 보조 메모로 키-값 쌍으로 추가한다. 
또한 새로운 property가 있다. 여기에서 새로운 prop5로 덮어쓰게 된다.

따라서 우리 자신의 property가 우선시 되어지는데, 이것이 스프레드 연산자이다.

REST 연산자는 동일한 연산자이지만 다르게 사용된다. 
여기서는 함수 인수 목록을 배열로 병합하는 데 사용된다.
그리고 이것은 우리가 그것을 사용하는 곳을 보여주는데, 함수 인수 목록에서 사용한다.

`Rest`
function sortArgs(...args){
  return args.sort();
}

sortArgs는 무제한의 인수를 받는다. 
따라서 하나의 인수, 둘, 셋 또는 무엇이든, ...으로 하나의 인수 인수를 작성하지만 
실제로 둘 이상의 인수를 수신 할 수 있으며 모두 하나의 배열로 병합된다. 
그런 다음 인수 목록에 배열 메소드를 적용하거나 편리하게 저장된 인수로 원하는 작업을 수행 할 수 있다.

const numbers = [1,2,3];
const newNumbers= [...numbers, 4];

console.log(newNumbers); // [1,2,3,4]

배열과 객체 모두에서 이 과정을 통해 배열이나 속성을 객체에 편리하게 복사하는 동시에 
오래된 객체를 안전하게 복사하는 것을 볼 수 있다.

const person = {
  name: 'Max';
}

const newPerson = {
  ...person,
  age: 28,
}

console.log(newPerson); 
// [Object object]{
//    name: 'Max',
//    age: 28
// }

이제 기능에서 사용 빈도가 적은 REST-Operator가 사용되며 ES6 화살표 기능도 사용할 수 있다.

Rest 파라미터는 Spread 연산자(...)를 
사용하여 함수의 파라미터를 작성한 형태를 말하는데, 이것은 Rest 파라미터를 사용하면 함수의 파라미터로 오는 값들을 배열로 전달 받을 수 있다는 뜻 이다.
