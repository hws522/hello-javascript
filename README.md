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

앞서 배운 변수와 비교연산자 그리고 조건문을 결합해보자. ID의 값으로 egoing을 입력해보고, 다른 값도 입력해보자. 아래의 예제는 브라우저에서 실행해야 한다. 다른 환경에서는 원하는데로 동작하지 않을 것이다.

    <!DOCTYPE html>
    <html>
    <head>
        <meta charset="utf-8"/>
    </head>
    <body>
        <script>
            id = prompt('아이디를 입력해주세요.')
            if(id=='egoing'){
                alert('아이디가 일치 합니다.')
            } else {
                alert('아이디가 일치하지 않습니다.')
            }
        </script>
    </body>
    </html>

위의 내용에서 prompt() 구문은 사용자가 입력한 값을 가져와서 id 변수의 값으로 대입한다. 이러한 것을 API 또는 함수라고 부르는데, 이에 대한 내용은 곧 배운다. 사용자가 입력한 값이 egoing이라면 '아이디가 일치 합니다'를 출력하고 그렇지 않다면 '아이디가 일치하지 않습니다'를 출력한다.

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
            if(id=='egoing'){
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
            if(id=='egoing' && password=='111111'){
                alert('인증 했습니다.');
            } else {
                alert('인증에 실패 했습니다.');
            }
        </script>
    </body>
    </html>


중첩된 if문을 하나로 줄였다. 덕분에 코드의 복잡성도 낮아졌다. &&는 아래와 같은 의미를 만든다.

"id의 값이 egoing이고 password의 값이 111111이면 참이다"

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

다음 예제는 id 값으로 egoing, k8805, sorialgi 중의 하나를 입력하면 '인증 했습니다'가 출력되고, 그 외의 값을 입력하면 '인증에 실패 했습니다.'를 출력하는 예제다.

    id = prompt('아이디를 입력해주세요.');
    if(id==='egoing' || id==='k8805' || id==='sorialgi'){
        alert('인증 했습니다.');
    } else {
        alert('인증에 실패 했습니다.');
    }


위의 예제에서는 논리 연산자를 3개 사용했다. 2개만 사용하는 것이 아니라는 것을 보여주기 위한 예제다.

다음 예제는 id 값으로 egoing, k8805, sorialgi 중의 하나를 사용하고 비밀번호는 111111을 입력하면 right 외의 경우에는 wrong를 출력하는 예다.


    id = prompt('아이디를 입력해주세요.');
    password = prompt('비밀번호를 입력해주세요.');
    if((id==='egoing' || id==='k8805' || id==='sorialgi') && password==='111111'){
    alert('인증 했습니다.');
    } else {
        alert('인증에 실패 했습니다.');
    }

위의 예제에서는 or와 and를 혼합해서 사용하는 방법을 보여준다. id 값을 테스트 하는 구간을 괄호()로 묶었다. 사용자가 id의 값으로 egoing 비밀번호를 111111을 입력했다면 연산의 순서는 아래와 같이 된다.

1. (id=="egoing" or id=="k8805" or id=="sorialgi") : true가 된다.
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

