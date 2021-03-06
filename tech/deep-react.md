# Deep React

{% hint style="info" %}
별도의 Gitbook으로 옮길예정
{% endhint %}

### 

#### I. shallow equal 코드

```javascript


// reference : https://stackoverflow.com/questions/36084515/how-does-shallow-compare-work-in-react 

// https://github.com/facebook/fbjs/blob/master/packages/fbjs/src/core/shallowEqual.js#L39-L67
function shallowEqual(objA: mixed, objB: mixed): boolean {
  if (is(objA, objB)) {
    return true;
  }

  if (typeof objA !== 'object' || objA === null ||
      typeof objB !== 'object' || objB === null) {
    return false;
  }

  const keysA = Object.keys(objA);
  const keysB = Object.keys(objB);

  if (keysA.length !== keysB.length) {
    return false;
  }

  // Test for A's keys different from B.
  for (let i = 0; i < keysA.length; i++) {
    if (
      !hasOwnProperty.call(objB, keysA[i]) ||
      !is(objA[keysA[i]], objB[keysA[i]])
    ) {
      return false;
    }
  }

  return true;
}
```



1. 같은 object인지 확인한다.
2. object가 아닌지 확인
3. 가지고 있는 key의 갯수가 같은지 확인
4. A가 가진 key를 가진지 체크, 같은 같은 property인지 체크

---

#### II. React 달라진점

* React 17 \([Naver D2](https://d2.naver.com/helloworld/7226235)\)
  * 이벤트 위임 방식 변경
  * JSX Transform
  * Event Pooling 제거
  * Native Component Stacks
* React 18 \([React blog](https://reactjs.org/blog/2021/06/08/the-plan-for-react-18.html)\)
  * Batch - [https://github.com/reactwg/react-18/discussions/21](https://github.com/reactwg/react-18/discussions/21)
  * startTransition - [https://github.com/reactwg/react-18/discussions/41](https://github.com/reactwg/react-18/discussions/41)





