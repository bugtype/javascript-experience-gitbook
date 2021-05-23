# 레거시 유지보수\) moment에서 date-fns로

약 1~2년 전에 date 관련 라이브러리를 고르는 이슈가 있었다.

moment가 대중적이였지만, 여러 단점이 보였고, 우리는 추후는 moment에서 다른 라이브러리로 변경될 수 있다고 생각하였다. 그래서 일단은 경험이 있는 **moment**를 사용하지만, 인터페이스를 제공하는 방식으로 구현하였다. 

기존 코드에서는 component, hooks, lib.. 등 어디서든 moment에 직접 접근 하였다

```text
// AS-IS Depeendacy
component, hooks ----> moment

// TO-BE Depeendacy
component, hooks ---> libs/date ----> moment

```

아니나 다를까... 추후에, **moment** 공식 Documentation에서 **이제 더이상 지원을 안한다**는 이슈가 올라왔다. 

우리는 미리 인터페이스르 제공하여, component, hooks 등에서 **moment** 의존성을 제거하였기 때문에 전체를 바꾸는 문제점이 발생하지 않았다. 덕분에 유지보수가 편해졌다.



#### 결론

* 변경될 여지가 있으면, 인터페이스를 제공하여, 유지보수성을 올리자



