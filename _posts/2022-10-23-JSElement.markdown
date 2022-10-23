---
layout: post
title: JavaScript에서 HTML 요소 가져오는법
date: 2022-10-23 09:38:56 +0900
category: sample
---
``` js
<h1 id="title">Grab me!</h1>

document.getElementById("") // This will return <h1 id="title">Grab me!</h1>
```

``` js
const title = document.getElementById("");

title.innerText = "Got you";

//console.dir(title)
```

보통 id보다는 class를 사용하거나 id, class를 동시에 사용함

``` js
<h1 class="hello">Grab me!</h1>

const hellos = document.getElementByClassName("hello");

console.log(hellos) // html내의 hello클래스를 다 가져옴

```

``` js
<div class="hello">
	<h1>Grab me!</h1>
</div>

const title = document.getElementByTagName("h1") //모든 h1을 가져옴

console.log(title) //array 형태
 
```

# querySelector

element를 css방식으로 검색할 수 있다.

``` js
<div class="hello">
	<h1>Grab me!</h1>
</div>

const title = document.querySelector(".hello h1"); // hello클래스의 h1을 가져옴

console.log(title) // this will show you <h1>Grab me!</h1>
```