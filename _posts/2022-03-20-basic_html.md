---
date : 2022-03-20
title : "[Html] Html 기본 정리"
comments : true
categories : 
    - Html
---
오늘은 다양한 언어의 기반이 되는 Html에 대해 공부해보았다. 다른 언어를 배우려고 할 때 Html을 기본적으로 알고있어야 하는 경우가 많아서 공부하게되었다. Html이 웹페이지를 위한 마크업 언어여서 그런지 markdown과도 유사한 부분이 꽤 있는 것 같다.<br/>
아래는 직접 Html로 직접 페이지를 만들어가면서 공부해본 소스코드이다.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>My website</title>
</head>
<div style="display: flex;">
    <h1>First page</h1>
    <body>
        <h1>h1</h1> <!--글자 크기별 조절-->
        <h2>h2</h2> 
        <h3>h3</h3>
        <h4>h4</h4>
        <h5>h5</h5>
        <h6>h6</h6> 
        <p>
            "P tag for sentence"<br/>
            <strong>"Hello world!"</strong>
            
        </p>
        <input type="text" style="width: 200px; height: 100px; font-size: 50px;">
        <div>
            <button style="width: 200px; height: 100px;font-size: 30px;">Button_1</button>
        </div>
        <br/>
        <div>
            <button style="width: 200px; height: 100px;font-size: 30px;">Button_2</button>
        </div>
        <br/>
        <a href="https://byeooon.github.io" style="font-size: 30;">Let's go!</a>
</div>
<div>
    <div>
        <h1>Second page</h1>
    </div>
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/61/HTML5_logo_and_wordmark.svg/800px-HTML5_logo_and_wordmark.svg.png" style="width: 100px; height: 100px;" alt="fail to load!"><br/>
    <!--alt 태그는 이미지 로딩실패시 뜨는 문구 -->
    <ul style="font-size: 25px;">
        <li>1</li>
        <li>2</li>
        <li>3</li>  <!--목록화-->
    </ul>
    <ol style="font-size: 25px;">
        <li>A</li>
        <li>B</li>
        <li>C</li>  <!--자동 숫자화-->
    </ol>
    <br/>
    <!--각주 사용할 떄는 이와 같이 사용한다-->
    <table summary = "table" style="width: 300;height: 300;">
        <caption>Table name</caption>
        <tr>
            <th>name</th>
            <th>number</th>
            <th>age</th>
        </tr>
        <tr>
            <td>byeon</td>
            <td>1234</td>
            <td>23</td>
        </tr>
    </table>
</div>
<div>
    <h1>third page</h1>
    <form>
        <input type="text"style="font-size: 30px;">
        <input type="email"style="font-size: 30px;">
        <input type="password"style="font-size: 30px;">
        <input type="date"style="font-size: 30px;">
        <input type="checkbox" style="font-size: 50px;">Check!</input><br/>

        <select name="Animals" style="font-size: 50px;">
            <option value="1">tiger</option>
            <option value="2">cow</option>
            <option value="3">bear</option>
        </select>

        <button type="submit" style="font-size: 30px;">SUBMIT!</button>
    </form>
</div>
    </body>
</body>
</html>
```