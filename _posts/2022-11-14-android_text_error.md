---
date : 2022-11-14
title : "[Android Studio] TextVieww android:text error"
comments : true
categories :
    - Android Studio
---

###### 안드로이드 스튜디오 TextView에서 android:text를 사용할 때 유의할 점을 기록해보도록 하겠습니다.

```xml
android:text="<테스트 문자열>"
```

###### 위와 같은 경우, text부분이라도 <>를 넣게되면 오류가 나는 경우가 있었습니다. 또한 오류표시가 바로 뜨지 않기 때문에 오류를  한번에 발견하기 쉽지 않았습니다. 따라서 text부분에는 <>를 넣지 않도록 주의하는 것이 좋을 것 같습니다.
