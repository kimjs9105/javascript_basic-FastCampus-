<h2 style="color: #EB4A5F; font-weight: bold;">[ Class 01 데이터의 선언과 데이터 타입 ]</h2>

### 01. 상수
#### 상수란?
&nbsp;&nbsp;&nbsp;&nbsp;상수란 <span style="color: #970747; font-weight: bold;">한번 저장하면 변하지 않는 데이터</span>로 하위 버전의 웹브라우저에서는 지원하지 않는 선언이다. 
#### 상수의 선언
상수를 선언 할 때는 <span style="color: #E20049;">'const'</span>를 사용하여 선언하며, 상수의 식별자는 보통 대문자를 사용한다.

    const MY_NAME = "김지선";

#### 상수의 유효범위
상수의 값은 한번 선언하면 변할 수 없지만 상수의 <span style="color: #970747; font-weight: bold;">데이터 타입으로 객체</span>가 온다면 객체 내부에 데이터 추가, 제거등이 가능해진다. 왜냐하면 <span style="color: #970747; font-weight: bold;">객체 내부의 값에 대해서는 상수의 영향을 받지 않기 때문</span>이다.

    const TEST = {
        test01 : 1,
        test02 : 2
    }

    TEST.test03 = 3; //TEST라는 객체 내부에 추가하는 것이므로 가능하다
    TEST = 'DataType 변경' //객체형 타입에서 문자형 타입으로 변경하는 것은 불가능하다.

--------------------------------

### 02. 변수
#### 변수란?
&nbsp;&nbsp;&nbsp;&nbsp;변수란 <span style="color: #970747; font-weight: bold;">저장 되어있는 값이 선언에 따라 변할 수 있는 것</span>으로 가장 마지막으로 선언된 저장 값이 반영된다.
#### 변수의 선언
&nbsp;&nbsp;&nbsp;&nbsp;변수를 선언 할 때는 <span style="color: #E20049;">'var'</span>와 <span style="color: #E20049;">'let'</span>을 사용하여 선언한다. 여러개의 변수를 선언 할 경우 콤마(,)를 사용하여 한번에 선언이 가능하다. 'var'의 경우 재사용이 가능 한 변수이며<span style="color: #9A9B94; font-size: 12px;">(스코프의 제한을 받지 않음)</span>, 'let'의 경우 해당 스코프에서만 사용 할 수있는 변수이다.<span style="color: #9A9B94; font-size: 12px;">(스코프는 심화 페이지에서 자세하게 다룰 예정)</span>또한 'let'의 경우 최신 브라우저에서만 지원되므로 <span style="color: #970747; font-weight: bold;">하위 버전과 호환이 필요하다면 'var'를 써야한다.</span>

    var my_age = 27;
    let my_address = "Korea";

    var my_age = 30; //앞서 변수의 값으로 27을 선언하였지만 30으로 값을 변경

    var a = 1,
        b = 2,
        c = 3; // 변수 3개를 한번에 선언

변수를 저장할때 선언('var','let')을 하지 않고 사용하여도 오류가 나지 않지만, 이렇게 사용 할 경우 전역스코프에 선언되어 원하는 결과를 도출하기 어려움으로 지양해야하는 방법이다.  

--------------------------------

### 03. 데이터와 데이터 타입
&nbsp;&nbsp;&nbsp;&nbsp;데이터의 성격에 따라 상수와 변수에 값을 선언하는 규칙이 각각 다르게 존재한다.

#### 1) String(문자형 데이터) 

&nbsp;&nbsp;&nbsp;&nbsp;문자형 데이터는 <span style="color: #970747; font-weight: bold;">값을 문자로 선언</span>하는 것이다. 문자는 따옴표(' ') 또는 쌍따옴표(" ")로 감싸서 선언한다. 문자형 데이터는 한 줄을 넘어가면 자동으로 다른 값으로 선언되므로 \n을 사용하여 처리한다.

    var text_type01 = 'text type'; //따옴표 사용
    var text_type02 = "text type"; //쌍따옴표 사용
    var text_type01 = 'text type \n texttype'; //줄넘김 처리 사용

#### 2) Number(숫자형 데이터) 

&nbsp;&nbsp;&nbsp;&nbsp;숫자형 데이터는 <span style="color: #970747; font-weight: bold;">값을 숫자로 선언</span>하는 것이다. 감싸거나 따로 표기하는 방식 없이 그래도 써주면 된다.

    var number_type = 25; //값 25 선언
    var text_type = "30"; // 단, 숫자형 데이터가 따옴표 또는 쌍따옴표에 들어가면 문자형 데이터로 형변환 된다
    
#### 3) Boolean

&nbsp;&nbsp;&nbsp;&nbsp;Boolean의 경우 <span style="color: #970747; font-weight: bold;">값이 true 와 false로만 존재</span>하며 다른 값을 올 수 없다. 보통 비교연산자 또는 판단문 등에 대한 데이터로 사용된다.

    var answer = true; // true 값 선언
    var test = ( 1 == 2 ); // 숫자 1과 2는 같지 않으므로 결과로 false 도출

#### 4) Object(객체형 데이터와 배열)
&nbsp;&nbsp;&nbsp;&nbsp;Object로는 객체형 데이터와 배열이 있는데 객체형 데이터는 <span style="color: #970747; font-weight: bold;">중괄호({ })안에 이름과 값을 한쌍으로 가지는 데이터들의 조합</span>이고, 배열은 <span style="color: #970747; font-weight: bold;">대괄호([ ])안에 저장하는 데이터들의 조합</span>이다. 회원관리 시스템처럼 동일한 변수의 값들의 그룹을 저장할 때 유용하게 사용된다

    // 객체형 데이터 

    var object = {a : 1,
                  b : 2,
                  c : 3
                  }; // 객체형 데이터 기본형

    var members = {
            member01: {
                name : "kim",
                age : 27
            },
            member02 : {
                name : "Lee",
                age : 50
            }
        } // 객체형 데이터 응용

    console.log(members.member02.name); 
    // 결과 : Lee, 
    // member 객체 내부의 member02를 찾아서 해당 객체의 name의 값을 가져옴
&nbsp;

    // 배열 
    
    var array = {'a', 'b', 'c'}; // 배열

&nbsp;&nbsp;&nbsp;&nbsp; 둘 다 <span style="color: #E20049;">'typeof'</span> 연산자<span style="color: #9A9B94; font-size: 12px;">(데이터의 타입을 알아보는 연산자)</span>를 사용하여 결과를 보면 object라는 결과값을 받게 되는데 두가지의 사용법과 응용<span style="color: #9A9B94; font-size: 12px;">(데이터추가,삭제등)</span>법은 다르게 사용되니 참고하여 사용한다<span style="color: #9A9B94; font-size: 12px;">(자세한 내용은 심화 페이지에서 다룰 예정)</span>

    var obj_group = {a : 1,
                  b : 2,
                  c : 3
                  }; // 객체형 데이터
    var arr_group = {'a', 'b', 'c'}; // 배열
    
    typeof obj_group; //object 출력
    typeof arr_group; //object 출력
    
#### 5) undefined 와 null
&nbsp;&nbsp;&nbsp;&nbsp; undefined 와 null 모두 <span style="color: #970747; font-weight: bold;">데이터가 없을 때 발생하며 아무것도 없음을 의미하는</span> 결과값이지만, 발생하는 조건에 있어서 차이점을 가지고 있다. undefined 데이터의 경우 변수를 선언 했지만 <span style="color: #970747; font-weight: bold;">값을 할당하지 않은 아무것도 없는 것을 의미하며 데이터의 성격조차도 알수 없는 것을 의미</span>한다. 반면 null은 변수로 <span style="color: #970747; font-weight: bold;">배열 또는 객체형 데이터 등을 선언했지만 그 안에 데이터가 없을경우를 의미</span>하는 데이터이다.

    var a; //undefined, 아무것도 선언하지 않음
    var b = []; //null, 빈 배열이기 때문에 데이터가 없음

#### 6) NaN
&nbsp;&nbsp;&nbsp;&nbsp; Not a Number의 약어로써 <span style="color: #970747; font-weight: bold;">해당 값이 숫자로써 정상적인 값이 아님을 의미</span>한다. 예를 들어 숫자가 들어와 연산을 진행해야 하는 명령어에서 숫자가 아닌 값이 들어온다거나, 데이터를 0으로 나누는 등의 연산에 대해 나오는 결과 값이다. NaN은 의미상 '숫자가 아니다'라는 뜻을 가져 데이터 타입이 애매해 보이지만 <span style="color: #970747; font-weight: bold;">'typeof'연산자로 결과를 출력할 경우 number를 출력</span>하니 참고하도록 하자.

--------------------------------

### 04. 데이터 타입의 분류
&nbsp;&nbsp;&nbsp;&nbsp;데이터 타입은 두가지 타입으로 나눌 수 있는데 기본형 데이터 타입<span style="color: #9A9B94; font-size: 12px;">(원시형)</span>과 참조형 데이터 타입이 있다.
* 기본형 데이터 타입<span style="color: #9A9B94; font-size: 12px;">(원시형)</span> : 기본형 데이터 타입으로는 문자형, 숫자형, boolean, null, undefined등 우리가 기본적으로 알고있는 데이터 타입이 이에 속한다.
* 참조형 데이터 타입 : 데이터가 너무 클 경우 값의 주소만 적어 로드를 하거나 특정 명령에에 따른 실행 시 데이터를 불러오는 형태를 가진 타입을 의미한다. 값은 외부에 저장해 두는 형태를 가지고 있으며 여기서 말하는 외부는 javascript가 구동되는 저장소 이 외의 공간을 의미한다.

