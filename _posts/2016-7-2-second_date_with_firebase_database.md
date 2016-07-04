---
layout: post
title: Firebase Realtime Database 사용하면서 드는 생각
---

[https://firebase.google.com/docs/database/android/save-data](https://firebase.google.com/docs/database/android/save-data)

1. '이게 정말 될까?' 생각이 드는 짧은 코드인데 제대로 동작한다.
안드로이드 앱에 적용하는 과정도 간단하다.
gradle 파일에 의존 패키지 추가하고 동기화하면 세팅이 끝난다.


2. rule을 잘 정해야한다.
몇일 전에 rule을 제대로(정말 제대로. 다른 uid는 쓰기기능에 접근을 못하도록) 정의했는데,
그게 잘 동작해서
``` updateChildren at / failed: DatabaseError: Permission denied ```
에러를 뱉어냈다.
처음엔 왜 퍼미션 에러가 날까 고민했는데,
알고보니 며칠 전에 정의했던 규칙때문이었다.
아무나 쓰기 가능하도록 정의하니 잘 동작했다.


3. 그러나, 읽고 쓰는 속도가 느리다.
아마도 서버가 바다 건너 있다보니 느릴 것이라 생각된다.
Callback 함수도 추가할 수 있으니,
ProgressDialog를 이용해서 그 시간을 처리하는 게 좋겠다.


4. 데이터를 받아오는 방법이 이벤트 리스너를 등록하고 처리하는 방법인데, 뭔가 생그럽다.
정렬도 그러하다.
