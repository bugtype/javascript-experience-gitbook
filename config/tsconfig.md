# tsconfig



* side effects
  * Tree Shaking 중 직접 평가하지 않는 이상, 사이드이펙트 여부를 알수 없다.
  * **Webpack이 ES Module로 의존성을 관리하는 모듈만 Tree Shaking을 한다**

```javascript
{
  "name": "your-project",
  "sideEffects": false
}

```



