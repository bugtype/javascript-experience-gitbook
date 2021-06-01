# state 종류



새로고침 해도 데이터가 유지 되어야 하는가?  
- query  
- local Storage  
- session Storage  
  
유저가 접근할 수 없어야 하는가?  
- useState



|  | useState | context API | history state | query  parmas \(url\) | cookie | local storage | session storage |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 새로고침 유지 | ❌ | ❌ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 뒤로가기 유지 | ❌ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 브라우져  탭 종료 | ❌ | ❌ | ❌ | ✅ | ❌ | ✅ | ✅ |
| 유저 접근 | ❌ | ❌ | ❌ | ✅ | ❌ | ❌ | ❌ |
| 유저 개발툴 접근 | ❌ | ❌ | ✅ | ✅ | ✅ | ✅ | ✅ |
| 사용 용도 | 페이지 상태관리 | 앱\(프로젝트\) 상태 관리  | 뒤로가기 상태 유지 \(SSR\) | url로 공유 등 |  |  |  |



