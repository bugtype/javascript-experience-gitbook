# rxjs



### I. 시각화 사이트

{% embed url="https://rxviz.com/" %}

{% embed url="https://rxmarbles.com/" %}



### II. 자주 사용된 스크립트



#### 1. 먼저 응답이 온 Observable만 받아오기 \(race\)

```typescript
//take the first observable to emit
race(
  //emit every 1.5s
  interval(1500).pipe(mapTo('aaaaaaaa')),
  //emit every 1s
  interval(1000).pipe(mapTo('bbbbbb')),
  //emit every 2s
  interval(2000).pipe(mapTo('cccccc')),
  //emit every 2.5s
  interval(2500).pipe(mapTo('ddddd')),
);

//output: bbbbbb (1초) bbbbbb (1초) bbbbbb
```



#### 2. 모든 응답이 오고 방출하기 \(zip\)

```typescript
const sourceOne = of('Hello');
const sourceTwo = of('World!');
const sourceThree = of('Goodbye');
const sourceFour = of('World!');

zip(
  sourceOne,
  sourceTwo.pipe(delay(1000)),
  sourceThree.pipe(delay(2000)),
  sourceFour.pipe(delay(3000))
);
//output: (3초 후...) ["Hello", "World!", "Goodbye", "World!"]
```

#### 3. 마지막 응답 pushing 할때 자주사용 \(shareReplay\)

```text
https://www.learnrxjs.io/learn-rxjs/operators/multicasting/sharereplay


```



