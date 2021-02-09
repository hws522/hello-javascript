# Study to JavaScript 
<br>
<br>

### **JavaScript**
---
JavaScript는 웹페이지를 동적으로, 프로그래밍적으로 제어하기 위해서 고안된 언어다. 그렇기 때문에 오늘날 가장 중요한 플랫폼이라고 할 수 있는 웹브라우저에서 유일하게 사용할 수 있는 프로그래밍 언어이다. 최근에는 HTML5의 적용이 가속화되면서 지금까지 모바일 환경에서 네이티브 앱(안드로이드, IOS)으로 구현해왔던 기능이 웹에서도 대부분 구현할 수 있게 되고 있다. 웹이 크로스플랫폼이라는 점, 검색 가능하다는 점, 네이티브 디바이스를 제어할 수 있는 하드브리드 시스템(phonegap 등)이 존재한다는 점에서 웹의 중요함은 더욱 확대될 전망이다. 자연스럽게 웹에서 구동되는 유일한 언어인 JavaScript의 중요함도 점점 커질 것으로 예상된다.

자바스크립트로 할 수 있는 일을 참고하면 알 수 있지만, 최근에는 자바스크립트가 웹을 벗어나서 광범위하게 사용되고 있다. 그 효용이 다각적이면서도 배우기 쉬운 점 때문에 자바스크립트는 중급 개발자나 프로그래밍 입문자 모두가 도전해볼만한 언어다.

<br>

### **역사**
---
HTML이 한번 화면에 출력된 후에는 그 형태나 동작방법을 바꿀 수 없는 문제를 해결하기 위해서 네스케이프에서 만들어졌다. 이후에 이 언어는 마이크로소프트의 인터넷 익스플로러에 jscript라는 이름으로 탑재된다. 후에 ECMA라는 표준화 기구로 이 언어의 관리 주체가 옮겨졌다.

<br>

### **실행**
---
자바스크립트는 원래 웹브라우저에서 HTML, CSS를 동적으로 제어하기 위해서 만들어진 언어다. 하지만 오늘날 자바스크립트가 웹브라우저를 벗어나서 매우 다양한 용도로 사용되고 있다. 이런 이유로 자바스크립트의 실행환경은 다양하다. 필자는 자바스크립트의 원래 목적이었고, 가장 보편적인 실행환경인 웹브라우저에서 실습을 진행할 것이다. 하지만 본 수업의 내용은 웹브라우저 뿐 아니라 node.js, 구글 크롭 웹브라우저 플러그인, 구글 스크립트, PDF, 각종 데스크탑 위젯에서 사용되는 자바스크립트에서도 적용될 수 있는 내용이다.
<br>

### **숫자와 문자**
---
자바스크립트에서는 큰따옴표나 작은따옴표가 붙지 않은 숫자는 숫자로 인식한다.

    Math.pow(3,2); // 3의 제곱
    Math.round(10.6); // 10.6을 반올림
    Math.cell(10.2); // 10.2를 올림
    Math.floor(10.6); // 10.6을 내림
    Math.sqrt(9); // 9의 제곱근
    Math.random(); // 0부터 1.0 사이의 랜덤한 숫자
    Math.round(100 * Math.random()); // 0부터 100사이의 수를 반올림한 숫자. 

문자는 "(큰 따옴표) 혹은 '(작은 따옴표) 중의 하나로 감싸야 한다. 큰 따옴표로 시작하면 큰 따옴표로 끝나야하고, 작은 따옴표로 시작하면 작은 따옴표로 끝나야 한다. String이라고 한다.

\를 ' 앞에 위치시키면 ' 를 문자열의 시작과 끝을 구분하는 구분자가 아니라 단순히 문자로 해석하도록 강제 할 수 있다. 이러한 기법을 이스케이프(escape)라고 한다.

    alert('hyunwoo'\s javascript');

여러줄을 표시하기 위해서는 아래와 같이 한다. \n는 줄바꿈을 의미하는 특수한 문자다.

    alert("hello.\njavascript!);

문자와 문자를 더할 때는 아래와 같이 한다.

    alert("coding"+" everybody"); //coding everybody

문자의 길이를 구할 때는 문자 뒤에 .length를 붙인다.

    alert("coding everybody".length); // 16

문자열에서 찾고자하는 문자의 위치를 구할 때는 .indexOf("찾고자하는문자")를 붙인다.

    alert("code".indexOf("c")); // 0

<br>

### **변수**
---
변수(Variable)는 (문자나 숫자 같은) 값을 담는 컨테이너로 값을 유지할 필요가 있을 때 사용한다. 여기에 담겨진 값은 다른 값으로 바꿀 수 있다. 변수는 마치 (사람이 쓰는 언어인) 자연어에서 대명사와 비슷한 역할을 한다.

JavaScript에서 변수는 var로 시작한다. var은 변수를 선언하겠다는 것을 의미한다. var을 생략 할수도 있지만 이것은 유효범위라는 것에 영향을 미친다. 그렇기 때문에 var의 의미를 명확하게 이해하기 전까지는 var를 사용하는 것이 권장된다. 유효범위에 대해서는 뒤에서 살펴볼 것이다. 변수의 이름은 $, _, 혹은 특수 문자를 제외한 모든 문자로 시작할 수 있다. 다음 예제는 변수에 값을 대입한 예제다.

    var a = 1;
    alert(a + 1);
    // 2

    var first = "hello";
    alert(first + " javascript");
    // hello javascript

<br>

### **비교**
---
연산자란 값에 대해서 어떤 작업을 컴퓨터에게 지시하기 위한 기호인데 우리는 이미 연산자를 사용했다. 아래 예제 중에서 '='는 우항의 값인 1을 좌항의 변수 a에 대입하는 '대입 연산자'다.

프로그래밍에서 비교란 주어진 값들이 같은지, 다른지, 큰지, 작은지를 구분하는 것을 의미한다. 이 때 비교 연산자를 사용하는데 비교 연산자의 결과는 true나 false 중의 하나다. true는 비교 결과가 참이라는 의미이고, false는 거짓이라는 뜻이다. true와 false는 블린(boolean)이라고 불리는 데이터 형식이다.

**==** 

동등 연산자로 좌항과 우항을 비교해서 서로 값이 같다면 true 다르다면 false가 된다. '='가 두개인 것을 주의하자. '='가 하나인 것은 대입 연산자로 우항의 값을 좌항의 변수에 대입할 때 사용하는 것으로 의미가 완전히 다르다.

**===** 

일치 연산자로 === 좌항과 우항이 '정확'하게 같을 때 true 다르면 false가 된다.

    alert(1 == '1'); // true
    alert(1 === '1') // false

'==='는 숫자 1과 문자 1을 다르게 인식한다. 반면에 '=='는 양쪽의 값을 같다고 판단한다. 바로 이것이 '정확'의 의미다. 즉 ===는 서로 같은 수를 표현하고 있더라도 데이터 형이 같은 경우에만 같다고 판단하기 때문이다. 결론부터 말하면 == 연산자 대신 === 연산자를 쓰는 것을 강력하게 권한다.

    alert(null == undefined);       //true
    alert(null === undefined);      //false
    alert(true == 1);               //true
    alert(true === 1);              //false
    alert(true == '1');             //true
    alert(true === '1');            //false 
    alert(0 === -0);                //true
    alert(NaN === NaN);             //false

null과 undefined는 값이 없다는 의미의 데이터 형이다. null은 값이 없음을 명시적으로 표시한 것이고, undefined는 그냥 값이 없는 상태라고 생각하자.

NaN은 0/0과 같은 연산의 결과로 만들어지는 특수한 데이터 형인데 숫자가 아니라는 뜻이다.

**!=** 

'!'는 부정을 의미한다. '같다'의 부정은 '같지 않다'이다. 이것을 기호로는 '!='로 표시한다. 아래의 결과는 !=의 결과인데 ==와 정반대의 결과를 보여준다.

    alert(1!=2);            //true
    alert(1!=1);            //false
    alert("one"!="two");    //true
    alert("one"!="one");    //false

**!==** 

'!=='는 '!='와 '=='의 관계와 같다. 정확하게 같지 않다는 의미다. 예제는 생략한다.

**>** 

좌항이 우항보다 크다면 참, 그렇지 않다면 거짓임을 알려주는 연산자다. '<'는 반대의 의미로 언급은 생략하겠다.

    alert(10>20);   //false
    alert(10>1);    //true
    alert(10>10);   //false
**>=** 

좌항이 우항보다 크거나 같다. '<='는 반대의 의미로 언급은 생략하겠다.

    alert(10>=20);      //false
    alert(10>=1);       //true
    alert(10>=10);      //true

<br>

### **Boolean**
---
'비교 수업'에서 비교 연산의 결과로 참(true)이나 거짓(false)을 얻을 수 있다고 배웠다. 여기서 참과 거짓은 '숫자와 문자 수업'에서 배운 숫자와 문자처럼 언어에서 제공하는 데이터 형이다. 이를 Boolean(불린)이라고 부르고 불린으로 올 수 있는 값은 true와 false 두가지 밖에 없다. 불린은 조건문에서 핵심적인 역할을 담당한다.

<br>

### **조건문**
---
**if** 

조건문은 if로 시작한다. if 뒤의 괄호에 조건이 오고, 조건이 될 수 있는 값는 Boolean이다. Boolean의 값이 true라면 조건이 담겨진 괄호 다음의 중괄호 구문이 실행된다.

아래 예제의 실행결과는 'result : true'다. if 뒤에 true가 왔기 때문이다.

    if(true){
        alert('result : true');
    }

다음 예제는 아무것도 출력하지 않을 것이다. if 뒤에 false가 왔기 때문이다.

    if(false){
        alert('result : true');
    }

다음 예제를 보자. 결과는 12345를 출력할 것이다.

    if(true){
        alert(1);
        alert(2);
        alert(3);
        alert(4);
    }
    alert(5);

다음 예제를 실행해보자. 결과는 5만 출력될 것이다.

    if(false){
        alert(1);
        alert(2);
        alert(3);
        alert(4);
    }
    alert(5);

왜 그럴까? if 문의 조건이 참이면 중괄호의 시작({}부터 중괄호의 끝(})까지의 구간이 실행되기 때문이다. 거짓이면 중괄호 구간이 실행되지 않기 때문에 alert(5); 구문만 실행된 것이다.

**else** 

if만으로는 좀 더 복잡한 상황을 처리하는데 부족하다. 아래 예제를 보자. 결과는 1이다.

    if(true){
        alert(1);
    } else {
        alert(2);
    }

다음 예제의 결과는 2다.

    if(false){
        alert(1);
    } else {
        alert(2);
    }

if문의 조건이 true라면 if의 중괄호 구간이 실행되고, false라면 else 이후의 중괄호 구간이 실행된다. 즉 else는 주어진 조건이 거짓일 때 실행할 구간을 정의하는 것이다.

**else if** 

else if를 이용하면 조건문을 좀 더 풍부하게 할 수 있다. 아래 예제를 보자. 결과는 2다.

    if(false){
        alert(1);
    } else if(true){
        alert(2);
    } else if(true){
        alert(3);
    } else {
        alert(4);
    }

다음 예제의 결과는 3이다.

    if(false){
        alert(1);
    } else if(false){
        alert(2);
    } else if(true){
        alert(3);
    } else {
        alert(4);
    }

다음 예제의 결과는 4다.

    if(false){
        alert(1);
    } else if(false){
        alert(2);
    } else if(false){
        alert(3);
    } else {
        alert(4);
    }

else if는 좀 더 다양한 케이스의 조건을 검사할 수 있는 기회를 제공한다. else if의 특징은 if나 else와는 다르게 여러개가 올 수 있다는 점이다. else if의 모든 조건이 false라면 else가 실행된다. else는 생략 가능하다.

앞서 배운 변수와 비교연산자 그리고 조건문을 결합해보자. ID의 값으로 hello을 입력해보고, 다른 값도 입력해보자. 아래의 예제는 브라우저에서 실행해야 한다. 다른 환경에서는 원하는데로 동작하지 않을 것이다.

    <!DOCTYPE html>
    <html>
    <head>
        <meta charset="utf-8"/>
    </head>
    <body>
        <script>
            id = prompt('아이디를 입력해주세요.')
            if(id=='hello'){
                alert('아이디가 일치 합니다.')
            } else {
                alert('아이디가 일치하지 않습니다.')
            }
        </script>
    </body>
    </html>

위의 내용에서 prompt() 구문은 사용자가 입력한 값을 가져와서 id 변수의 값으로 대입한다. 이러한 것을 API 또는 함수라고 부르는데, 이에 대한 내용은 곧 배운다. 사용자가 입력한 값이 hello이라면 '아이디가 일치 합니다'를 출력하고 그렇지 않다면 '아이디가 일치하지 않습니다'를 출력한다.

**조건문의 중첩** 

위의 예제에서 아이디와 비밀번호를 모두 검증해야 한다면 어떻게 하면 될까? 다음 예제를 보자.

    <!DOCTYPE html>
    <html>
    <head>
        <meta charset="utf-8"/>
    </head>
    <body>
        <script>
            id = prompt('아이디를 입력해주세요.');
            if(id=='hello'){
                password = prompt('비밀번호를 입력해주세요.');
                if(password==='111111'){
                    alert('인증 했습니다.');
                } else {
                    alert('인증에 실패 했습니다.');
                }
            } else {
                alert('인증에 실패 했습니다.');
            }
        </script>
    </body>
    </html>

if문 안에 다시 if문이 등장했다. 즉 사용자가 입력한 값과 아이디의 값이 일치하는지를 확인한 후에 일치한다면 비밀번호가 일치하는지 확인한 것이다. 이렇게 조건문은 조건문 안에 중첩해서 사용될 수 있다.


**&&** 

&&는 좌항과 우항이 모두 참(true)일 때 참이된다. 다음 예제를 보자. 결과는 1이다. &&의 좌우항이 모두 true인 것은 첫번째 조건문 밖에 없기 때문이다. 이러한 논리 연산자를 and 연산자라고 한다.

    if(true && true){
        alert(1);
    }
    if(true && false){
        alert(2);
    }
    if(false && true){
        alert(3);
    }
    if(false && false){
        alert(4);
    }

논리 연산자를 이용한 사례를 살펴보자. 다음 예제는 논리 연산자를 이용해서 이전 예제를 개선한 것이다.

    <!DOCTYPE html>
    <html>
    <head>
        <meta charset="utf-8"/>
    </head>
    <body>
        <script>
            id = prompt('아이디를 입력해주세요.');
            password = prompt('비밀번호를 입력해주세요.');
            if(id=='hello' && password=='111111'){
                alert('인증 했습니다.');
            } else {
                alert('인증에 실패 했습니다.');
            }
        </script>
    </body>
    </html>


중첩된 if문을 하나로 줄였다. 덕분에 코드의 복잡성도 낮아졌다. &&는 아래와 같은 의미를 만든다.

"id의 값이 hello이고 password의 값이 111111이면 참이다"

즉 && 연산자의 좌항과 우항이 모두 참일 때 전체가 참이 되는 것이다.

**||** 

'||'는 '||'의 좌우항 중에 하나라도 true라면 true가 되는 논리 연산자다. |기호는 통상 엔터키 위에 있는 원화표시 키를 쉬프트와 함께 누르면 입력된다. or 연산자라고 부른다. 다음 예를 보자. 결과는 1,2,3이 출력된다. 마지막 조건문의 '||'는 좌항과 우항이 모두 false이기 때문에 false가 된다.

    if(true || true){
        alert(1);
    }
    if(true || false){
        alert(2);
    }
    if(false || true){
        alert(3);
    }
    if(false || false){
        alert(4);
    }

다음 예제는 id 값으로 hello, javascript, study 중의 하나를 입력하면 '인증 했습니다'가 출력되고, 그 외의 값을 입력하면 '인증에 실패 했습니다.'를 출력하는 예제다.

    id = prompt('아이디를 입력해주세요.');
    if(id==='hello' || id==='javascript' || id==='study'){
        alert('인증 했습니다.');
    } else {
        alert('인증에 실패 했습니다.');
    }


위의 예제에서는 논리 연산자를 3개 사용했다. 2개만 사용하는 것이 아니라는 것을 보여주기 위한 예제다.

다음 예제는 id 값으로 hello, javascript, study 중의 하나를 사용하고 비밀번호는 111111을 입력하면 right 외의 경우에는 wrong를 출력하는 예다.


    id = prompt('아이디를 입력해주세요.');
    password = prompt('비밀번호를 입력해주세요.');
    if((id==='hello' || id==='javascript' || id==='study') && password==='111111'){
    alert('인증 했습니다.');
    } else {
        alert('인증에 실패 했습니다.');
    }

위의 예제에서는 or와 and를 혼합해서 사용하는 방법을 보여준다. id 값을 테스트 하는 구간을 괄호()로 묶었다. 사용자가 id의 값으로 hello 비밀번호를 111111을 입력했다면 연산의 순서는 아래와 같이 된다.

1. (id=="hello" or id=="javascript" or id=="study") : true가 된다.
2. password=='111111' : true가 된다.
3. true(1항) and true(2항) : true가 된다.

id 비교를 할 때 괄호를 사용한 것은 사칙 연산을 할 때 괄호부터 계산하는 것과 같은 원리다.

**!** 

'!'는 부정의 의미로, Boolean의 값을 역전시킨다. true를 false로 false를 true로 만든다. not 연산자라고 부른다. 아래의 결과는 4다.

    if(!true && !true){
        alert(1);
    }
    if(!false && !true){
        alert(2);
    }
    if(!true && !false){
        alert(3);
    }
    if(!false && !false){
        alert(4);
    }

조건문에 사용될 수 있는 데이터 형이 꼭 불린만 되는 것은 아니다. 관습적인 이유로 0는 false 0이 아닌 값은 true로 간주된다. 아래의 예제는 2를 출력한다.

    if(0){
        alert(1)
    }
    if(1){
        alert(2)
    }


다음은 false와 0 외에 false로 간주되는 데이터형의 리스트다. if문의 조건으로 !(부정) 연산자를 사용했기 때문에 각 조건문의 첫번째 블록이 실행되는 것은 주어진 값이 false이기 때문이다.

    if(!''){
        alert('빈 문자열')
    }
    if(!undefined){
        alert('undefined');
    }
    var a;
    if(!a){
        alert('값이 할당되지 않은 변수'); 
    }
    if(!null){
        alert('null');
    }
    if(!NaN){
        alert('NaN');
    }

<br>

### **반복문**
---
반복문의 문법은 몇가지가 있다. 각각의 구문은 서로 대체 가능하기 때문에 상황과 취향에 따라서 선택해서 사용하면 된다.

**While**
    
    while (조건){
        반복해서 실행할 코드
    }

document.write는 자바스크립트를 이용해서 웹페이지에 텍스트를 출력한다. 이것은 웹브라우저에서만 동작할 것이다. node.js 콘솔과 같은 환경에서 실습을 한다면 console.log와 같은 메소드를 대신 사용한다.

    while(true){
        document.write('coding everybody <br />');
    }

이번에는 true를 false로 바꾼 아래의 예제를 실행해보자. 아무런 결과도 출력하지 않을 것이다.

    while(false){
        document.write('coding everybody <br />');
    }

while문은 while문 뒤에 따라오는 괄호 안의 조건이 참(true)면 중괄호 안의 코드 구간을 반복적으로 실행한다. 조건이 false면 반복문이 실행되지 않는다. 여기서 true와 false는 종료조건이 되는데, 이 값을 변경하는 것을 통해서 반복문을 종료시킬 수 있다. 반복문에서 종료조건을 잘못 지정하면 무한반복이 되거나, 반복문이 실행되지 않는다.

아래의 반복문은 i의 값을 1씩 순차적으로 증가시킴으로서 반복의 지속 여부를 결정하고 있다.

    var i = 0;
    // 종료조건으로 i의 값이 10보다 작다면 true, 같거나 크다면 false가 된다.
    while(i < 10){
        // 반복이 실행될 때마다 coding everybody <br />이 출력된다. <br /> 줄바꿈을 의미하는 HTML 태그
        document.write('coding everybody <br />');
        // i의 값이 1씩 증가한다.
        i++
    }

**for**

```
    for(초기화; 반복조건; 반복이 될 때마다 실행되는 코드){
        반복해서 실행될 코드
    }
```
```
    for(var i = 0; i < 10; i++){
        document.write('coding everybody'+i+'<br />');
    }
```
for문은 제일 먼저 '초기화'를 한다. 위의 예제에서 초기화는 var i = 0;이다. 즉 변수 i의 값을 0으로 설정한 것이다. 그 다음에는 '반복조건'인 i < 10이 실행된다. 현재 i의 값은 0이다. 그렇기 때문에 이 조건은 참이다. 반복조건이 참이면 중괄호 안의 내용이 실행된다. i의 값이 0이기 때문에 `'coding everybody0<br />'`이라는 텍스트가 출력된다. '반복해서 실행될 코드'의 실행이 끝나면 '반복이 될 때마다 실행되는 코드'가 실행된다. i++는 현재 i의 값에 1을 더하라는 의미다. 현재 i의 값은 0이다. 따라서 i++의 결과로 i는 1이 되었다. 그리고 '반복조건'이 실행된다. 현재 i의 값은 1이기 때문에 i < 10은 참이다. 다시 '반복해서 실행될 코드'가 실행된다. 그렇게 반복해서 작업이 실행된다. 이 과정에서 i의 값은 반복 할 때마다 1씩 증가한다. 결국 i의 값이 10이 되는 순간 i < 10을 충족시키지 못하게 되고 반복문은 종료된다.

**break**

반복작업을 중간에 중단시키고 싶다면 어떻게 해야할까?  break를 사용하면 된다. 아래의 예제는 위에서 살펴본 예제를 일부 변형한 것이다.

    for(var i = 0; i < 10; i++){
        if(i === 5) {
            break;
        }
        document.write('coding everybody'+i+'<br />');
    }

종료조건에 따르면 10행이 출력돼야 하는데 5행만 출력되었다. 2행의 if(i === 5) 에 의해서 i의 값이 5일 때 break 문이 실행되면서 반복문이 완전히 종료된 것이다. 반복문 안에서 break가 실행되면 반복문을 즉시 종료시키는 것이다.

**continue**

그럼 실행을 즉시 중단 하면서 반복은 지속돼게 하려면 어떻게 해야 할까? 설명이 어렵다면 예제를 보자. 이전 예제의 break를 continue로 변경했을 뿐이지만 결과는 전혀 다르다.

    for(var i = 0; i < 10; i++){
        if(i === 5) {
            continue;
        }
        document.write('coding everybody'+i+'<br />');
    }

i의 값이 5가 되었을 때 실행이 중단 됐기 때문에 continue 이후의 구문이 실행되지 않은 것이다. 하지만 반복문은 중단되지 않았기 때문에 나머지 결과가 출력된 것이다.

**반복문 중첩**

반복문 안에는 다시 반복문이 나타날 수 있다. 다음 예제를 보자. 다음 예제는 00, 01, 02....99 까지를 화면에 출력한다.

    // 0부터 9까지 변수 i에 순차적으로 값을 할당        
    for(var i = 0; i < 10; i++){
        // 0부터 9까지의 변수를 j의 값에 순차적으로 할당
        for(var j = 0; j < 10; j++){    
            // i와 j의 값을 더한 후에 출력
            // String은 숫자인 i와 j의 데이터 타입을 문자로 형태를 변환하는 명령이다. 
            // String()을 제거하고 실행해보면 의미가 좀 더 분명하게 드러날 것이다.
            document.write(String(i)+String(j)+'<br />');
        }
    }

<br>

### **함수**
---
함수의 형식은 아래와 같다.

    function 함수명( [인자...[,인자]] ){
        코드
        return 반환값
    }

함수는 function 뒤에 함수의 이름이 오고, 소괄호가 따라온다. 소괄호에 인자라는 값이 차례로 들어오는데 이 값은 함수를 호출할 때 함수의 로직으로 전달될 변수다. 인자는 생략 할 수 있다. 함수를 호출 했을 때 실행하게 될 부분이 중괄호 안쪽에 온다.

다음 예제를 보자. 이 함수의 이름은 numbering이고, 내용은 0부터 9까지를 화면에 출력한다.

    function numbering(){
        i = 0;
        while(i < 10){
            document.write(i);
            i += 1;
        }   
    }
    numbering();
    //0123456789

함수의 핵심은 입력과 출력이다. 입력된 값을 연산해서 출력하는 것이 함수의 기본적인 역할이다. 다음은 함수에서 입력과 출력의 역할을 하는 구문들에 대한 설명이다.

**return**

함수 내에서 사용한 return은 return 뒤에 따라오는 값을 함수의 결과로 반환한다. 동시에 함수를 종료시킨다. 

    
    function get_member1(){
        return 'study';
    }
 
    function get_member2(){
        return 'javascript';
    }
 
    alert(get_member1());
    alert(get_member2());

get_member1와 get_member2를 출력(alert)한 결과가 각각 study와 javascript인 이유는 함수 내에서 문자열 study와 javascript를 return을 하기 때문이다.

return은 결과를 반환하는 것 외에 함수를 중지시키는 역할도 한다. 다음 코드를 보자. 결과는 study이다.

    function get_member(){
        return 'study';
        return 'javascript';
        return 'everyday';
    }
    alert(get_member());

javascript, everyday는 출력하지 않았다. 왜 그럴까? 그것은 return 'study'을 실행한 후에 함수가 종료되었기 때문이다. return 'javascript' 이하는 어떠한 경우도 실행되지 않는다.

**인자**

인자(argument)는 함수로 유입되는 입력 값을 의미하는데, 어떤 값을 인자로 전달하느냐에 따라서 함수가 반환하는 값이나 메소드의 동작방법을 다르게 할 수 있다. 다음 예를보자. 결과는 1,2이다.

    function get_argument(arg){
        return arg;
    }
 
    alert(get_argument(1));
    alert(get_argument(2));

5행의 get_argument(1)은 1행에서 3행 사이에 정의된 함수를 실행하는 구문이다. 5행의 1은 get_argument로 1이라는 값을 전달하겠다는 의미다. 이 때 1행에 정의된 (arg) 구문에 의해서 변수 arg의 값으로 숫자 1이 함수 안으로 전달된다. 이 변수 arg는 함수 get_argument 안에서만 유효하다.

그럼 여러개의 입력 값을 받고 싶다면 어떻게 해야할까? 다음 예제를 보자. 결과는 30과 50이다.

    function get_arguments(arg1, arg2){
        return arg1 + arg2
    }
 
    alert(get_arguments(10, 20));  
    alert(get_arguments(20, 30));

함수를 호출 할 때 전달한 인자 10과 20은 함수의 선언부(1행)의 arg1, arg2에 차례로 할당된다. 이렇게 전달된 값은 함수 내부로 전달되서 더해진 후에 반환된다.

자바스크립트는 함수를 정의하는 또 다른 방법을 제공한다. 다음 예제를 보자. 아래 방법은 함수를 정의 하는 또 다른 방법이다.

```
    var numbering = function (){
        i = 0;
        while(i < 10){
            document.write(i);
            i += 1;
        }   
    }
    numbering();
```   
```
    (function (){
        i = 0;
        while(i < 10){
            document.write(i);
            i += 1;
        }   
    })(); //익명함수. 바로 실행된다. 1회성 실행에 사용된다.
```

자바스크립트를 함수형 언어로 표현하기도 한다. 

자바스크립트는 다른언어에 비해, 함수라는 것이 이 언어에서 차지하는 위상이 매우 높다 할 수 있다.

<br>

### **배열**
---
배열(array)이란 연관된 데이터를 모아서 통으로 관리하기 위해서 사용하는 데이터 타입이다. 변수가 하나의 데이터를 저장하기 위한 것이라면 배열은 여러 개의 데이터를 하나의 변수에 저장하기 위한 것이라고 할 수 있다. 아래의 예제를 보자. 변수 name에는 문자 study가 할당되었다. 이제부터 name을 호출하면 문자 study를 사용할 수 있다.

    var name = 'study'
    alert(name);

그렇다면 여러 개의 데이터를 하나의 변수에 담아서 관리할 수 있는 방법은 없을까? 있다. 배열을 쓰면 된다. 변수 member에 회원정보를 담아보자. 대괄호([])는 배열을 만드는 기호다. 대괄호 안에 데이터를 콤마(,)로 구분해서 나열하면 배열이 된다.

    var member = ['hello', 'javascript', 'study']

하나의 변수에 3개의 데이터를 담았다. 각각의 데이터를 원소(Element)이라고 부른다. 자 그럼 이 데이터를 꺼내오려면 어떻게 해야 할까? 아래의 예제를 보자.

    var member = ['hello', 'javascript', 'study']
    alert(member[0]);
    alert(member[1]);
    alert(member[2]);

결과는 아래의 문자열을 차례로 경고창으로 출력 할 것이다.

    hello
    javascript
    study

즉 배열에 담겨있는 값을 가져올 때는 대괄호 안에 숫자를 넣는다. 이 숫자를 색인(index)라고 부르고 0부터 시작한다. 즉 첫번째 원소(hello)를 가져오려면 대괄호 안에 0을 넣어주어야 한다는 것이다. 두번째는 1, 세번째는 2를 입력한다. 이 값을 이용해서 배열에 저정된 값을 가져올 수 있다.

배열의 진가는 반복문과 결합했을 때 나타난다. 반복문으로 리스트에 담긴 정보를 하나씩 꺼내서 처리 할 수 있기 때문이다. 다음 예제를 보자

    function get_members(){
        return ['hello', 'javascript', 'study'];
    }
    members = get_members();
    // members.length는 배열에 담긴 값의 숫자를 알려준다. 
    for(i = 0; i < members.length; i++){
        // members[i].toUpperCase()는 members[i]에 담긴 문자를 대문자로 변환해준다.
        document.write(members[i].toUpperCase());   
        document.write('<br />');
    }


    //HELLO
    //JAVASCRIPT
    //STUDY

위의 예제에서 주목해야 할 것은 반복문과 배열을 결합한 부분이다. 반복문을 이용해서 배열 members의 내용을 하나씩 꺼낸 후에 이름을 대문자로 변경한 후에 출력하고 있다. 정리하면, 배열이란 연관된 정보를 하나의 그룹으로 관리하기 위해서 사용한다. 그리고 그 정보를 처리 할 때는 반복문을 이용한다.

다음은 배열의 끝에 원소를 추가하는 방법이다. push는 인자로 전달된 값을 배열(li)에 추가하는 명령이다. 배열 li의 값은 a, b, c, d, e, f가 됐다.

    var li = ['a', 'b', 'c', 'd', 'e'];
    li.push('f');
    alert(li);

다음은 복수의 원소를 배열에 추가하는 방법이다. concat은 인자로 전달된 값을 추가하는 명령이다.

    var li = ['a', 'b', 'c', 'd', 'e'];
    li = li.concat(['f', 'g']);
    alert(li);

다음은 배열의 시작점에 원소를 추가하는 방법이다. 배열 li는 z, a, b, c, d, e가 됐다. unshift는 인자로 전달한 값을 배열의 첫번째 원소로 추가하고 배열의 기존 값들의 색인을 1씩 증가시킨다.

    var li = ['a', 'b', 'c', 'd', 'e'];
    li.unshift('z');
    alert(li);

만약 두번째 인덱스 뒤에 대문자 B를 넣고 싶다면 아래와 같이한다. splice는 첫번째 인자에 해당하는 원소부터 두번째 인자에 해당하는 원소의 숫자만큼의 값을 배열로부터 제거한 후에 리턴한다. 그리고 세번째 인자부터 전달된 인자들을 첫번째 인자의 원소 뒤에 추가한다.

    var li = ['a', 'b', 'c', 'd', 'e'];
    li.splice(2, 0, 'B');
    alert(li);

다음은 배열의 첫번째 원소를 제거하는 방법이다. shift를 사용하면 된다. 아래 결과는 b, c, d, e 다.

    var li = ['a', 'b', 'c', 'd', 'e'];
    li.shift();
    alert(li);

다음은 배열 끝점의 원소를 배열 li에서 제거한다. 이때는 pop를 사용한다. 결과는 a, b, c, d 다.

    var li = ['a', 'b', 'c', 'd', 'e'];
    li.pop();
    alert(li);

다음은 정렬하는 방법이다. 결과는 a, b, c, d, e 다.

    var li = ['c', 'e', 'a', 'b', 'd'];
    li.sort();
    alert(li);

역순으로 정렬하고 싶을 때는 아래와 같이 한다.

    var li = ['c', 'e', 'a', 'b', 'd'];
    li.reverse();
    alert(li);

<br>

### **객체**
---

지금까지 살펴본 배열은 아이템에 대한 식별자로 숫자를 사용했다. 데이터가 추가되면 배열 전체에서 중복되지 않는 인덱스가 자동으로 만들어져서 추가된 데이터에 대한 식별자가 된다. 이 인덱스를 이용해서 데이터를 가져오게 되는 것이다. 만약 인덱스로 문자를 사용하고 싶다면 객체(dictionary)를 사용해야 한다. 다른 언어에서는 연관배열(associative array) 또는 맵(map), 딕셔너리(Dictionary)라는 데이터 타입이 객체에 해당한다.


다음은 객체를 만드는 법이다.

    var grades = {'hello': 10, 'javascript': 6, 'study': 80};

위의 예제에서 hello은 key가 되고, 10은 value가 된다. 아래는 객체를 만드는 다른 방법이다.

    var grades = {};
    grades['hello'] = 10;
    grades['javascript'] = 6;
    grades['study'] = 80;

아래와 같은 방법으로 객체를 만들수도 있다.

    var grades = new Object();
    grades['hello'] = 10;
    grades['javascript'] = 6;
    grades['study'] = 80;

객체를 만들었으니 이제는 객체에서 필요한 값을 가져와보자. 다음은 study라는 이름(key)으로 저장된 값을 가져오는 법이다. 결과는 80이다.

    var grades = {'hello': 10, 'javascript': 6, 'study': 80};
    alert(grades['study']);

다음 방법으로도 객체의 속성에 접근 할 수 있다.

    alert(grades.study);

다음은 객체에 저장된 데이터를 기준으로 반복작업을 하는 방법이다.

    var grades = {'hello': 10, 'javascript': 6, 'study': 80};
    for(key in grades) {
        document.write("key : " +key+ " value : " +grades[key]+ "<br />");
    }

결과는 아래와 같다.

    key : hello value : 10
    key : javascript value : 6
    key : study value : 80

for 문은 in 뒤에 따라오는 배열의 key 값을 in 앞의 변수 name에 담아서 반복문을 실행한다. 반복문이 실행될 때 변수 key의 값으로 hello, javascript, study가 순차적으로 할당되기 때문에 grades[key]를 통해서 객체의 값을 알아낼 수 있다.

객체에는 객체를 담을수도 있고, 함수도 담을 수 있다. 

    var grades = {
        'list': {'hello': 10, 'javascript': 6, 'study': 80},
        'show' : function(){
            for(var name in this.list){
                document.write(name+':'+this.list[name]+"<br />");
            }
        }
    };
    grades.show();

이것은 자바스크립트를 이용한 객체 지향 프로그래밍 기법의 핵심이 되는 성질로 취지에 따라서 로직을 객체에 그룹핑해서 객체라는 부품을 조립해서 소프트웨어라는 완제품을 만들 수 있게 해준다. 객체 지향에 대해서는 뒤에서 자세히 살펴본다.

<br>

### **모듈**
---

순수한 자바스크립트에서는 모듈(module)이라는 개념이 분명하게 존재하지는 않는다. 하지만 자바스크립트가 구동되는 호스트 환경에 따라서 서로 다른 모듈화 방법이 제공되고 있다. 이 수업에서는 자바스크립트의 대표적인 호스트 환경인 웹브라우저에서 로직을 모듈화하는 방법에 대해서 알아볼 것이다.

    <!DOCTYPE html>
    <html>
    <head>
        <meta charset="utf-8"/>
    </head>
    <body>
        <script>
            function welcome(){
                return 'Hello world'
            }
            alert(welcome());
        </script>
    </body>
    </html>

위의 코드는 아무런 문제가 없다. 하지만 welcome 함수가 자주 사용되는 것이라고 가정해보자. 이런 경우 이것이 필요할 때마다 이 함수를 정의해서 사용하는 것은 유지보수도 어렵고 낭비가 될 것이다. 이럴 때 모듈이 필요하다. 함수 welcome을 모듈로 만들어보자.

새로운 파일을 만든다. 이름은 greeting.js 다. 자바스크립트 파일은 확장자로 js를 사용한다.

**greeting.js**

    function welcome(){
        return 'Hello world';
    }

**main.html**

    <!DOCTYPE html>
    <html>
    <head>
        <meta charset="utf-8"/>
        <script src="greeting.js"></script>
    </head>
    <body>
        <script>
            alert(welcome());
        </script>
    </body>
    </html>

이전 예제와 비교했을 때 결과는 같다. 하지만 함수 welcome을 main.html의 외부 파일로 분리했다. 다음은 위의 코드에 대한 분석이다.

**`<script src="greeting.js"></script>`**

JavaScript와 HTML은 완전히 다른 문법을 가진 언어다. 그런데 HTML 문서 안에는 JavaScript와 HTML이 동시에 표현된다. 따라서 브라우저에게 어디서부터 어디까지가 JavaScript이고, HTML인지를 구분해서 알려줘야 한다. 이 역할을 하는 HTML 태그가 script 태그다. script 태그 안쪽에 위치하는 컨텐츠는 브라우저에 의해서 JavaScript로 인식된다. 그런데 위의 코드는 컨텐츠 대신에 src 속성이 있다. 브라우저는 src 속성에 있는 파일을 다운로드해서 실행시킨다. greeting.js에는 함수 welcome가 정의되어 있기 때문에 main.html 안에 이 함수가 정의 되어 있지 않음에도 실행할 수 있는 것이다.

<br>

모듈을 로드하는 방법은 호스트 환경에 따라서 달라진다. Node.js에서는 아래와 같은 방법으로 모듈을 로드한다.

**node.circle.js (로드될 대상)**

    var PI = Math.PI;
  
    exports.area = function (r) {
    return PI * r * r;
    };
  
    exports.circumference = function (r) {
    return 2 * PI * r;
    };

**node.demo.js (로드의 주체)**

    var circle = require('./node.circle.js');
    console.log( 'The area of a circle of radius 4 is '
               + circle.area(4));

아래는 실행방법과 실행 결과다.

    F:\BitNami\wampstack-5.4.22-0\apache2\htdocs\javascript\module>node node.demo.js
    The area of a circle of radius 4 is 50.26548245743669

**라이브러리**

라이브러리는 모듈과 비슷한 개념이다. 모듈이 프로그램을 구성하는 작은 부품으로서의 로직을 의미한다면 라이브러리는 자주 사용되는 로직을 재사용하기 편리하도록 잘 정리한 일련의 코드들의 집합을 의미한다고 할 수 있다. 프로그래밍의 세계에는 휼룡한 라이브러리가 많다. 좋은 라이브러리를 선택하고 잘 사용하는 것은 프로그래밍의 핵심이라고 할 수 있다. 

아래 예제는 유명 라이브러리인 jQuery를 사용하는 방법이다. 

jQuery 홈페이지에서 파일을 다운로드 받는다. 

http://jquery.com/

jQuery 메뉴얼을 이용해서 사용법을 파악한다.

http://api.jquery.com/

아래는 jQuery를 이용한 예제이다.

    <!DOCTYPE html>
    <html>
    <head>
        <script src="https://code.jquery.com/jquery-1.11.0.min.js"></script>
    </head>
    <body>
        <ul id="list">
            <li>empty</li>
            <li>empty</li>
            <li>empty</li>
            <li>empty</li>
        </ul>
        <input id="execute_btn" type="button" value="execute" />
        <script type="text/javascript">
        $('#execute_btn').click(function(){
            $('#list li').text('coding everybody');
        })
        </script>
    </body>
    </html>

다음은 jQuery를 이용하지 않고 동일한 기능을 구현한 예제이다.

    <!DOCTYPE html>
    <html>
    <body>
        <ul id="list">
            <li>empty</li>
            <li>empty</li>
            <li>empty</li>
            <li>empty</li>
        </ul>
        <input id="execute_btn" type="button" value="execute" />
        <script type="text/javascript">
        function addEvent(target, eventType,eventHandler, useCapture) {
            if (target.addEventListener) { // W3C DOM
                target.addEventListener(eventType,eventHandler,useCapture?useCapture:false);
            } else if (target.attachEvent) {  // IE DOM
                var r = target.attachEvent("on"+eventType, eventHandler);
            }
        }
        function clickHandler(event) {
            var nav = document.getElementById('list');
            for(var i = 0; i < nav.childNodes.length; i++) {
                var child = nav.childNodes[i];
                if(child.nodeType==3)
                    continue;
                child.innerText = 'Coding everybody';
            }
        }
        addEvent(document.getElementById('execute_btn'), 'click', clickHandler);
        </script>
    </body>
    </html>

<br>

### **정규표현식**
---

정규표현식(regular expression)은 문자열에서 특정한 문자를 찾아내는 도구다. 이 도구를 이용하면 수십줄이 필요한 작업을 한줄로 끝낼 수 있다. 

정규표현식은 하나의 언어라고 할 수 있다. 

정규표현식은 두가지 단계로 이루어진다. 하나는 컴파일(compile) 다른 하나는 실행(execution)이다. 우선 컴파일부터 알아보자.

컴파일은 검출하고자 하는 패턴을 만드는 일이다. 우선 정규표현식 객체를 만들어야 한다. 객체를 만드는 방법은 두가지가 있다. a라는 텍스트를 찾아내는 정규표현식을 만들어보자.


```
    var pattern = /a/
```
```
    var pattern = new RegExp('a');
```

정규표현식을 컴파일해서 객체를 만들었다면 이제 문자열에서 원하는 문자를 찾아내야 한다. 

**RegExp.exec()**

    console.log(pattern.exec('abcdef')); // ["a"]

실행결과는 문자열 a를 값으로 하는 배열을 리턴한다.

    console.log(pattern.exec('bcdefg')); // null

인자 'bcdefg'에는 a가 없기 때문에 null을 리턴한다.

**RegExp.test()**         

test는 인자안에 패턴에 해당되는 문자열이 있으면 true, 없으면 false를 리턴한다.

    console.log(pattern.test('abcdef')); // true
    console.log(pattern.test('bcdefg')); // false


문자열 객체의 몇몇 메소드는 정규표현식을 사용할 수 있다. 

**String.match()**

    console.log('abcdef'.match(pattern)); // ["a"]
    console.log('bcdefg'.match(pattern)); // null

**String.replace()**

문자열에서 패턴을 검색해서 이를 변경한 후에 변경된 값을 리턴한다.

    console.log('abcdef'.replace(pattern, 'A')); // Abcdef


정규표현식 패턴을 만들 때 옵션을 설정할 수 있다. 옵션에 따라서 검출되는 데이터가 달라진다.

**i**

i를 붙이면 대소문자를 구분하지 않는다.

    var xi = /a/;
    console.log("Abcde".match(xi)); // null
    var oi = /a/i;
    console.log("Abcde".match(oi)); // ["A"];

**g**

g를 붙이면 검색된 모든 결과를 리턴한다.

    var xg = /a/;
    console.log("abcdea".match(xg)); // ["a"]
    var og = /a/g;
    console.log("abcdea".match(og)); // ["a", "a"]

i 와 g 를 동시에 쓸 수도 있다.

    var ig = /a/ig;
    console.log("AbcabcAbcabc".match(ig)) // ["A", "a", "A", "a"]

**캡처**

괄호안의 패턴은 마치 변수처럼 재사용할 수 있다. 이 때 기호 $를 사용하는데 아래 코드는 coding과 everybody의 순서를 역전시킨다.

    var pattern = /(\w+)\s(\w+)/;
    var str = "coding everybody";
    var result = str.replace(pattern, "$2, $1");
    console.log(result); // everybody, coding


**치환**

아래 코드는 본문 중의 URL을 링크 html 태그로 교체한다.

    var urlPattern = /\b(?:https?):\/\/[a-z0-9-+&@#\/%?=~_|!:,.;]*/gim;
    var content = '생활코딩 : http://opentutorials.org/course/1 입니다. 네이버 : http://naver.com 입니다. ';
    var result = content.replace(urlPattern, function(url){
        return '<a href="'+url+'">'+url+'</a>';
    });
    console.log(result);



    // 생활코딩 : <a href="http://opentutorials.org/course/1">http://opentutorials.org/course/1</a> 입니다. 네이버 : <a href="http://naver.com">http://naver.com</a> 입니다.

<br>

### **함수지향**

<br>

### **유효범위**
---


유효범위(Scope)는 변수의 수명을 의미한다. 아래의 예제를 보자. 결과는 global이다.

```
var vscope = 'global';
function fscope(){
    alert(vscope);
}
fscope();
```

함수 밖에서 변수를 선언하면 그 변수는 전역변수가 된다. 전역변수는 에플리케이션 전역에서 접근이 가능한 변수다. 다시 말해서 어떤 함수 안에서도 그 변수에 접근 할 수 있다. 그렇기 때문에 함수 fscope 내에서 vscope를 호출 했을 때 함수 밖에서 선언된 vscope의 값 global이 반환된 것이다. 아래 예제를 보자. 결과는 '함수안 local'과 '함수밖 global'이 출력된다.

```
var vscope = 'global';
function fscope(){
    var vscope = 'local';
    alert('함수안 '+vscope);
}
fscope();
alert('함수밖 '+vscope);
```

즉 함수 안에서 변수 vscope을 조회(4행) 했을 때 함수 내에서 선언한 지역변수 vscope(3행)의 값인 local이 사용되었다. 하지만 함수 밖에서 vscope를 호출(7행) 했을 때는 전역변수 vscope(1행)의 값인 global이 사용된 것이다. 즉 지역변수의 유효범위는 함수 안이고, 전역변수의 유효범위는 에플리케이션 전역인데, 같은 이름의 지역변수와 전역변수가 동시에 정의되어 있다면 지역변수가 우선한다는 것을 알 수 있다. 아래 예제를 보자. 결과는 모두 local이다.

```
var vscope = 'global';
function fscope(){
    vscope = 'local';
    alert('함수안'+vscope);
}
fscope();
alert('함수밖'+vscope);
```

함수밖에서도 vscope의 값이 local인 이유는 무엇일까? 그것은 함수 fscope의 지역변수를 선언할 때 var를 사용하지 않았기 때문이다. var를 사용하지 않은 지역변수는 전역변수가 된다. 따라서 3행은 전역변수의 값을 local로 변경하게 된 것이다. var을 쓰는 것과 쓰지 않는 것의 차이를 이해해야 한다.

전역변수는 사용하지 않는 것이 좋다. 여러가지 이유로 그 값이 변경될 수 있기 때문이다. 함수 안에서 전역변수를 사용하고 있는데, 누군가에 의해서 전역변수의 값이 달라졌다면 어떻게 될까? 함수의 동작도 달라지게 된다. 이것은 버그의 원인이 된다. 또한 함수를 다른 에플리케이션에 이식하는데도 어려움을 초래한다. 함수의 핵심은 로직의 재활용이라는 점을 상기하자. 변수를 선언할 때는 꼭 var을 붙이는 것을 습관화해야 한다. 전역변수를 사용해야 하는 경우라면 그것을 사용하는 이유를 명확히 알고 있을 때 사용하도록 하자.

아래 두개의 예제는 변수 i를 지역변수로 사용했을 때와 전역변수로 사용했을 때의 차이점을 보여준다. 전역변수는 각기 다른 로직에서 사용하는 같은 이름의 변수값을 변경시켜서 의도하지 않은 문제를 발생시킨다.

```
function a (){
    var i = 0;
}
for(var i = 0; i < 5; i++){
    a();
    document.write(i);
}

// 01234
```
```
function a (){
    i = 0;
}
for(i = 0; i < 5; i++){
    a();
    document.write(i);
}

// 무한반복
```

불가피하게 전역변수를 사용해야 하는 경우는 하나의 객체를 전역변수로 만들고 객체의 속성으로 변수를 관리하는 방법을 사용한다.

```
var MYAPP = {}
MYAPP.calculator = {
    'left' : null,
    'right' : null
}
MYAPP.coordinate = {
    'left' : null,
    'right' : null
}
 
MYAPP.calculator.left = 10;
MYAPP.calculator.right = 20;
function sum(){
    return MYAPP.calculator.left + MYAPP.calculator.right;
}
document.write(sum());
```

전역변수를 사용하고 싶지 않다면 아래와 같이 익명함수를 호출함으로서 이러한 목적을 달성할 수 있다.

```
(function(){
    var MYAPP = {}
    MYAPP.calculator = {
        'left' : null,
        'right' : null
    }
    MYAPP.coordinate = {
        'left' : null,
        'right' : null
    }
    MYAPP.calculator.left = 10;
    MYAPP.calculator.right = 20;
    function sum(){
        return MYAPP.calculator.left + MYAPP.calculator.right;
    }
    document.write(sum());
}())
```
위와 같은 방법은 자바스크립트에서 로직을 모듈화하는 일반적인 방법이다. 

자바스크립트는 함수에 대한 유효범위만을 제공한다. 많은 언어들이 블록(대체로 {,})에 대한 유효범위를 제공하는 것과 다른 점이다. 아래 예제의 결과는 coding everybody이다.

```
for(var i = 0; i < 1; i++){
    var name = 'coding everybody';
}
alert(name);
```

자바에서는 아래의 코드는 허용되지 않는다. name은 지역변수로 for 문 안에서 선언 되었는데 이를 for문 밖에서 호출하고 있기 때문이다.

```
for(int i = 0; i < 10; i++){
    String name = "js";
}
System.out.println(name);
```
자바스크립트의 지역변수는 함수에서만 유효하다.

자바스크립트는 함수가 선언된 시점에서의 유효범위를 갖는다. 이러한 유효범위의 방식을 정적 유효범위(static scoping), 혹은 렉시컬(lexical scoping)이라고 한다. 

```
var i = 5;
 
function a(){
    var i = 10;
    b();
}
 
function b(){
    document.write(i);
}
 
a();

// 5
```

<br>

### **값으로서의 함수**
---


JavaScript에서는 함수도 객체다. 다시 말해서 일종의 값이다. 거의 모든 언어가 함수를 가지고 있다. JavaScript의 함수가 다른 언어의 함수와 다른 점은 함수가 값이 될 수 있다는 점이다. 다음 예제를 통해서 그 의미를 알아보자.

    function a(){}

위의 예제에서 함수 a는 변수 a에 담겨진 값이다. 
    
    var a = function(){}

또한 함수는 객체의 값으로 포함될 수 있다. 이렇게 객체의 속성 값으로 담겨진 함수를 메소드(method)라고 부른다.

```
a = {
    b:function(){
    }
};
```

함수는 값이기 때문에 다른 함수의 인자로 전달 될수도 있다. 아래 예제를 보자.

```
function cal(func, num){
    return func(num)
}
function increase(num){
    return num+1
}
function decrease(num){
    return num-1
}
alert(cal(increase, 1));
alert(cal(decrease, 1));
```

10행을 실행하면 함수 increase와 값 1이 함수 cal의 인자로 전달된다. 함수 cal은 첫번째 인자로 전달된 increase를 실행하는데 이 때 두번째 인자의 값이 1을 인자로 전달한다. 함수 increase은 계산된 결과를 리턴하고 cal은 다시 그 값을 리턴한다.

함수는 함수의 리턴 값으로도 사용할 수 있다.

```
function cal(mode){
    var funcs = {
        'plus' : function(left, right){return left + right},
        'minus' : function(left, right){return left - right}
    }
    return funcs[mode];
}
alert(cal('plus')(2,1));
alert(cal('minus')(2,1));   
```
당연히 배열의 값으로도 사용할 수 있다.

```
var process = [
    function(input){ return input + 10;},
    function(input){ return input * input;},
    function(input){ return input / 2;}
];
var input = 1;
for(var i = 0; i < process.length; i++){
    input = process[i](input);
}
alert(input);

// 60.5
```
<br>

### **콜백**
---
**처리의 위임**

값으로 사용될 수 있는 특성을 이용하면 함수의 인자로 함수로 전달할 수 있다. 값으로 전달된 함수는 호출될 수 있기 때문에 이를 이용하면 함수의 동작을 완전히 바꿀 수 있다. 인자로 전달된 함수 sortNumber의 구현에 따라서 sort의 동작방법이 완전히 바뀌게 된다.

```
function sortNumber(a,b){ // 콜백함수.
    // 위의 예제와 비교해서 a와 b의 순서를 바꾸면 정렬순서가 반대가 된다.
    return b-a;
}
var numbers = [20,1,9,7,6,8,5,4,3,2,10];
alert(numbers.sort(sortNumber)); // array, [20,10,9,8,7,6,5,4,3,2,1]
```
**비동기 처리**

콜백은 비동기처리에서도 유용하게 사용된다. 시간이 오래걸리는 작업이 있을 때 이 작업이 완료된 후에 처리해야 할 일을 콜백으로 지정하면 해당 작업이 끝났을 때 미리 등록한 작업을 실행하도록 할 수 있다.

<br>

### **클로저**
---
클로저(closure)는 내부함수가 외부함수의 맥락(context)에 접근할 수 있는 것을 가르킨다. 클로저는 자바스크립트를 이용한 고난이도의 테크닉을 구사하는데 필수적인 개념으로 활용된다.

**내부함수**

자바스크립트는 함수 안에서 또 다른 함수를 선언할 수 있다. 아래의 예제를 보자. 결과는 경고창에 coding everybody가 출력될 것이다.

```
function outter(){
    function inner(){
        var title = 'coding everybody'; 
        alert(title);
    }
    inner();
}
outter();
```
위의 예제에서 함수 outter의 내부에는 함수 inner가 정의 되어 있다. 함수 inner를 내부 함수라고 한다.

내부함수는 외부함수의 지역변수에 접근할 수 있다. 아래의 예제를 보자. 결과는 coding everybody이다.

```
function outter(){
    var title = 'coding everybody';  
    function inner(){        
        alert(title);
    }
    inner();
}
outter();
```

위의 예제는 내부함수 inner에서 title을 호출(4행)했을 때 외부함수인 outter의 지역변수에 접근할 수 있음을 보여준다.

**클로저**

클로저(closure)는 내부함수와 밀접한 관계를 가지고 있는 주제다. 내부함수는 외부함수의 지역변수에 접근 할 수 있는데 외부함수의 실행이 끝나서 외부함수가 소멸된 이후에도 내부함수가 외부함수의 변수에 접근 할 수 있다. 이러한 메커니즘을 클로저라고 한다. 아래 예제는 이전의 예제를 조금 변형한 것이다. 결과는 경고창으로 coding everybody를 출력할 것이다.

```
function outter(){
    var title = 'coding everybody';  
    return function(){        
        alert(title);
    }
}
var inner = outter();
inner();
```

예제의 실행순서를 주의깊게 살펴보자. 7행에서 함수 outter를 호출하고 있다. 그 결과가 변수 inner에 담긴다. 그 결과는 이름이 없는 함수다. 실행이 8행으로 넘어오면 outter 함수는 실행이 끝났기 때문에 이 함수의 지역변수는 소멸되는 것이 자연스럽다. 하지만 8행에서 함수 inner를 실행했을 때 coding everybody가 출력된 것은 외부함수의 지역변수 title이 소멸되지 않았다는 것을 의미한다. 클로저란 내부함수가 외부함수의 지역변수에 접근 할 수 있고, 외부함수는 외부함수의 지역변수를 사용하는 내부함수가 소멸될 때까지 소멸되지 않는 특성을 의미한다.


조금 더 복잡한 아래 예제를 살펴보자. 아래 예제는 클로저를 이용해서 영화의 제목을 저장하고 있는 객체를 정의하고 있다. 실행결과는 Ghost in the shell -> Matrix -> 공각기동대 -> Matrix 이다.

```
function factory_movie(title){
    return {
        get_title : function (){
            return title;
        },
        set_title : function(_title){
            title = _title
        }
    }
}
ghost = factory_movie('Ghost in the shell');
matrix = factory_movie('Matrix');
 
alert(ghost.get_title()); // Ghost in the shell
alert(matrix.get_title()); // Matrix
 
ghost.set_title('공각기동대'); // Ghost in the shell -->> 공각기동대
 
alert(ghost.get_title()); // 공각기동대
alert(matrix.get_title()); // Matrix
```

위의 예제를 통해서 알 수 있는 것들을 정리해보면 아래와 같다.

1. 클로저는 객체의 메소드에서도 사용할 수 있다. 위의 예제는 함수의 리턴값으로 객체를 반환하고 있다. 이 객체는 메소드 get_title과 set_title을 가지고 있다. 이 메소드들은 외부함수인 factory_movie의 인자값으로 전달된 지역변수 title을 사용하고 있다.

2. 동일한 외부함수 안에서 만들어진 내부함수나 메소드는 외부함수의 지역변수를 공유한다. 17행에서 실행된 set_title은 외부함수 factory_movie의 지역변수 title의 값을 '공각기동대'로 변경했다. 19행에서 ghost.get_title();의 값이 '공각기동대'인 것은 set_title와 get_title 함수가 title의 값을 공유하고 있다는 의미다.

3. 그런데 똑같은 외부함수 factory_movie를 공유하고 있는 ghost와 matrix의 get_title의 결과는 서로 각각 다르다. 그것은 외부함수가 실행될 때마다 새로운 지역변수를 포함하는 클로저가 생성되기 때문에 ghost와 matrix는 서로 완전히 독립된 객체가 된다.

4. factory_movie의 지역변수 title은 2행에서 정의된 객체의 메소드에서만 접근 할 수 있는 값이다. 이 말은 title의 값을 읽고 수정 할 수 있는 것은 factory_movie 메소드를 통해서 만들어진 객체 뿐이라는 의미다. JavaScript는 기본적으로 Private한 속성을 지원하지 않는데, 클로저의 이러한 특성을 이용해서 Private한 속성을 사용할 수 있게된다.

`참고 Private 속성은 객체의 외부에서는 접근 할 수 없는 외부에 감춰진 속성이나 메소드를 의미한다. 이를 통해서 객체의 내부에서만 사용해야 하는 값이 노출됨으로서 생길 수 있는 오류를 줄일 수 있다. 자바와 같은 언어에서는 이러한 특성을 언어 문법 차원에서 지원하고 있다.`

아래의 예제는 클로저와 관련해서 자주 언급되는 예제다. 

```
var arr = []
for(var i = 0; i < 5; i++){
    arr[i] = function(){
        return i;
    }
}
for(var index in arr) {
    console.log(arr[index]());
}
```

함수가 함수 외부의 컨텍스트에 접근할 수 있을 것으로 기대하겠지만 위의 결과는 아래와 같다.

```
5
5
5
5
5
```
위의 코드는 아래와 같이 변경해야 한다.

```
var arr = []
for(var i = 0; i < 5; i++){
    arr[i] = function(id) {
        return function(){
            return id;
        }
    }(i);
}
for(var index in arr) {
    console.log(arr[index]());
}
```
결과는 아래와 같다.

```
0
1
2
3
4
```

<br>

### **arguments**
---

함수에는 arguments라는 변수에 담긴 숨겨진 유사 배열이 있다. 이 배열에는 함수를 호출할 때 입력한 인자가 담겨있다. 아래 예제를 보자. 결과는 10이다.

```
function sum(){
    var i, _sum = 0;    
    for(i = 0; i < arguments.length; i++){
        document.write(i+' : '+arguments[i]+'<br />');
        _sum += arguments[i];
    }   
    return _sum;
}
document.write('result : ' + sum(1,2,3,4));

// 0 : 1
// 1 : 2
// 2 : 3
// 3 : 4
// result : 10
```

함수 sum은 인자로 전달된 값을 모두 더해서 리턴하는 함수다. 그런데 1행처럼 함수 sum은 인자에 대한 정의하가 없다. 하지만 마지막 라인에서는 4개의 인자를 함수 sum으로 전달하고 있다. 함수의 정의부분에서 인자에 대한 구현이 없음에도 인자를 전달 할 수 있는 것은 왜 그럴까? 그것은 arguments라는 특수한 배열이 있기 때문이다.

arguments는 함수안에서 사용할 수 있도록 그 이름이나 특성이 약속되어 있는 일종의 배열이다. arguments[0]은 함수로 전달된 첫번째 인자를 알아낼 수 있다. 또 arguments.length를 이용해서 함수로 전달된 인자의 개수를 알아낼 수도 있다. 이러한 특성에 반복문을 결합하면 함수로 전달된 인자의 값을 순차적으로 가져올 수 있다. 그 값을 더해서 리턴하면 인자로 전달된 값에 대한 총합을 구하는 함수를 만들 수 있다.

`arguments는 사실 배열은 아니다. 실제로는 arguments 객체의 인스턴스다.`

매개변수와 관련된 두가지 수가 있다. 하나는 함수.length, 다른 하나는 arguments.length이다. arguments.length는 함수로 전달된 실제 인자의 수를 의미하고, 함수.length는 함수에 정의된 인자의 수를 의미한다. 아래의 코드를 보자.

```
function zero(){
    console.log(
        'zero.length', zero.length,
        'arguments', arguments.length
    );
}
function one(arg1){
    console.log(
        'one.length', one.length,
        'arguments', arguments.length
    );
}
function two(arg1, arg2){
    console.log(
        'two.length', two.length,
        'arguments', arguments.length
    );
}
zero(); // zero.length 0 arguments 0 
one('val1', 'val2');  // one.length 1 arguments 2 
two('val1');  // two.length 2 arguments 1
```

경우에 따라 사용하고있는 함수의 인자와 정의된 매개변수의 수가 일치해야 하는 경우가 있다. 그때 함수.length와 arguments.length를 비교해서 의도하는 것과 다르게 함수를 사용한 경우라면 에러를 발생시키거나 경고를 띄움으로써 유용하게 사용될 수 있다.

<br>

### **함수호출**
---
함수에 대한 기본 수업에서 함수를 호출하는 방법을 알아봤다. 아래는 함수를 호출하는 가장 기본적인 방법이다.

```
function func(){
}
func();
```

JavaScript는 함수를 호출하는 특별한 방법을 제공한다. 본 토픽의 시작에서 함수를 객체라고 했다. 위의 예제에서 함수 func는 Function이라는 객체의 인스턴스다. 따라서 func는 객체 Function이 가지고 있는 메소드들을 상속하고 있다. 지금 이야기하려는 메소드는 Function.apply과 Function.call이다. 이 메소드들을 이용해서 함수를 호출해보자. 결과는 3이다.

```
function sum(arg1, arg2){
    return arg1+arg2;
}
alert(sum.apply(null, [1,2]))
```

함수 sum은 Function 객체의 인스턴스다. 그렇기 때문에 객체 Function 의 메소드 apply를 호출 할 수 있다. apply 메소드는 두개의 인자를 가질 수 있는데, 첫번째 인자는 함수(sum)가 실행될 맥락이다. 맥락의 의미는 다음 예제를 통해서 살펴보자. 두번째 인자는 배열인데, 이 배열의 담겨있는 원소가 함수(sum)의 인자로 순차적으로 대입된다. Function.call은 사용법이 거의 비슷하다. 여기서는 언급하지 않는다.

좀 더 흥미로운 예제를 살펴보자. 결과는 6과 185이다.

```
o1 = {val1:1, val2:2, val3:3}
o2 = {v1:10, v2:50, v3:100, v4:25}
function sum(){
    var _sum = 0;
    for(name in this){
        _sum += this[name];
    }
    return _sum;
}
alert(sum.apply(o1)) // 6
alert(sum.apply(o2)) // 185
```

예제가 복잡해보이지만 하나씩 분해해서 생각해보면 어렵지 않다.

우선 두개의 객체를 만들었다. o1는 3개의 속성을 가지고 있다. 각각의 이름은 val1, val2,val3이다. o2는 4개의 속성을 가지고 있고 o1과는 다른 속성 이름을 가지고 있고 속성의 수도 다르다.

그 다음엔 함수 sum을 만들었다. 이 함수는 객체의 속성을 열거할 때 사용하는 for in 문을 이용해서 객체 자신(this)의 값을 열거한 후에 각 속성의 값을 지역변수 _sum에 저장한 후에 이를 리턴하고 있다.

객체 Function의 메소드 apply의 첫번째 인자는 함수가 실행될 맥락이다. 이렇게 생각하자. sum.apply(o1)은 함수 sum을 객체 o1의 메소드로 만들고 sum을 호출한 후에 sum을 삭제한다. 아래와 비슷하다. (실행결과가 조금 다를 것이다. 그것은 함수 for in문으로 객체 o1의 값을 열거할 때 함수 sum도 포함되기 때문이다.)

```
o1.sum = sum;
alert(o1.sum());
delete o1.sum();
```

sum의 o1 소속의 메소드가 된다는 것은 이렇게 바꿔 말할 수 있다. 함수 sum에서 this의 값이 전역객체가 아니라 o1이 된다는 의미다. 일반적인 객체지향 언어에서는 하나의 객체에 소속된 함수는 그 객체의 소유물이 된다. 하지만 JavaScript에서 함수는 독립적인 객체로서 존재하고, apply나 call 메소드를 통해서 다른 객체의 소유물인 것처럼 실행할 수 있다. 흥미롭다.

만약 apply의 첫번째 인자로 null을 전달하면 apply가 실행된 함수 인스턴스는 전역객체(브라우저에서는 window)를 맥락으로 실행되게 된다.

<br>

### **객체지향**

---

객체란 서로 연관된 변수와 함수를 그룹핑한 그릇이라고 할 수 있다. 객체 내의 변수를 프로퍼티(property) 함수를 메소드(method)라고 부른다. 객체를 만들어보자.

```
var person = {}
person.name = 'js';
person.introduce = function(){
    return 'My name is '+this.name;
}
document.write(person.introduce());
```

객체를 만드는 과정이 분산되어 있다. 객체를 정의 할 때 값을 셋팅하도록 코드를 바꿔보자.

```
var person = {
    'name' : 'js',
    'introduce' : function(){
        return 'My name is '+this.name;
    }
}
document.write(person.introduce());
```

만약 다른 사람의 이름을 담을 객체가 필요하다면 객체의 정의를 반복해야 할 것이다. 객체의 구조를 재활용할 수 있는 방법이 필요하다. 이 때 사용하는 것이 생성자다.

생성자(constructor)는 객체를 만드는 역할을 하는 함수다. 자바스크립트에서 함수는 재사용 가능한 로직의 묶음이 아니라 객체를 만드는 창조자라고 할 수 있다.

```
function Person(){}
var p = new Person();
p.name = 'js';
p.introduce = function(){
    return 'My name is '+this.name; 
}
document.write(p.introduce());
```

함수를 호출할 때 new을 붙이면 새로운 객체를 만든 후에 이를 리턴한다. 위의 코드는 새로운 객체를 변수 p에 담았다. 여러사람을 위한 객체를 만든다면 아래와 같이 코드를 작성해야 할 것이다. 

```
function Person(){}
var p1 = new Person();
p1.name = 'js';
p1.introduce = function(){
    return 'My name is '+this.name; 
}
document.write(p1.introduce()+"<br />");
 
var p2 = new Person();
p2.name = 'study';
p2.introduce = function(){
    return 'My name is '+this.name; 
}
document.write(p2.introduce());
```

별로 개선된 것이 없다. 

```
function Person(name){
    this.name = name;
    this.introduce = function(){
        return 'My name is '+this.name; 
    }   
}
var p1 = new Person('js');
document.write(p1.introduce()+"<br />");
 
var p2 = new Person('study');
document.write(p2.introduce());
```

생성자 내에서 이 객체의 프로퍼티를 정의하고 있다. 이러한 작업을 초기화라고 한다. 이를 통해서 코드의 재사용성이 대폭 높아졌다.

코드를 통해서 알 수 있듯이 생성자 함수는 일반함수와 구분하기 위해서 첫글자를 대문자로 표시한다.


일반적인 객체지향 언어에서 생성자는 클래스의 소속이다. 하지만 자바스크립트에서 객체를 만드는 주체는 함수다. 함수에 new를 붙이는 것을 통해서 객체를 만들 수 있다는 점은 자바스크립트에서 함수의 위상을 암시하는 단서이면서 또 자바스크립트가 추구하는 자유로움을 보여주는 사례라고 할 수 있다.

<br>

### **전역객체**
---

전역객체(Global object)는 특수한 객체다. 모든 객체는 이 전역객체의 프로퍼티다. 

```
function func(){
    alert('Hello?');    
}
func();
window.func();
```

func();와 window.func();는 모두 실행이 된다. 모든 전역변수와 함수는 사실 window 객체의 프로퍼티다. 객체를 명시하지 않으면 암시적으로 window의 프로퍼티로 간주된다. 

```
var o = {'func':function(){
    alert('Hello?');
}}
o.func();
window.o.func();
```

자바스크립트에서 모든 객체는 기본적으로 전역객체의 프로퍼티임을 알 수 있다. 

<br>


ECMAScript에서는 전역객체의 API를 정의해두었다. 그 외의 API는 호스트 환경에서 필요에 따라서 추가로 정의하고 있다. 이를테면 웹브라우저 자바스크립트에서는 alert()이라는 전역객체의 메소드가 존재하지만 node.js에는 존재하지 않는다. 또한 전역객체의 이름도 호스트환경에 따라서 다른데, 웹브라우저에서 전역객체는 window이지만 node.js에서는 global이다. 

<br>

### **this**
---



