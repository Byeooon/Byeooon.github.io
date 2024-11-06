---
date : 2023-12-22
title : "[Python] Meaning of if __name__ ==\"__main__\""
comments : true
categories : 
    - Python
---

###### 오늘은 파이썬의 if __name__ == "__main__" 의 의미에 대해서 기록해보도록 하겠습니다.

###### if __name__ == "__main__" 을 사용하면 해당 파이썬 파일을 직접 실행했을 때 "__main__"이 참이 되어 if문 다음 문장이 수행됩니다.

###### 하지만 대화형 인터프리터나 다른 파일에서 이 모듈을 불러 사용할 때는 __name__ == "__main__"이 거짓이 되어 if문 다음 문장이 수행되지 않습니다. 따라서 if __name__ == "__main__" 를 사용하여 원하지 않는 파이썬 파일의 실행을 막을 수 있습니다.