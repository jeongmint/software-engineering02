# Markdown Syntax 정리

<br/>



## 1. Headings(제목)

* h1 부터 h6 까지 '#' 기호를 통해 헤더 층위 변경

```markdown
# h1

## h2

### h3

#### h4

##### h5

###### h6

```
==== **결과** ====

# h1

## h2

### h3

#### h4

##### h5

###### h6

============ <br/><br/>

---

## 2. Paragraphs(문단)

* 마크다운 문법은 한 줄 씩 띄어서 작성하는 것이 원칙이며 제목과 문단 조합을 사용하기 위해서는 다음과 같이 사용

```markdown

# 제목

<p>제목에 해당하는 문단입니다.</p>

```

==== **결과** ====

# 제목

<p>제목에 해당하는 문단입니다.</p>

============ <br/><br/>

* 제목을 # 외에 '=' 혹은 '-' 를 사용하여 나타낼 수 있음

```markdown

h1
===============

h2
---------------

### h3
```

==== **결과** ====

h1
===============

h2
---------------

### h3

============ <br/><br/>

---

## 3. Line Breaks(개행)

* 문단 상에서 엔터를 여러 번 친다고 개행이 되지 않기 때문에 강제 개행을 위해서는 <br/>
<
br/> 태그를 사용

```markdown

## LILAC

오 라일락 꽃이 지는 날 goodbye<br/>
이런 결말이 어울려<br/>
안녕 꽃잎 같은 안녕<br/>

```

==== **결과** ====

## LILAC

오 라일락 꽃이 지는 날 goodbye<br/>
이런 결말이 어울려<br/>
안녕 꽃잎 같은 안녕<br/>

============ <br/><br/>

---

## 4. Emphasis(강조)

### - *(Italic)이탤릭체*

```markdown

이탤릭체는 *Italic* 혹은 _Italic_ 처럼
하나의 '*' 혹은 '_'를 문자 양 옆에 사용

```

### - **(Bold)볼드체**

```markdown

볼드체는 **Bold** 혹은 __Bold__ 처럼
두 개의 '**' 혹은 '__'를 문자 양 옆에 사용

```

### - __*(Italic & Bold)이탤릭 & 볼드체 동시 사용*__

```markdown

이탤릭과 볼드체를 동시에 사용하기 위해
__*Italic & Bold*__ 사용

```

### - <u>(Underline)밑줄</u>

```markdown

밑줄은 <u>Highlight it!</u> 처럼
태그 <u>를 문자 양 옆에 사용

```

### - ~~(Strikethrough)취소선~~

```markdown

취소선은 ~~Cancel it!~~ 처럼
두 개의 물결 '~~'을 문자 양 옆에 사용

```

==== **결과** ====

-이텔릭체는 *Italic* 혹은 _Italic_

-볼드체는 **Bold** 혹은 __Bold__

-이탤릭과 볼드 __*Italic & Bold*__

-밑줄은 <u>Highlight it!</u>

-취소선은 ~~Cancel it!~~


============ <br/><br/>

---

<br/>

## Escaping Characters (추후에 서술되는 11. Escaping Characters 참고)

### ' \* '와 ' \_ '를 문자로 사용하고 싶을 때

해당 문자를 이탤릭체가 아닌 텍스트 문자로 사용하고자 할 때는<br/>
이스케이프 문자 ' \ '를 이용

```
이스케이프 문자로 양 옆에 *과 _ 표시하기

\* Veritas Lux Mea \*
\__ Veritas Lux Mea \__
```

==== **결과** ====



\* Veritas Lux Mea \*

\__ Veritas Lux Mea \__

<br/>

---
<br/>

## 5. Blockquotes(인용구)
- 단일인용 : '>' 를 사용하여 표현
```
느낌이 오잖아 떨리고 있잖아 언제까지 눈치만 볼 거니 네 맘을 말해봐 딴청 피우지 말란 말이야 네 맘 가는 그대로 지금 내 손을 잡아
```
> 느낌이 오잖아 떨리고 있잖아
언제까지 눈치만 볼 거니
네 맘을 말해봐 딴청 피우지 말란 말이야
네 맘 가는 그대로 지금 내 손을 잡아

- 중첩인용 : '>' 를 중첩해서 사용
```
> 우연히 고개를 돌릴 때 마다 눈이 마주치는 건 몇일밤 내내 꿈속에 나타나 밤새 나를 괴롭히는 건
>> 그 많은 빈자리 중에서 하필 내 옆자릴 고르는 건 나도 모르게 어느새 실없는 웃음 흘리고 있다는 건
>>> 그럼 말 다했지 뭐 우리 얘기 좀 할까
>>>> 느낌이 오잖아 떨리고 있잖아 언제까지 눈치만 볼 거니 네 맘을 해봐 딴청 피우지 말란 말이야 네 맘 가는 그대로 지금 내 손을 잡아
```
> 우연히 고개를 돌릴 때 마다 눈이 마주치는 건 몇일밤 내내 꿈속에 나타나 밤새 나를 괴롭히는 건
>> 그 많은 빈자리 중에서 하필 내 옆자릴 고르는 건 나도 모르게 어느새 실없는 웃음 흘리고 있다는 건
>>> 그럼 말 다했지 뭐 우리 얘기 좀 할까
>>>> 느낌이 오잖아 떨리고 있잖아 언제까지 눈치만 볼 거니 네 맘을 해봐 딴청 피우지 말란 말이야 네 맘 가는 그대로 지금 내 손을 잡아


---

## 6. Lists(리스트)

### 순서가 있는 리스트(Ordered)
- 정렬된 숫자 뒤에 '.' 붙여 사용
( 0 이상의 정수여야 함 )

```
1. 순서 1
2. 순서 2
3. 순서 3
```
1. 순서 1
2. 순서 2
3. 순서 3
---

- 공백을 활용하여 중첩리스트 표현

```
1. 순서 1
2. 순서 2
3. 순서 3
    1. 순서 3-1
    2. 순서 3-2
4. 순서 4
```

1. 순서 1
2. 순서 2
3. 순서 3
    1. 순서 3-1
    2. 순서 3-2
4. 순서 4

<br/>

### 순서가 없는 리스트(Unordered) : 마커는 *, +, - 를 사용
* '*' 표현

```
* 리스트 1
* 리스트 2
```
* 리스트 1
* 리스트 2
---
+ '+' 표현

```
+ 리스트 1
+ 리스트 2
```
+ 리스트 1
+ 리스트 2
---
- '-' 표현

```
- 리스트 1
- 리스트 2
```
- 리스트 1
- 리스트 2

모두 동일하게 표현되기 때문에 어떤 것을 사용하여도 무방

---

 * 2 개의 공백(space)만을 삽입하여 중첩리스트 표현
```
- 리스트 1
(space)(space)- 리스트 2
(space)(space)(space)(space)- 리스트 3
```
- 리스트 1
  - 리스트 2
    - 리스트 3
<br/>

* 2 개를 사용하지 않고 1개의 공백을 사용하면 다음과 같이 하나의 계층으로 출력

```
- 리스트 a
  - 리스트 b
   - 리스트 c
    - 리스트 d
     - 리스트 e 
```

- 리스트 a
  - 리스트 b
   - 리스트 c
    - 리스트 d
     - 리스트 e 

---
* 리스트와 인용구를 활용하여 다음과 같이 작성 가능, 그러나 빈 리스트가 존재할 때는 빈 리스트가 어느 상황에서든 출력되지 않음

```
* 리스트 a
  > 리스트 b
  >
* 리스트 c
```

* 리스트 a
  > 리스트 b
  >
* 리스트 c

---
<br>

### Task Lists

* 리스트를 활용하여 작업 목록 체크리스트를 대괄호 []를 리스트의 숫자 대신 붙여 작성할 수 있음

```
- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item
```
  
- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item


---
<br>


## 7. Code(코드 작성)

* Syntax highlighting 이라고도 하며 IDE와 동일하게 구문 강조 라이브러리 사용이 가능

type `nano` 즉, ``` 기호를 쓰고자 하는 언어 앞에 붙이고 다음과 같이 작성

* C 언어

```
``` c
#include <stdio.h>

int main(){

    printf("Hello World-!!");

}
```
==== **결과** ====


``` c
#include <stdio.h>

int main(){

    printf("Hello World-!!");

}
```

* javascript

```
``` javascript
    function fancyAlert(arg) {
     if(arg) {
    $.facebox({div:'#foo'})
  }
}
```
==== **결과** ====
  
  ```javascript
    function fancyAlert(arg) {
     if(arg) {
    $.facebox({div:'#foo'})
  }
}
```

---



<br>

## 8. Horizontal Rules(줄표 넣기)
* 줄표를 넣으려면 한 줄에 세 개 이상의 별표(***), 대시(---) 또는 밑줄(__) 사용


```
***
---
_________________
```

==== **결과** ====
***
---
_________________

============

<br><br>

---

## 9.  Links(링크 걸기)

* 링크 텍스트를 대괄호(예: [Twitch])로 묶은 다음 즉시 URL을 괄호 안에 삽입 <br>(예: (https://www.twitch.tv/)

```
[Twitch](https://www.twitch.tv/)
```
[Twitch](https://www.twitch.tv/)

---

<br>

* 위 방법이 귀찮거나 더 빠른 방법을 원한다면 URL 및 이메일 주소에 바로 사용하거나, 꺾쇠 사용

```
[자동 링크]
www.youtube.com/channel/UC3SyT4_WLHzN7JmHQwKQZww

[꺾쇠 링크]
<https://jieuninus.com/> <br>
<jeongmint@kakao.com>
```
[자동 링크]<br>
www.youtube.com/channel/UC3SyT4_WLHzN7JmHQwKQZww

[꺾쇠 링크]<br>
<https://jieuninus.com/> <br/>
<jeongmint@kakao.com>

---
<br>

* 링크 뒤에 괄호() 나 큰따옴표""로 문자를 삽입하면 설명(title)을 다는 것이 가능, 다음과 같이 모든 링크 형식을 정리할 수 있음

```
[1]: https://madeedam.com/
[1]: https://madeedam.com/ "New IU Fan Products"
[1]: https://madeedam.com/ 'New IU Fan Products'
[1]: https://madeedam.com/ (New IU Fan Products)
[1]: <https://madeedam.com/> "New IU Fan Products"
[1]: <https://madeedam.com/> 'New IU Fan Products'
[1]: <https://madeedam.com/> (New IU Fan Products)
(https://madeedam.com/)

```
[1]: https://madeedam.com/ 
[1]: https://madeedam.com/ "New IU Fan Products"
[1]: https://madeedam.com/ 'New IU Fan Products'
[1]: https://madeedam.com/ (New IU Fan Products)
[1]: <https://madeedam.com/> "New IU Fan Products"
[1]: <https://madeedam.com/> 'New IU Fan Products'
[1]: <https://madeedam.com/> (New IU Fan Products)
(https://madeedam.com/)

---
<br>

## 10. Images(이미지)

```
형식 : ![Image id](url)
```

* 이미지 추가는 느낌표(!)를 대체 텍스트의 대괄호 앞에 붙인 후, 경로 또는 URL을 괄호 안에 삽입(링크와 마찬가지로 괄호() 나 큰따옴표""를 통해 설명(title)을 달 수 있음)

```
![LILAC](https://user-images.githubusercontent.com/39428260/112938741-2695ad80-9165-11eb-850a-dfbe7c20fee0.jpg)
```

![LILAC](https://user-images.githubusercontent.com/39428260/112938741-2695ad80-9165-11eb-850a-dfbe7c20fee0.jpg)

* 이미지 링크를 만들기 위해서는 전체 대괄호를 만들어 뒤에 링크를 삽입

```
[![buying-albums](https://user-images.githubusercontent.com/39428260/112939323-3792ee80-9166-11eb-9df3-0e1e1a2725f7.jpg)"앨범 구매하러 가기"](http://www.hottracks.co.kr/ht/record/detail/2300186089126)
```
[![buying-albums](https://user-images.githubusercontent.com/39428260/112939323-3792ee80-9166-11eb-9df3-0e1e1a2725f7.jpg)"이미지 클릭 시 사이트 이동"](http://www.hottracks.co.kr/ht/record/detail/2300186089126)

---
<br>

## 11. Escaping Characters(탈출문자)
* 앞의 4. Emphasis에서 잠깐 언급한 바 있는데, 문법에서 사용되는 문자를 텍스트로 표현하기 위해 문자 앞에 백슬래시(\)를 추가하는 것을 말함


```
[백슬래시 사용 전]
*백슬래시를 사용하여 (*)를 탈출시켜 보자!

[백슬래시 사용 후]
\*백슬래시를 사용하여 (*)를 탈출시켜 보자!
```

[백슬래시 사용 전]
*백슬래시를 사용하여 (*)를 탈출시켜 보자!

[백슬래시 사용 후]
\*백슬래시를 사용하여 (*)를 탈출시켜 보자!

* 그 밖의 탈출문자를 사용해야 하는 문자 모음

|**Character**|**Name**|
|------|---|
|\\ |backslash 백슬래시|
|`|backtick 백틱(코드를 탈출시킬 때)|
|\*|asterisk 별표|
|\_|underscore 언더바|
|{} |curly braces 중괄호|
|[]|brackets 대괄호|
|<>|angle brackets 꺾쇠|
|()|parentheses 소괄호|
|#|pound sign 샵|
|+|plus sign 덧셈 기호|
|-|minus sign/hyphen 뺄셈 기호/하이픈|
|.|dot 온점|
|!|exclamation mark 느낌표|
|||파이프(표를 탈출시킬 때)|

<br>

---

<br>

## 12. Tables(표)
 
* 마크다운에서는 앞서 정리한 탈출문자 중 파이프 기호 ' | ' 와 하이픈 ' - '을 사용하여 표를 나타냄

```
| 동물 | 울음소리 |
| --- | --- |
| 고양이 | 야옹 |
| 닭 | 꼬꼬댁 |
```

| 동물 | 울음소리 |
| --- | --- |
| 고양이 | 야옹 |
| 닭 | 꼬꼬댁 |

<br>

* 정렬은 칼럼을 두고 싶은 방향으로 콜론 ' : ' 기호를 추가 

```
[왼쪽 정렬]
| 동물 | 울음소리 |
| :--- | :--- |
| 고양이 | 야옹 |
| 닭    | 꼬꼬댁 |
| 하마  |      |
|       | 멍멍 |

[오른쪽 정렬]
| 동물 | 울음소리 |
| ---: | ---: |
| 닭    | 꼬꼬댁 |
| 하마  |      |
|       | 멍멍 |

[가운데 정렬]
| 동물 | 울음소리 |
| :---: | :---: |
| 고양이 | 야옹 |
| 닭    | 꼬꼬댁 |
| 하마  |      |
|       | 멍멍 |
```
[왼쪽 정렬]
| 동물 | 울음소리 |
| :--- | :--- |
| 고양이 | 야옹 |
| 닭 | 꼬꼬댁 |
| 하마 |  |
| | 멍멍 |
<br>

[오른쪽 정렬]
| 동물 | 울음소리 |
| ---: | ---: |
| 고양이 | 야옹 |
| 닭 | 꼬꼬댁 |
| 하마 |  |
| | 멍멍 |
<br>

[가운데 정렬]
| 동물 | 울음소리 |
| :---: | :---: |
| 고양이 | 야옹 |
| 닭 | 꼬꼬댁 |
| 하마 |  |
| | 멍멍 |
<br>


---
<br><br>

## 13. HTML
* HTML은 마크다운에서 자주 사용되는 언어기 때문에 HTML 태그 사용이 빈번

* 사용하는 방법은 새로운 줄에세 HTML 태그(예: \<div>, \<table>, \<pre>, \<p>)를 삽입

* 주로 마크다운 문법에서 HTML을 사용하는 목적은 텍스트 색상, 이미지 너비 변경에 있음

### - HTML 로 텍스트 변경

```
[텍스트 원본 : 마크다운]

강자에게 더 세게 I love gamble

[텍스트 수정 : HTML]

<span style = " font-size:1.5em;  color: plum;">
강자에게 더 세게 I love gamble
</span>
```

[텍스트 원본 : 마크다운]

강자에게 더 세게 I love gamble

[텍스트 수정 : HTML]

<span style = " font-size:1.5em;  color: plum;">
강자에게 더 세게 I love gamble
</span>

<br><br>

### -  HTML 로 이미지 너비 변경

```
[이미지 원본 : 마크다운]

![coin](https://user-images.githubusercontent.com/39428260/112941600-d4a35680-9169-11eb-8cfc-dbbe6b4bdf81.jpg)

[이미지 수정 : HTML]

<img src="https://user-images.githubusercontent.com/39428260/112941600-d4a35680-9169-11eb-8cfc-dbbe6b4bdf81.jpg" width="20%" height="20%" alt="Markdown Logo">
</img>
```

[이미지 원본 : 마크다운]

![coin](https://user-images.githubusercontent.com/39428260/112941600-d4a35680-9169-11eb-8cfc-dbbe6b4bdf81.jpg)

[이미지 수정 : HTML]

<img src="https://user-images.githubusercontent.com/39428260/112941600-d4a35680-9169-11eb-8cfc-dbbe6b4bdf81.jpg" width="20%" height="20%" alt="Markdown Logo">
</img>

<br><br>

* 하지만 마크다운 문법에서는 허용되지 않는 RAW HTML 태그가 존재
* GFM는 태그 필터를 사용하고 HTML 출력을 렌더링할 때 다음 HTML 태그가 필터링되는데 여기서 [사용불가] 처리한 태그는 마크다운 문법에서 사용할 수 없음
  * \<title>
  * \<textarea>
  * \<style>
  * \<xmp> [사용불가]
  * \<iframe>
  * \<noembed> [사용불가]
  * \<noframes> [사용불가]
  * \<script>
  * \<plaintext> [사용불가]

여기서 사용불가 처리한 태그들은 다음과 같이 <>가 \&lt;> 처리되어 표현됨

```
<strong> <title> <style> <em>

<blockquote>
  <xmp> is disallowed.  <XMP> is also disallowed.
</blockquote>
```

```
<p><strong> &lt;title> &lt;style> <em></p>
<blockquote>
  &lt;xmp> is disallowed.  &lt;XMP> is also disallowed.
</blockquote>
```
-> 그렇기 때문에 이탤릭체로 표시되는 현상 발생

---

<br>


## 14. 기타 GFM 정리


### - SHA 참조
* Refs가 있으면 커밋을 찾기 쉬워지는데 [SHA-1 hash](https://en.wikipedia.org/wiki/SHA-1) 는 자동으로 GitHub에 커밋에 대한 링크로 변환해 줌

```
16c999e8c71134401a78d4d46435517b2271d6ac
mojombo@16c999e8c71134401a78d4d46435517b2271d6ac
mojombo/github-flavored-markdown@16c999e8c71134401a78d4d46435517b2271d6ac
```
<br>

---


<br>


### - 저장소 내에서의 이슈 참조
이슈 또는 Pull Request 요청의 모든 번호가 자동 링크로 변환

```
#1
mojombo#1
mojombo/github-flavored-markdown#1
```

<br>

---

<br>


### - 사용자 이름 태그 @mentions
* @ 기호 다음에 사용자 이름을 입력하면 그 사람에게 깃허브 상에서 알림 메시지 호출
* 조직 내에서 팀을 @mention 할 수 있음

<br>

---

<br>

### - Emoji(이모지)
* GitHub에서도 마크다운을 통해 이모티콘 사용이 가능
  ```
  "상상이 현실이 된다!"
  👐➡🦋✨
  ```
<br>

---

<br>

## GitHub repository URL

https://github.com/jeongmint/software-engineering

<br>

---

### **참조**

[Markdown Guide Basic Syntax](https://www.markdownguide.org/basic-syntax/ "마크다운 가이드")

[Markdown Guide Extended Syntax - GFM](https://github.github.com/gfm/ "마크다운 가이드")

https://guides.github.com/features/mastering-markdown/

[마크다운 위키백과 사이트](https://ko.wikipedia.org/wiki/%EB%A7%88%ED%81%AC%EB%8B%A4%EC%9A%B4 "마크다운 위키백과 사이트")
