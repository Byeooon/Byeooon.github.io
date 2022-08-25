---
date : 2022-08-25
title : "[Google Colab] Google Colab 런타임 유지 코드"
comments : true
categories :
    - Google Colab
---

###### 코랩의 런타임을 유지시킬 수 있는 방법에 대해 알아보도록 하겠습니다.

* 코랩 무료버전 최대 런타임 : 12시간

* 입력이 없을 런타임이 종료되는 시간 : 90분

-----

###### 적용 방법

- F12를 눌러줍니다(개발자 모드).

- Console 창을 눌러줍니다.

- 맨 아랫부분에 아래의 코드를 붙여넣고 Enter를 입력해줍니다.


* 소스코드 

```javascript
function ClickConnect(){
	console.log("Working"); 
	document.querySelector("colab-toolbar-button").click() 
} setInterval(ClickConnect, 1800000)
```