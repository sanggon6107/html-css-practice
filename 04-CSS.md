# CSS : Cascading Style Sheet

## 1. 의미
**html의 스타일을 지정한다.** 스타일의 세부 정의가 css파일(author style)에 지정되어 있다면 반영되고, css파일에 지정되어있지 않다면 User Style(브라우저 사용자가 지정한 다크모드 등의 세팅), 마지막으로 기본 브라우저의 스타일이 적용된다.


이 cascading의 연결고리를 끊는 것이 !important. 가능하면 쓰지 않는 것이 좋다.


html의 박스를 잘 작성해야 하는 이유는 박스를 적절히 작성해야 css로 스타일을 원하는 범위에 적용할 수 있기 때문이다.<br></br>

## 2. css selectors(선택자)

스타일을 적용할 **범위**를 선택한다.


1. Universal : *  
모든 태그를 고른다.
1. type : Tag  
해당 태그만 고른다.
2. ID : #id  
해당 id를 가진 범위에만 적용시킨다.
4. Class : .class  
해당 class를 가진 범위에만 적용시킨다.
5. State : ":"  
태그 뒤에 :로 특정 state에 대한 범위로 제한할 수 있다.
6. Attribute : []  
마찬가지로 태그 뒤에 []로 특정 Attribute를 가지는 경우에 대해서만 적용할 수 있다.<br></br>

## 3. practice

***html***
```html
<!DOCTYPE html>

<html>
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width">
    </head>
    <body>
        <ol>
            <li id = "id_1">First</li>
            <li>Second</li>
        </ol>
    <button>Button 1</button>
    <button>Button 2</button>
    <div class="red"></div>
    <div class="blue"></div>
    <a href="naver.com">Naver</a>
    <a href="https://google.com">google</a>    
    <a>Empty</a>
    </body>

</html>
```
<br></br>
  
css를 작성하는 방법은 아래와 같다.
```css
selector {
    property:value;
}
```
<br></br>
각 셀렉터에 대해 알아보면, 아래와 같다.
<br></br>

1. Universal selector : 전역에 대해 적용한다.  
```css
* {
    color:green;
}
```  
모든 범위에 color라는 property를 green으로 적용한다.  


2. type  
```css
li{
    color:blue;
}
```  
모든 li 태그에 대하여 적용한다. 이 때, 만약 universal selector와 함께 쓰였다면, li 타입이 universal보다는 구체적이기 때문에 우선순위를 가진다.  

3. id  
```css
#id_1{
    color:pink;
}
```  
\#뒤에 id이름을 적는다.  

한편, 아래와 같이 적으면 li의 해당 아이디에 대해서만 적용할 수도 있다.
```css
li #id_1{
    color:pink;
}
```  
4. class  
```css
.red{
    width:100px;
    height:100px;
    background:yellow;
}
```
클래스에 대해 스타일을 지정한다.  

5. state
```css
button:hover{
    color:red;
    background:beige;
}
```  
태그가 특정 state에 있을 때 적용시킨다.


6. Attribute  
```css
a [href]{
    color:purple;
}
```  
만약 앵커\<a> 중 href Attribute를 가지는 태그에만 적용시키고 싶다면 위와 같이 작성할 수 있다.

```css
a [href="naver.com"]{
    color:purple;
}
```  
위 처럼 작성하면 attribute가 href="naver.com"인 경우에 대해서만 적용한다.

```css
a [href^="naver"]{
    color:purple;
}
```  
위 처럼 작성하면 attribute의 href가 naver로 시작하는 모든 경우에 대해서 적용한다. 마찬가지로 &=를 사용하여 naver로 끝나는 경우에 대해서도 적용할 수 있다.<br></br>

## 4. padding, margin에 대하여

```css
.red{
    width:100px;
    height:100px;
    padding:20px;
    padding-top:100px;
    padding-right:100px;
    margin:20px;
    background:yellow;
}
```  

1. margin  
margin은 컨첸츠 바깥 영역에 대해 적용시킨다. 즉 컨첸츠 바깥 스페이스와 컨첸츠 사이의 거리.

2. padding  
padding은 컨첸츠 안쪽 영역에 대해 적용시킨다.

3. 속성 한번에 적용시키기 1   
top - right ....을 모두 적지 않고 아래 처럼 한번에 적용시킬 수 있다.


```css
.red{
   padding:20px 30px 30px 20px;
}
```  
이 경우, top - right - botton - left 순으로 적용된다.

4. 속성 한번에 적용시키기 2  
아래처럼 border의 여러 속성이 있다고 하자.
```css
.red{
    border-width:2px;
    border-style:solid;
    border-color:pink;
}
```  

아래처럼 한번에 적용할 수 있다.

```css
.red{
    border : 2px dashed pink;
}
```

>> 참고 : 속성값들은 css reference 웹사이트에 접속하면 참고할 수 있다.  
