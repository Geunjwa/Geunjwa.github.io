---
layout: post
title: "REACT - Day3"
author: "Geunjwa"
categories: sample
tags: [sample]
image: city-1.jpg
---

# REACT day3

금일의 강의는 "JSX만의 특징을 알아보자" 이다.

JSX(JavaScript Syntax Extension)은 REACT용 문법이며, HTML과 유사하지만 JAVASCRIPT라고 한다.

## 표현식

{% highlight jsx %}
const name = 'Josh Perez';
const element1 = <h1>Hello, {name}</h1>;
const element2 = {
  <h1>
    Hello, {formatName(name)}!
  </h1>
};
{% endhighlight %}

JSX 내부에 JAVASCRIPT표현식을 쓰고 싶다면, {} 중괄호 안에 넣으면 된다.
element1처럼, 변수 명을 넣을 수도 있고
element2처럼, 함수를 넣을 수도 있다.
심지어 또다른 JSX도 넣을 수 있다고 한다.

## JSX Element 특징

{% highlight jsx %}
const element = {
  <div>
    <h1>Hello!</h1>
    <h2>Good to see you here.</h2>
      <Body /> {/*<Body></Body>*/}
  </div>
  
};
{% endhighlight %}

여러개의 TAG를 사용하고 싶다면 걔들을 Tag로 묶어줘야 된다. 위의 경우 h1, h2, Body를 div로 묶어주고 있다.
HTML과 마찬가지로 Tag 하위에 Tag를 추가하여 Tag들의 레벨을 지정할 수 있다.
JSX는 항상 Tag를 열었으면 닫아야 된다. 위 코드에서 Body Tag가 참 특이하게 생겨먹었는데 저거는 열고 닫는 것을 한번에 써둔 것이다.

## REACT fragment

{% highlight jsx %}
import React from 'react';
import Hello from './Hello';
function App() {
  <>
    <Hello />
    <div>Goodbye</div>
  </>
};
export default App;
{% endhighlight %}

REACT fragment는 Tag안에 아무것도 안써둔거를 말한다. <>와 </>
다른 Tag를 묶기 위해서 보통 <div> Tag를 사용했는데, <div> Tag의 이름이 필요 없어서 저렇게 만들어 졌다고 한다. (단순히 다른 Tag를 묶는 용도라서...)

## Attribute, 주석

{% highlight jsx %}
import React from 'react';
import Hello from './Hello';
import './App.css';
function App() {
// comment in javascript
return (
<>
{/* comment in jsx */}
/* This is normal text */
<Hello />
<div className="good-bye">Goodbye</div>
</>
);
}
export default App;
{% endhighlight %}

JSX는 JavaScript이기때문에 Attribute사용시, Camal Case로 작성한다.
주석은 {/* 내용내용내용 */} 처럼 사용한다. 


## 마무리...

아무 생각 없이 REACT 강의를 수강하기 시작했는데, JavaScript를 선수로 알고 있어야 할 것 같다. JavaScript를 몰라서 낯설게 느껴지는 부분이 많다.
아무튼 오늘은 REACT의 JSX라는 문법을 배웠다. JSX는 JavaScript이며, Bebel?이라는 컴파일러인지 뭐시긴지 모르겠는데 이걸 통해서 JS형태로 변환하여 사용한다. 브라우저에 넣을때는 JavaScript랑 또 무슨 파일?만 인식할 수 있다고 하던데 이건 차차 알아가도록 하자....

베어유에서 블로그에 강의 홍보해야 된다고 해서 부랴부랴 깃허브로 블로그도 만들고 강의듣고 후기 남기느라 정신이 없었다.
그래도 항상 벼르고만 있던 개인 블로그를 개설하였다!!!! 
근데 아직 템플릿 포스트도 안내렸다 ㅋㅋㅋㅋ

  > 오늘 포스트가 마지막이 아니길 바라며... 끗!

