# package.json



* side effects
  * Tree Shaking 중 직접 평가하지 않는 이상, 사이드이펙트 여부를 알수 없다.
  * **Webpack이 ES Module로 의존성을 관리하는 모듈만 Tree Shaking을 한다**

```javascript
{
  "name": "your-project",
  "sideEffects": false
}

```



* peerDependencis
  * 호환성 체크

```javascript
"peerDependencies": {
    "tea": "2.x"
}

// 
├── tea-latte@1.3.5
└── tea@2.2.0
```



참고

* [https://programmingsummaries.tistory.com/385](https://programmingsummaries.tistory.com/385)

