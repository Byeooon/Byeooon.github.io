---
date : 2022-10-06
title : "[Android Studio] 페이지 연결시 Androidmanifest 설정"
comments : true
categories :
    - Android Studio
---

###### 안드로이드 스튜디오에서 페이지를 연결을 할 때, 꼭 수정해줘야하는 파일이 AndroidManifest.xml파일입니다.

<br>

###### AndroidManifest.xml에 아래와 같이 자바파일명을 포함한 activity를 추가해줘야 합니다.

```xml
<activity android:name=".SecondActivity" android:label="두번째 화면"/>
```