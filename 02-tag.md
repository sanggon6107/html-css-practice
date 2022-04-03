# 02-tag에 대하여

## 1. 아이템과 박스
태그는 크게 두가지로 나뉜다.  


이삿짐을 옮길 때, "아이템"들을 "박스"에 담아 분류하는 것처럼, **html에는 실제로 눈에 보이는 item들과 그들을 담을 수 있는 box가 있다.**

1. 박스(box)  
1-1. header  
1-2. footer  
1-3. nav  
1-4. aside  
1-5. main  
1-6. section  
1-7. article : 반복성이 있는 것들을 섹션 안에 넣을 때 사용된다.  
1-8. div : 버튼과 텍스트를 묶어서 스타일링 하고 싶을 때 사용할 수 있다.  
1-9. span  
1-10. form

1. 아이템(item)  
2-1. a : 앵커. 링크를 걸 수 있다.  
2-2. button  
2-3. input  
2-4. label  
2-5. img  
2-6. video  
2-7. audio  
2-8. map  
2-9. canvas  
2-10. table  

## 2. html body의 구조
html 은 기본적으로 다음과 같은 구조를 취한다.

![html 구조](https://github.com/sanggon6107/python-opencv-practice/blob/master/card_crop_1.png?raw=true)  
↑*html의 기본 구조*


## 3. 아이템의 분류
아이템은 block레벨과 inline레벨로 나뉜다.  
인라인 레벨의 태그는, 공간이 옆에 남으면 아이템을 작성하는 대로 기존 아이템의 옆에 배치된다. 반면 block레벨의 태그는 한 줄에 한 개만 둘 수 있으므로 바로 뒤에 적더라도 밑에 아이템이 배치된다.


## 4. 엘리먼트와 테그의 Attributes
```html
<p>content</p>
```
처음부터 끝까지 \<p>content\</p>를 element라고 부른다.  
\<p>를 opening tag, \</p>를 closing tag라고 부른다.  
안에 내용물을 content라고 부른다.  

```html
<p class="editor-note"> content </p>
```

태그는 attributes를 가질 수 있다. 해당 태그 내에서 적용되는 property를 설정하는 것. 클릭이 가능하지 않게 하거나, 투명한 버튼 등을 만들 수 있다.  
>> 참고 : id와 class는 무엇이 다른가?  
id는 유일하고, class는 같은 이름으로 중복 사용 가능하다.  
또, 한 요소는 여러개의 클래스를 가질 수 있지만 여러개의 id는 가질 수 없다.