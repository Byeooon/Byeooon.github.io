---
date : 2022-09-11
title : "[Github] Connect github repository with local"
comments : true
categories : 
    - Github
---

###### Github 레포지토리와 로컬 저장소를 연동하는 방법에 대해 정리해보도록 하겠습니다.

* 먼저 해당 레포지토리를 원하는 위치에 클론해줍니다.

```python
git clone "[Repository Address]"
```

* config 명령어를 통해 이름과 이메일이 등록되어있는지 확인해줍니다.

```pyhon
git config --list
```

* 등록되어있지 않은 경우, 아래의 명령어를 통해 등록해줍니다.

```pyhon
git config user.name [User Name]
git config user.email [Email Address]
```

* 다시 확인을 해보면 등록되어있는 것을 확인할 수 있습니다.

```pyhon
git config --list
```

---

* 추가적으로 브랜치를 이동하고 싶으면, 아래의 checkout명령어를 통해 이동할 수 있습니다.

```python
git checkout [Bracnh Name]
```