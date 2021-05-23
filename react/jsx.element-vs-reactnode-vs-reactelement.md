# JSX.Element vs ReactNode vs ReactElement

{% embed url="https://simsimjae.tistory.com/426" %}

{% embed url="https://velog.io/@winney\_77/JSX.Element-ReactNode-ReactElement" %}

\*\*\*\*



1. **React.element**는 type과 props를 가진 객체이다.
2. **ReactNode**는 ReactElement, ReactFragment, string, number, ReactNode의 Array, null, undefined, boolean이다.
3. **JSX.Element**는 props와 type이 any인 **제네릭 타입을 가진 ReactElement**이다

```typescript
// ReactNode는 boolean | null | undefined 가 포함.
type ReactNode = ReactChild | ReactFragment | ReactPortal | boolean | null | undefined;

```







![](../.gitbook/assets/image%20%281%29.png)

