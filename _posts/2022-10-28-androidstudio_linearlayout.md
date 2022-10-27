---
date : 2022-10-27
title : "[Android Studio] Linear Layout 정렬방식"
comments : true
categories :
    - Android Studio
---

###### Linear Layout은 순서대로 객체들이 쌓이기 때문에 단순하게 객체들을 추가하다보면 객체들이 화면밖으로 나가는 경우가 생기기 때문에 추가로 설정을 해줘야합니다. 간단하게 Linear Layout의 정렬 방법에 대해 기록해보도록 하겠습니다.

* ex)


```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical">
```

###### 위와 같이 android:orientation 을 추가해서 원하는 방향으로 정렬해줄 수 있습니다.