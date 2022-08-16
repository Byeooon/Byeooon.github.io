---
date : 2022-08-15
title : "[Markdown] markdown Table 만들기"
comments : true
categories : 
    - MarkDown
---

###### 마크다운 문법 중 테이블(표)를 만드는 방법을 자세히 알아보도록 하겠습니다.

* 기본 표 만들기

```
|제목|내용|설명|
|---|---|---|
|💻1|💻2|💻3|
|💻4|💻5|💻6|
|💻7|💻8|💻9|
```

* 출력결과 

<img width="150" alt="스크린샷 2022-08-15 오후 2 49 47" src="https://user-images.githubusercontent.com/55019557/184583109-4c8551fe-2b38-482b-88ed-e356c387b874.png">

* 정렬하기

```
|제목|내용|설명|
|:---|---:|:---:|
|LEFT|RIGHT|CENTER|
|LEFT|RIGHT|CENTER|
|LEFT|RIGHT|CENTER|
```

* 출력

<img width="150" alt="스크린샷 2022-08-15 오후 2 51 40" src="https://user-images.githubusercontent.com/55019557/184583284-9c593f58-7cba-49a7-950b-6e46158407c4.png">

* 셀 확장

```
|제목|내용|설명|
|:---|:---:|---:|
||CENTER||
|||RIGHT|
|LEFT|||
```

* 출력 

<img width="150" alt="스크린샷 2022-08-15 오후 2 53 27" src="https://user-images.githubusercontent.com/55019557/184583447-c7988999-482f-4836-9c66-454fe49fdc19.png">

<br>

* 참고 : [www.markdownguide.org](https://www.markdownguide.org/extended-syntax/)
