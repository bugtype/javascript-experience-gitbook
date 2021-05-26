# Recoil



|  | context API | redux | recoil |
| :--- | :--- | :--- | :--- |
| React 내부 접근 | ✅ | ❌ | ✅ |
| 동시성 모드_\(실험적\)_ | ✅ | ❌ | ✅ |
| 디버깅 extension 제공 | ❌ | ✅ | ❌ |
| 서브셋을 대상으로 변경을 감지 | ❌ | ✅ | ✅ |





* **useRecoilState** : 기존 `useState` 와 같이 변경되는 값과 해당 값을 변경하는 함수를 반환합니다.
* **useRecoilValue** : 구독하는 값만 반환하는 함수입니다. 값의 update 함수가 필요없을 경우 사용합니다.
* **useSetRecoilState** : 구독하는 값을 변경하는 함수만 반환합니다.
* **useResetRecoilState**: 값을 기본값으로 reset 시키는 함수를 반환합니다.



* [https://ui.toast.com/weekly-pick/ko\_20200616](https://ui.toast.com/weekly-pick/ko_20200616)
* [https://blog.woolta.com/categories/1/posts/209](https://blog.woolta.com/categories/1/posts/209)

