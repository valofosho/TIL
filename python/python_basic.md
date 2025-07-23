- Python
    
    표현식(Expression)
    
    - 하나의 ‘값’으로 평가될 수 있는 모든 코드
        - 평가 → 표현식을 계산하여 그 결과인 ‘값’을 만들어내는 과정
    
    값(Value)
    
    - 표현식이 평가된 결과
    - 더 이상 계산되거나 평가될 수 없는, 프로그램의 가장 기본적인 데이터 조각
    
    불리언(Boolean)
    
    - 컴퓨터에서 참과 거짓을 나타내는 숫자 1과 0만을 이용하는 방식
    
    변수(Variable)
    
    - 값을 나중에 다시 사용하기 위해, 그 값에 붙여주는 고유한 이름
    
    변수 할당(Variable Assignment)
    
    - 표현식이 만들어 낸 값에 이름을 붙이는 과정(연결)
    
    변수명 규칙
    
    - 영문 알파벳, 언더스코어, 숫자로 구성
    - 숫자로 시작할 수 없음
    - 대소문자를 구분
    - 아래 키워드는 파이썬의 내부 예약어로 사용할 수 없음
        
    
    메모리 주소
    
    - 컴퓨터가 특정 데이터 값을 정확히 찾아가기 위해 사용하는 기계적인 숫자 주소
    
    객체
    
    - 값, 타입, 그리고 관련된 행동까지 하나로 묶인 개념, 객체는 파이썬에서 다루는 모든 데이터의 실체
    - 값 + 타입 + 주소 정보(메모리)를 묶은 것을 객체(Object)라고 부름
    - 변수는 특정 객체를 ‘가리키는(refer/point to)’ 이름표
    - 변수는 메모리 주소를 ‘가지지(contain)’ 않습니다.
    
    ---
    
    변수
    
    - 값을 나중에 다시 사용하기 위해, 그 값에 붙여주는 고유한 이름
    - “객체를 가리키는 이름”
    
    할당문 동작 순서
    
    ```python
    Variable = expression
    ```
    
    1. 오른쪽 표현식 평가
        - 가장 먼저, 할당 연산자(=)의 오른쪽에 있는 표현식 전체를 계산해 하나의 객체 생성
    2. 왼쪽 변수명 확인
        - 이름이 처음 사용되었다면: 새로운 “이름표”를 준비
        - 이미 존재하는 이름이라면: 기존 “이름표”를 그대로 사용
    3. 변수명과 결과값 연결(참조)
        - 마지막으로 왼쪽의 변수명이 오른쪽에서 만들어진 결과값을 가리키도록 연결
        - 변수명이 이전에 다른 객체를 가리키고 있었다면, 그 연결은 끊어지고 새로운 객체와의 연결만 남음(재할당)
    
    재할당(Reassignment)
    
    - 이미 값이 할당된 변수에 새로운 값을 다시 할당
    
- Data Types
    
    Type
    
    - 변수나 값이 가질 수 있는 데이터의 종류
    - “값”과 “값에 적용할 수 있는 연산”
    
    Data Types
    
    - 값의 종류와 그 값으로 할 수 있는 ‘동작(연산)’을 결정하는 속성
    - 각 타입에 따라 가능한 기능과 연산이 달라 데이터 타입이 필요
- Numeric Types
    
    숫자형 데이터 
    
    1. 정수 자료형(int)
    2. 실수 자료형(float)
        - 지수 표현법
            - big_num = 1.23e9 == (1.23*10^9)
            - small_num = 3.14e-3 == (3.14*10^-3)
    
    숫자형의 ‘행동’ - 산술 연산
    
    - 숫자형 데이터의 핵심 ‘행동’은 바로 계산
    - 데이터 타입은 ‘값의 종류’와 ‘적용 가능한 행동’의 묶음
    - 파이썬은 다양한 계산을 위한 산술 연산자 제공
        
        
        | 기호 | 설명 |
        | --- | --- |
        | + | 덧셈 |
        | - | 뺄셈 |
        | * | 곱셈 |
        | / | 나눗셈 |
        | // | 몫 나눗셈 |
        | % | 나머지 |
        | ** | 거듭제곱 |
        | - | 음수 부호  |
    - 연산자 우선순위
        
        
        | 우선순위 | 연산자 | 연산 |
        | --- | --- | --- |
        | 높음 | ** | 지수 |
        |  | - | 음수 부호 |
        |  | *, /, //, % | 곱셈, 나눗셈, 정수 나눗셈, 나머지 |
        | 낮음 | +, - | 덧셈, 뺄셈 |
- Sequence Type
    - 여러 값들을 순서대로 나열하여 저장하는 자료형
    - Sequence → 여러 데이터가 정해진 순서대로 일렬로 늘어선 자료구조
    - str, list, tuple, range
    - 인덱스(Index) → 시퀀스 자료형에서 각 값의 위치를 식별하기 위해 부여된 고유번호
    - 시퀀스 타입의 5가지 공통 특징
        1. 순서 (Order)
            - 값들이 순서대로 저장(정렬 X)
        2. 인덱싱(Indexing)
            - 각 값에 고유 번호(인덱스)를 가지고 있으며, 인덱스를 사용하여 특정 위치의 값을 선택하거나 수정할 수 있음
        3. 슬라이싱(Slicing)
            - 인덱스 범위를 조절해 전체 데이터 중 원하는 부분만 값을 잘라내서 사용
        4. 길이(Length)
            - len() 함수를 사용하여 저장된 값의 개수(길이)를 구할 수 있음
        5. 반복(Iteration)
            - 반복문을 사용하여 각 값을 하나씩 순서대로 꺼내 사용할 수 있음
        
        ---
        
        시퀀스 타입 특징 예시
        
        - my_data = “hello”
            
            
            | 특징 | 사용 예시 | 결과 |
            | --- | --- | --- |
            | 인덱싱 | my_data[1] | ‘e’ |
            | 슬라이싱 | my_data[1:4] | ‘ell’ |
            | 길이 | len(my_data) | 5 |
            | 반복 | for char in my_data | H, e, l, l, o 가 차례로 출력 |
- str(문자열)
    
    문자열 → 문자들의 순서가 잇는 변경 불가능한 시퀀스 자료형
    
    - 이스케이프 시퀀스(Escape Sequence)
        - 역슬래시(\)와 문자를 조합해 특별한 기능을 수행(e.g. 줄바꿈, 탭)
            
            
            | 예약 문자 | 기능 |
            | --- | --- |
            | \n | 줄 바꿈 |
            | \t | 탭 |
            | \\ | 백슬래시 |
            | \’ | 작은 따옴표 |
            | \” | 큰 따옴표 |
    - 문자열에 값 삽입: f-string
        - 문자열 내에 변수나 표현식의 결과를 손쉽게 삽입
        - 문자열 시작 전 ‘f’ 접두어를 붙이고, 삽입할 부분(표현식)을 중괄호 {}로 감싸줌
    - 시퀀스로서의 문자열
        - 문자열은 시퀀스이므로, 인덱싱, 슬라이싱, 길이 확인, 반복 등 공통 기능 모두 사용
            
            
            | 특징 | 사용 예시 | 결과 | 설명 |
            | --- | --- | --- | --- |
            | 인덱싱 | my_str[1] | ‘e’ | 1번 위치의 글자 선택 |
            | 슬라이싱 | my_str[1:4] | ‘ell’ | 1번부터 4번 앞까지 부분 추출 |
            | 길이 | len(my_str) | 5 | 문자열의 전체 길이 |
            | 반복 | for char in my_str | H, e, l, l, o | 각 문자를 순서대로 처리 |
    
    ---
    
    인덱스
    
    - 시퀀스 자료형에서 각 값의 위치를 식별하기 위해 부여된 고유한 번호
    
    슬라이싱(Slicing)
    
    - 시퀀스의 일부를 잘라내어 새로운 시퀀스를 만드는 작업
    - 대괄호 `[]` 안에 시작 위치, 끝 위치, 간격(step)을 콜론(:)으로 구분하여 지정
        
        `my_sequence[start:stop:step]`
        
        1. start: 슬라이싱을 시작할 인덱스(포함됨)
        2. stop: 슬라이싱을 끝낼 인덱스(포함되지 않음)
        3. step: 몇 개씩 건너뛰며 값을 가져올지에 대한 간격
            
            
            | 사용 예시 | 결과 |
            | --- | --- |
            | my_str[2:4] | ‘ll’ |
            | my_str[:3] | ‘hel’ |
            | my_str[3:] | ‘lo’ |
            | my_str[::2] | ‘hlo’ |
            | mystr[::-1] | ‘olleh’ |
    
    문자열의 불변성
    
    - 문자들의 순서가 있는 변경 불가능한 시퀀스 자료형
        - `'str' object does not support item assignment`
    - 기존의 문자열을 바꾸려면 일부 + 새로운 값을 조합해 새로운 문자열 생성
        
        ```python
        my_str = 'Hello'
        new_str = my_str[0] + 'a' + my_str[2:]
        ---
        my_str = 'Hallo'
        # >>> my_str을 변경한게 아닌 새로운 값으로 '재할당' 한 것
        ```
        
- 참고
    1. 정수형의 진법 표현
        - 파이썬은 코드 내 다양한 진법의 숫자 표현을 위해 특별한 접두사(prefix) 제공
            
            
            | 진법 | 접두사 | 사용하는 숫자/문자 |
            | --- | --- | --- |
            | 2진수(binary) | 0b | 0과 1 |
            | 8진수(octal) | 0o | 0부터 7까지 |
            | 16진수(hexadecimal) | 0x | 0부터 9, a부터 f 까지 |
            
            ```python
            # 2진수 10은 10진수로 2입니다.
            print(0b10)
            # 8진수 30은 10진수로 24입니다.
            print(0o30)
            # 16진수 10은 10진수로 16입니다.
            print(0x10)
            ```
            
    2. 실수의 함정, 부동소수점의 오차
        
        부동소수점 (반올림) 오차 (Floating-point Rounding Error)
        
        - 발생 원인
            1. 컴퓨터는 2진법 사용
            2. 무한 소수의 발생과 근사값 저장
                - 10진수 소수 중 일부(예:0.1)는 2진수로 바꾸면 무한히 반복되는 무한 소수가 됨
                - 0.1(10진수) → 0.0001100110011(2진수)
                - 메모리는 유한하기 때문에, 가장 가까운 근사값으로 잘라서 저장
        - 해결책
            - Decimal 모듈을 활용해 부동소수점 연산의 정확성 보장
            - decimal은 실수를 2진수로 변환하지 않고, 10진수 자체로 정확하게 연산


- list
    
    리스트
    
    - 여러 개의 값을 순서대로 저장하는, 변경 가능한(mutable) 시퀀스 자료형
    
    리스트 표현
    
    - 대괄호 `[]` 안에 값들을 쉼표`(,)`로 구분
    - 숫자, 문자열, 리스트까지 모든 종류의 데이터를 담음
    - 값을 추가, 수정, 삭제 등 자유롭게 변경 가능
        
        ```python
        my_list1 = []
        my_list_2 = [1, 'a', 3, 'b', 5]
        my_list_3 = [1, 2, 3, 'Python', ['hello', 'world', '!!!']]
        ```
        
    
    리스트의 시퀀스 특징
    
    - 리스트는 시퀀스 자료형으로 문자열처럼 인덱싱, 슬라이싱, 길이 확인, 반복 등 공통 기능 모두 가능
        
        ```python
        my_list = [1, 'a', 3, 'b', 5]
        
        #인덱싱
        print(my_list[1]) # a
        
        #슬라이싱
        print(my_list[2:4]) # [3, 'b']
        print(my_list[:3]) # [1, 'a', 3]
        print(my_list[3:]) # ['b', 5]
        print(my_list[::2]) # [1, 3, 5]
        print(my_list[::-1]) # [5, 'b', 3, 'a', 1]
        
        #길이
        print(len(my_list)) # 5
        ```
        
    
    중첩 리스트 (Nested List)
    
    - 다른 리스트를 값으로 가진 리스트
    - 인덱스를 연달아 사용해 안쪽 리스트의 값에 접근
        1. 먼저 바깥 리스트의 인덱스로 안쪽 리스트를 선택
        2. 선택된 안쪽 리스트에 다시 한 번 인덱스를 사용
            
            ```python
            my_list = [1, 2, 3, 'Python', ['hello', 'world', '!!!']
            
            print(len(my_list)) # 5
            print(my_list[4][-1]) # !!!
            print(my_list[-1][1][0] # w
            ```
            
    
    리스트의 가변성
    
    - 한 번 생성된 리스트는 “그 내용을 자유롭게 수정, 추가, 삭제 가능”
        
        → 문자열의 `불변성(Immutability)`과 정반대되는 매우 중요한 특징
        
        1. 인덱싱으로 값 수정
            
            ```python
            my_list = [1, 2, 3, 4, 5]
            my_list[1] = 'two'
            print(my_list) # [1, 'two', 3, 4, 5]
            ```
            
        2. 슬라이싱으로 여러 값 한 번에 변경
            
            ```python
            my_list = [1, 2, 3, 4, 5]
            my_list[2:4] = ['three', 'four']
            print(my_list) # [1, 2, 'three', 'four', 5]
            ```
            
    
- tuple
    
    튜플(tuple)
    
    - 여러 개의 값을 순서대로 저장하는 변경 불가능한 시퀀스 자료형
    
    튜플 표현
    
    - 소괄호 `()` 안에 값들을 쉼표`(,)`로 구분하여 만듦
    - 모든 종류의 데이터를 담을 수 있음
    - 리스트와 달리 한 번 만들어지면 절대 수정할 수 없음
        
        ```python
        my_tuple_1 = ()
        my_tuple_2 = (1,)
        my_tuple_3 = (1, 'a', 3, 'b', 5)
        my_tuple_4 = 1, 'hello', 3.14, True
        ```
        
    - 소괄호 `()` 없이도 튜플 생성 가능
    - 단일 요소 튜플 생성시 반드시 Trailing comma(후행 쉼표)를 사용
    
    튜플의 시퀀스 특징
    
    - 인덱싱, 슬라이싱, 길이 확인, 반복 등 공통 기능 모두 사용 가능
        
        ```python
        my_tuple = (1, 'a', 3, 'b', 5)
        
        # 인덱싱
        print(my_tuple[1]) # a
        
        # 슬라이싱
        print(my_tuple[2:4]) # (3, 'b')
        print(my_tuple[:3]) # (1, 'a', 3)
        print(my_tuple[3:]) # ('b', 5)
        print(my_tuple[::2]) # (1, 3, 5)
        print(my_tuple[::-1]) # (5, 'b', 3, 'a', 1)
        
        #길이
        print(len(my_tuple)) # 5
        ```
        
    
    튜플의 불변성
    
    - 한 번 생성된 튜플은 그 내용을 절대 수정, 추가, 삭제 불가능
        
        ```python
        my_tuple = (1, 'a', 3, 'b', 5)
        
        #TypeError: 'tuple' object does not support item assignment
        my_tuple[1] = 'z'
        ```
        
    
    튜플의 쓰임새
    
    - 튜플의 불변 특성을 통해 내부 동작과 안전한 데이터 전달에 사용
    - 다중 할당, 값 교환, 다중 반환 값 등
    - 튜플은 데이터의 `"안정성과 무결성"`을 보
        
        ```python
        # 다중 할당
        x, y = 10, 20
        print(x) # 10
        print(y) # 20
        
        #실제 내부 동작
        (x, y) = (10, 20)
        
        #값 교환
        x, y = 1, 2
        x, y = y, x
        #실제 내부 동작
        temp = (y,x) # 튜플 생성
        x, y= temp # 튜플 풀어냄
        print(x, y) # 2 1
        ```
        
- range
    
    Range
    
    - 연속된 정수 시퀀스를 생성하는, 변경 불가능한(immutable) 자료형
    - 주로 반복문과 함께 사용되어 특정 횟수만큼 코드 반복 실행
    - 모든 숫자를 메모리에 저장하는 대신 `start, stop, step` 이라는 ‘규칙’만 기억해 메모리 효율적 사용
    
    range 기본 구문
    
    - `range()`는 1개, 2개, 또는 3개의 매개변수(인자)를 가질 수 있다
    - `range(strat, stop, step)`
    
    range 매개변수별 특징
    
    - `range(stop)`
        - 매개변수가 하나면 stop으로 인식
        - start는 0이 step은 1이 디폴트
    - `range(start, stop)`
        - 매개변수가 두 개면 start와 stop으로 인식
        - step은 1이 디폴트
    - `range(start, stop, step)`
        - 모든 매개변수를 직접 지정
        
        ```python
        my_range_1 = range(5)
        my_range_2 = range(1, 10)
        my_range(5, 0, -1)
        
        print(my_range_1) # range(0, 5)
        print(my_range_2) # range(1, 10)
        print(my_range_3) # range(5, 0, -1)
        
        print(list(my_range_1)) # [0, 1, 2, 3, 4]
        print(list(my_range_2)) # [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
        print(list(my_range_3)) # [5, 4, 3, 2, 1]
        ```
        
        Range 기본 규칙
        
        1. 값의 범위 규칙
            - stop 값은 생성되는 시퀀스에 절대 포함되지 않음
        2. 증가/감소 값(step) 규칙
            - step 값은 숫자 시퀀스의 간격과 방향을 결정
            1. step이 양수일 때 (기본값: 1)
                - 숫자가 start부터 stop을 향해 증가
            2. step이 음수일 때
                - 숫자가 start부터 stop을 향해 감소
                - start는 반드시 stop 값보다 커야함
            
            ```python
            # 시작 값이 끝 값보다 작은 경우 (정상)
            print(list(range(1, 5))) # [1, 2, 3, 4, 5]
            # 시작 값이 끝 값보다 큰 경우
            print(list(range(5,1))) # []
            #시작 값이 끝 값보다 큰 경우 (정상)
            print(list(range(5, 1, -1))) # [5, 4, 3, 2, 1]
            # 시작 값이 끝 값보다 작은 경우
            print(list(range(1, 5, -1) # []
            ```
            
- dict
    
    딕셔너리 (dict)
    
    - key -value 쌍으로 이루어진 순서와 중복이 없는 변경 가능한 자료형
    
    딕셔너리 표현
    
    - `중괄호 {}` 안에 값들이 쉼표(,) 로 구분
    - 값 1개는 키와 값이 쌍으로 이루어져 있음
    - Key(키)
        - 값을 식별하기 위한 고유의 ‘이름표’ `(중복 불가)`
    - Value(값)
        - 키에 해당하는 실제 데이터
    - 각 값에는 순서가 없음
        - 파이썬 3.7 이상에서는 입력 순서는 출력시 그대로 유
        
        ```python
        my_dict_1 = {}
        my_dict_2 = {'key': 'value'}
        my_dict_3 = {'apple': 12, 'list': [1, 2, 3]}
        
        print(my_dict_1) # {}
        print(my_dict_2) # {'key': 'value'}
        print(my_dict_3) # {'apple': 12, 'list': [1, 2, 3]}
        ```
        
    
    딕셔너리 규칙
    
    Key 규칙
    
    - 고유해야 함 (중복 불가)
    - 변경 불가능한(immutable) 자료형만 사용 가능
        - `str, int, float, tuple` >> 가능
        - `list, dict` >> 불가능
    
    Value의 규칙
    
    - 어떤 자료형이든 자유롭게 사용 가능
    
    딕셔너리 값 접근 방법
    
    - Key를 사용해 해당 Value 꺼내옴
    - Key에 접근 시 `대괄호 []` 사용
    - 존재하지 않는 Key로 접근하면 KeyError
        
        ```python
        my_dict = {'name': '홍길동', 'age': 25}
        print(my_dict['name']) #'홍길동'
        print(my_dict['test']) # KeyError: 'test'
        ```
        
    
    딕셔너리 값 추가 및 변경
    
    ```python
    my_dict = {'apple': 12, 'list': [1, 2, 3]}
    
    # 추가
    my_dict['banana'] = 50
    print(my_dict) # {'apple': 12, 'list': [1, 2, 3], 'banana': 50}
    # 변경
    my_dict['apple'] = 100
    print(my_dict) # {'apple': 100, 'list': [1, 2, 3], 'banana': 50)
    ```
    
- set
    
    세트(set)
    
    - 순서와 중복이 없는 변경 가능한 자료형
    
    세트 표현
    
    - `중괄호{}` 안에 값들을 쉼표(,)로 구분하여 만듦
    - 수학에서의 집합과 동일한 연산 처리 가능
    - 딕셔너리와의 혼등을 피해 비어있는 세트는 set()으로 생
    
    세트의 핵심 특징
    
    1. 중복 불허
        - 똑같은 값은 단 하나만 존재
    2. 순서가 없음
        - 인덱싱(`set[0]`)이나 슬라이싱(`set[0:2]`)을 사용 불가
        
        ```python
        my_set_1 = set()
        my_set_2 = {1, 2, 3}
        my_set_3 = {1, 1, 1}
        
        print(my_set_1) # set()
        print(my_set_2) # {1, 2, 3}
        print(my_set_3) # {1}
        ```
        
    
    세트의 집합 연산
    
    ```python
    my_set_1 = {1, 2, 3}
    my_set_2 = {3, 6, 9}
    
    # 합집합
    print(my_set_1 | my_set_2_) # {1, 2, 3, 6, 9}
    # 차집합
    print(my_set_1 - my_set_2) # {1, 2}
    #교집합
    print(my_set_1 & my_set_2) # {3}
    ```
    
- Other Types
    
    None
    
    - 파이썬에서 ‘값이 없음’을 표현하는 데이터 타입
    - 숫자 0이나 빈 문자열(’’)과는 다른, `‘값이 존재하지 않음’` 또는 `‘아직 정해지지 않음'’`
        
        ```python
        # my_variable에는 아직 아무 값도 할당하고 싶지 않을 때
        my_variable = None
        print(my_variable) # None
        ```
        
    
    Boolean
    
    ‘참(True)’과 ‘거짓(False)’ 단 두 가지 값만 가지는 데이터 타입
    
    Boolena 표현
    
    - 비교 /논리 연산의 평가 결과로 사용됨
        
        ```python
        is_active = True
        is_logged_in = False
        
        print(is_active) # True
        print(is_logged_in) # False
        print(10 > 5) # True
        print(10 == 5) # False
        ```
        
- Collection
    
    Collection
    
    - 여러 개의 값을 하나로 묶어 관리하는 자료형 통칭
    - str, list, tuple, range, set, dict 데이터 타입이 모두 Collection에 분류
        
        
        | 컬렉션명 | 변경 가능 여부 | 순서 존재 여부(시퀀스 여부) |
        | --- | --- | --- |
        | str | X | O |
        | list | O | O |
        | tuple | X | O |
        | dict | O | X |
        | set | O | X |
    
    불변 VS 가변
    
    - 컬렉션 타입은 생성 후 내용 변경 가능 여부에 따라 ‘불변’과 ‘가변’ 두 그룹으로 나뉨
        
        
        | 구분 | 불변(Immutable) | 가변(Mutable) |
        | --- | --- | --- |
        | 특징 | 변경 불가, 안전성, 예측 가능 | 변경 가능, 유연성, 효율성 |
        | 종류 | str, tuple, range | list, dict, set |
- 형변환
    
    형변환(Type Conversion)
    
    - 한 데이터 타입을 다른 데이터 타입으로 변환하는 과정
    
    암시적 형변환(Implicit Conversion)
    
    - 파이썬이 연산 중에 자동으로 데이터 타입을 변환
    - 정수와 실수의 연산에서 정수가 실수로 변환
    - Boolean과 Numeric Type에서만 가능
        
        ```python
        # 정수(int)와 실수(float)의 덧셈
        print(3 + 5.0) # 8.0
        # 불리언(bool)과 정수(int)의 덧셈
        print(True + 3) # 4 >>> True = 1, False = 0
        # 불리언(bool)간의 덧셈
        print(True + False) # 1
        ```
        
    
    명시적 형변환(Explicit Conversion)
    
    - 직접 함수로 지정하여 형변환
        
        
        | 함수 | 설명 | 예시 | 결과 |
        | --- | --- | --- | --- |
        | int() | 정수로 변환 | int(”123”) | 123 |
        | float() | 실수로 변환 | float(”3.14”) | 3.14 |
        | str() | 문자열로 변환 | str(100) | “100” |
        | list() | 리스트로 변환 | list(”abc”) | [’a’, ‘b’, ‘c’] |
        | tuple() | 튜플로 변환 | tuple([1, 2]) | (1, 2) |
        | set() | 세트로 변환 | set([1, 2, 2]) | {1, 2} |
- 연산자
    
    산술 연산자
    
    - 수학적 계산을 위해 사용
        
        
        | 기호 | 연산자 |
        | --- | --- |
        | - | 음수 부호 |
        | + | 덧셈 |
        | - | 뺄셈 |
        | * | 곱셈 |
        | / | 나눗셈 |
        | // | 정수 나눗셈(몫) |
        | % | 나머지 |
        | ** | 지수(거듭제곱) |
    
    복합 연산자
    
    - 연산과 할당이 함께 이루어짐
        
        
        | 기호 | 예시 | 의미 |
        | --- | --- | --- |
        | += | a += b | a = a + b |
        | -= | a -= b | a = a - b |
        | *= | a *= b | a = a * b |
        | /= | a /= b | a = a / b |
        | //= | a //= b | a = a // b |
        | %= | a %= b | a = a % b |
        | **= | a **= b | a = a ** b |
    
    비교 연산자
    
    - 두 값을 비교하여 그 관계가 맞는지 틀리는지를  True 또는 False로 반환
        
        
        | 기호 | 내용 |
        | --- | --- |
        | < | 미만 |
        | <= | 이하 |
        | > | 초과 |
        | >= | 이상 |
        | == | 같음 |
        | != | 같지 않음 |
        | is | 같음 |
        | is not | 같지 않음 |
        - == 연산자
            - 값(데이터)이 같은지를 비교
            - 동등성(equality)
        - is 연산자
            - 객체 자체가 같은지를 비교
            - 식별성(identity)
            - 두 변수가 완전히 동일한 객체, 즉 메모리 주소가 같은지 확인에 사
        
        ```python
        print(2 == 2.0) # True
        print(2 != 2) # False
        print('HI' == 'hi') # False
        print(1 == True) # True
        
        #SyntaxWarning: "is" with a literal. Did you mean "=="?
        print(1 is True) # False
        print(2 is 2.0) # False
        ```
        
        `is` VS `==`
        
        - `is`는 ‘정체성’, `==`는 ‘가치’
        - `is`(Identity Operator):
            - 두 변수가 완전히 동일한 메모리 주소의 객체를 가리키는지
        - `==`(Equality Operator):
            - 두 변수가 가리키는 객체의 내용, 즉 ‘값(Value)’이 같은지
    
    `is`는 언제 사용하는가
    
    주로 싱글턴 객체를 비교 할 때 사용
    
    - 싱글턴(Singleton) 객체란?
        - 특정 값에 대해 파이썬 전체에서 단 하나의 객체만 생성되어 재사용되는 객체
        - ex) None, True, False
    
    ---
    
    리스트나 객체 비교 시 주의사항
    
    - 리스트 또는 다른 가변 객체(mutable)를 비교할 때, 값 자체가 같은지 >> `==`
    - 두 변수가 완전히 동일한 객체를 가리키는지 >> `is`
        
        ```python
        a = [1, 2, 3]
        b = [1, 2, 3]
        
        print(a == b) # True(두 리스트의 값은 동일)
        print(a is b) # False(서로 다른 리스트 객체 >> 메모리 주소가 다름)
        
        # b가 a를 그대로 참조하도록 할 경우
        b = a
        print(a is b) #True (같은 객체를 가리키므로 True)
        ```
        
    
    논리 연산자
    
    - 여러 조건을 조합하거나, True/False 값을 반대로 뒤집을 때 사용
        
        
        | 기호 | 연산자 | 내용 |
        | --- | --- | --- |
        | and | 논리곱 | 두 피연산자 모두 True > True |
        | or | 논리합 | 두 피연산자 중 하나라도 True > True |
        | not | 논리부정 | 단일 피연산자를 부정 |
    
    단축 평가
    
    - 논리 연산에서 두 번째 피연산자를 평가하지 않고 결과를 결정하는 동작
        
        ```python
        item1 = '지도'
        item2 = '나침반'
        # and는 item1('지도')를 보고 통과
        # -> item2('나침반')를 보고 통과
        # -> 맨 마지막 값인 '나침반'을 최종 결과롤 선택
        
        result = item1 and item2
        print(f"최종적으로 챙긴 물건: {result}")
        # >> 최종적으로 챙긴 물건: 나침반
        
        item1 = '지도'
        item2 = ''
        # and는 item1('지도')를 보고 통과 -> item2('')를 봄
        # -> item2가 '내용 없는 값'이므로, 여기서 멈추고 ''를 최종 결과롤 선택
        
        result = item1 and item2
        print(f"최종적으로 챙긴 물건: {result}")
        # >> 최종적으로 챙긴 물건: ''
        
        item1 = ''
        item2 = '나침반'
        # and는 item1('')를 보자마자 '탈락!'을 외치며 평가를 멈춤
        # -> 그 자리에서 바로 ''를 최종 결과로 선택!
        # (item2는 쳐다보지도 않음)
        
        result = item1 and item2
        print(f"최종적으로 챙긴 물건: {result}")
        # >> 최종적으로 챙긴 물건: ''
        ```
        
    - 코드 실행 최적화 및 불필요한 연산 피하기
    
    멤버십 연산자
    
    - 특정 값이 시퀀스나 다른 컬렉션 안에 포함되어 있는지 확인하는 연산자
        
        
        | 기호 | 내용 |
        | --- | --- |
        | in | 왼쪽 피연산자가 오른쪽 피연산자의 시퀀스에 속하는지를 확인 |
        | not in | 왼쪽 피연산자가 오른쪽 피연산자의 시퀀스에 속하지 않는지를 확인 |
    
    시퀀스형 연산자
    
    - 시퀀스 자료형(문자열, 리스트, 튜플)에 특별한 의미로 사용되는 연산자
    - `+`는 시퀀스를 연결하는 기능을, `*`는 시퀀스를 반복하는 기능
        
        
        | 연산자 | 내용 |
        | --- | --- |
        | `+` | 결합 연산자 |
        | `*`  | 반복 연산자 |
    
    연산자 우선순위
    
    | 우선순위 | 연산자 | 내용 |
    | --- | --- | --- |
    | 높음 | () | 소괄호 grouping |
    |  | [] | 인덱싱, 슬라이싱 |
    |  | ** | 거듭제곱 |
    |  | +, - | 단항 연산자 양수/음수 |
    |  | *, /, //, % | 산술 연산자 |
    |  | +, - | 산술 연산자 |
    |  | <, <=, >, >=, ==, != | 비교 연산자 |
    |  | is, is not | 객체 비교 |
    |  | in, not in | 멤버십 연산자 |
    |  | not | 논리 부정 |
    |  | and | 논리 AND |
    | 낮음 | or | 논리 OR |
- Trailing Comma
    
    Trailing Comma
    
    - 컬렉션의 마지막 요소 뒤에 붙는 쉼표
    
    기본 규칙
    
    - 각 요소를 별도의 줄에 작성
    - 마지막 요소 뒤에 trailing comma 추가
    - 닫는 괄호는 새로운 줄에 배치
        
        ```python
        items = [
        		'item1',
        		'item2',
        		'item3',
        ]
        
        config = {
        		'host': 'localhost',
        		'port': 8080,
        		'debug': True,
        }
        ```

---
- 함수
    - 함수(Function)
        - 특정 작업을 수행하기 위한 재사용 가능한 코드 묶음
        
        함수를 사용하는 이유
        
        - 재사용성이 높아지고, 코드의 가독성과 유지보수성 향상
        
        함수 호출(function call)
        
        - 함수를 실행하기 위해 함수의 이름을 사용하여 해당 함수의 코드 블록을 실행하는 것
    - 함수 구조
        
        INPUT x → (Docstring + Function Body) → OUTPUT f(x) 
        
        함수 정의와 호출
        
        - 함수 정의(정의)
            - `def` 키워드로 시작
            - `def`키워드 이후 함수 이름 작성
            - 괄호 안에 함수에 전달되는 매개변수(parameter) 정의
        - 함수 body
            - `콜론 (:)` 다음에 들여쓰기 된 코드 블록
            - 함수가 실행될 때 수행되는 코드를 정의
        - Docstring
            - 함수 body 앞에 선택적으로 작성 가능한 함수 설명서
        - 함수 반환 값
            - 함수는 필요한 경우 결과를 반환 가능
            - `return` 키워드 이후 반환 값 명시
            - `return` 문은 함수의 실행 종료 후, 결과 호출 부분으로 반환
            - 함수 내에서 `return` 문이 없다면 `None` 이 반환
        - 함수 호출
            - 함수를 사용을 위해서는 호출이 필요
            - 함수의 이름과 소괄호를 활용해 호출
            - 필요한 경우 `인자(argument)` 를 전달
            - 호출 부분에서 전달된 인자는 함수 정의 시 작성한 매개변수에 대입
    - 함수와 반환 값
        - `print()` 함수는 화면에 값을 출력만, `반환(return)` 값이 없음
        - 파이썬에서 반환 값이 없는 함수는 기본적으로 None 반환 간주
            
            ```python
            return_value = print(1)
            print(return_value) # None
            def my_func():
            	print('hello')
            	
            result = my_func()
            	print(result) # None
            ```
            
    - 매개변수와 인자
        - 매개변수(parameter)
            - 함수를 정의할 때, 함수가 받을 값을 나타내는 변수
        - 인자(argument)
            - 함수를 호출할 때, 실제로 전달되는 값
            
            ```python
            def add_numbers(x, y): # x 와 y는 매개변수(parameter)
            		result = x + y
            		return result
            		
            	a = 2
            	b = 3
            	
            	sum_result = add_numbers(a, b) # a 와 b는 인자(argument)
            	print(sum_result)
            	
            ```
            
        - 다양한 인자 종류
            1. Positional Arguments(위치 인자)
                - 함수 호출 시 인자의 위치에 따라 전달되는 인자
                - 위치 인자는 함수 호출 시 반드시 값을 전달해야 함
                    
                    ```python
                    def greet(name, age):
                    		print(f'안녕하세요, {name}님! {age}살이시군요.')
                    greet('Alice', 25) # 안녕하세요, Alice님! 25살이시군요.
                    greet('Alice') # TypeError: greet() missing 1 required positional argument: 'age'
                    ```
                    
            2. Default Argument Values(기본 인자 값)
                - 함수 정의에서 매개변수에 기본 값을 할당
                - 함수 호출 시 인자를 전달하지 않으면, 기본값이 매개변수에 할당
                    
                    ```python
                    def greet(name, age=30):
                    		print(f'안녕하세요, {name}님! {age}살이시군요.')
                    greet('Alice') # 안녕하세요, Alice님! 30살이시군요.
                    ```
                    
            3. Keyword Arguments(키워드 인자)
                - 함수 호출 시 인자의 이름과 함께 값을 전달하는 인자
                - 매개변수와 인자를 일치시키지 않고, 특정 매개변수에 값 할당 가능
                - 인자의 순서는 중요하지 않고 이름을 명시하여 전달
                - 단, 호출 시 키워드 인자는 위치 인자 뒤에 위치
                    
                    ```python
                    def greet(name, age):
                    		print(f'안녕하세요, {name}님! {age}살이시군요.')
                    greet(name='Alice', age=25) # 안녕하세요, Alice님! 25살이시군요.
                    greet(age=35, name='Dave') # 안녕하세요, Dave님! 35살이시군요.
                    ---
                    greet(age=35, 'Dave') # positional argument follows keyword argument
                    ```
                    
            4. Arbitrary Arguments Lists(임의의 인자 목록)
                - 정해지지 않은 개수의 인자를 처리하는 인자
                - 함수 정의 시 매개변수 앞에 `'*'` 를 붙여 사용
                - 여러 개의 인자를 tuple로 처리
                    
                    ```python
                    def calculate_sum(*args):
                    		print(args) # (1, 100, 5000, 30)
                    		print(type(args)) # <class 'tuple'>
                    		
                    		calculate_sum(1,100,5000,30)
                    ```
                    
            5. Arbitrary Keyword Argument Lists(임의의 키워드 인자 목록)
                - 정해지지 않은 개수의 키워드 인자를 처리하는 인자
                - 함수 정의 시 매개변수 앞에 `'**'` 를 붙여 사용
                - 여러 개의 인자를 `dictionary` 로 묶어 처리
                    
                    ```python
                    def print_info(**kwargs):
                    		print(kwargs)
                    	
                    	print_info(name='Eve', age=30) # {'name': 'Eve', 'age': 30}
                    ```
                    
            
            함수 인자 권장 작성 순서
            
            - 위치 → 기본 → 가변 → 가변 키워드
            - 단, 모든 상황에 적용되는 절대적인 규칙 X, 상황에 따라 유연하게 조정
                
                ```python
                def func(pos1, pos2, default_arg='default', *args, **kwargs):
                		print('pos1':, pos1)
                		print('pos2:', pos2)
                		print('default_arg:', default_arg)
                		print('args:', args)
                		print('kwargs:', kwargs)
                		
                func(1, 2, 3, 4, 5, 6, key1='value1', key2='value2')
                
                """
                pos1: 1
                pos2: 2
                default_arg: 3
                args: (4,5,6)
                kwargs: {'key1': 'value1', 'key2': 'value2'}
                """
                ```
                
    - 재귀 함수
        
        재귀 함수
        
        - 함수 내부에서 자기 자신을 호출하는 함수
        - 재귀 함수 예시 - 팩토리얼
            - 재귀 호출의 결과를 이용하여 문제를 작은 단위로 분할
            - 분할된 문제들의 결과를 조합하여 최종 결과 도출
                
                ```python
                def factorial(n):
                		# 종료 조건: n이 0이면 1을 반환
                		if n == 0:
                				return 1
                		else:
                				# 재귀 호출: n과 n-1의 팩토리얼을 곱한 결과를 반환
                				return n * factorial(n-1)
                				
                # 팩토리얼 계산 예시
                print(factorial(5)) #120
                ```
                
            
        
        재귀 함수 특징
        
        - 특정 알고리즘 식을 표현할 때 변수의 사용이 줄어드며, 코드의 가독성이 높아짐
        - 1개 이상의 base case(종료되는 상황)가 존재하고, 수렴하도록 작성
        - 메모리 사용량이 많고 느림
        - 종료 조건이 잘못되면 `Stack Overflow` 에러 발생
        
        재귀 함수 활용 시 기억할 것
        
        - 종료 조건을 명확히 명시
        - 반복되는 호출이 종료 조건을 향하도록 할 것
        
        재귀 함수 사용 이유
        
        - 문제의 자연스러운 표현
            - 복잡한 문제를 간결하고 직관적으로 표현
        - 코드 간결성
            - 상황에 따라 반복문보다 알고리즘 코드가 더 간결하고 명확
        - 수학적 문제 해결
            - 수학적 정의가 재귀적으로 표현되는 경우(e.g.점화식), 직접적인 구현 가능
        
    - 내장 함수
        
        내장 함수(Built-in function)
        
        - 파이썬이 기본적으로 제공하는 함수(`import` 불필요)
            
            ```python
            numbers = [1, 2, 3, 4, 5]
            
            print(numbers) # [1, 2, 3, 4, 5]
            print(len(numbers)) # 5
            print(max(numbers)) # 5
            print(min(numbers)) # 1
            print(sum(numbers)) # 15
            print(sorted(numbers, reverse=True)) # [5, 4, 3, 2, 1]
            ```
            
    - 함수와 Scope
        
        Python의 범위(Scope)
        
        - 함수는 코드 내부에 `local scope` 를 생성, 그 외의 공간인 `global scope` 로 구분
        
        범위와 변수 관계
        
        - scope
            - global scope: 코드 어디에서든 참조할 수 있는 공간
            - local scope: 함수가 만든 scope(함수 내부에서만 참조 가능)
        - variable
            - gloabal variable: global scope에 정의된 변수
            - local variable: local scope에 정의된 변수
        
        Scope 예시
        
        ```python
        def func():
        		num = 20
        		print('local', num) # local 20
        
        func()
        
        print('global', num) # NameError: name 'num' is not defined
        ```
        
        변수 수명주기(lifecycle)
        
        - 변수 수명주기는 변수가 선언되는 위치와 scope에 따라 결정
        1. built-in scope
            - 파이썬이 실행된 이후부터 영원히 유지
        2. global scope
            - 모듈이 호출된 시점 이후 혹은 인터프리터가 끝날 때까지 유지
        3. local scope
            - 함수가 호출될 때 생성, 함수가 종료될 때까지 유지
        
        이름 검색 규칙(Name Resolution)
        
        - 파이썬에서 사용되는 이름(식별자)들은 특정 이름공간(namespace)에 저장
        - 아래와 같은 순서로 이름을 찾아 나가며, `LEGB Rule` 이라 부름
            1. Local scope: 지역 범위(현재 작업 중인 범위)
            2. Enclosed scope: 지역 범위 한 단계 위 범위
            3. Global scope: 최상단에 위치한 범위
            4. Built-in scope: 모든 것을 담고 있는 범위
                - 정의하지 않고 사용할 수 있는 모든 것)
        - 함수 내에서는 바깥 Scope의 변수에 접근 가능하나 수정은 불가
        
        LEGB Rule 예시
        
        - `sum` 이라는 이름을 global scope에서 사용해, 기존 built-in scope에 있던 내장함수 `sum` 을 사용하지 못하게 됨
            
            >> `sum` 을 참조 시 LEGB Rule에 따라 global에서 먼저 찾기 때문
            
            ```python
            print(sum) # <built-in function sum>
            print(sum(range(3))) # 3
            
            sum = 5
            
            print(sum) # 5
            print(sum(range(3))) # TypeError: 'int' object is not callble
            ```
            
            LEGB 퀴즈
            
            ```python
            x = 'G'
            y = 'G'
            
            def outer_func():
            		x = 'E'
            		y = 'E'
            		
            		def inner_func(y):
            				z = 'L'
            				print(x, y, z)  # E P L
            		
            		inner_func('P')
            		print(x, y) # E E
            outer_func()
            print(x, y) # G G 
            ```
            
        
        `'global'` 키워드
        
        - 변수의 스코프를 전역 범위로 지정하기 위해 사용
        - 일반적으로 함수 내에서 전역 변수를 수정하려는 경우에 사용
            
            ```python
            num = 0 # 전역 변수
            
            def increment():
            		global num # num를 전역 변수로 선언
            		num += 1
            
            print(num) # 0
            increment()
            print(num) # 1
            ```
            
        - `global` 키워드 선언 전에 참조 불가
            
            ```python
            num = 0
            def increment():
            		# SyntaxError: name 'num' is used
            		# prior to global declaration
            		print(num)
            		global(num)
            		num += 1
            ```
            
        - 매개변수에는 `global` 키워드 사용 불가
            
            ```python
            num = 0
            def increment(num):
            		# "num" is assigned before global
            		# declaraion
            		global num
            		num += 1
            ```
            
    - 함수 스타일 가이드
        
        함수 이름 작성 규칙
        
        기본 규칙
        
        - 소문자와 언더스코어 `(_)` 사용
        - 동사로 시작하여 함수의 동작 사용
        - 약어 사용 지양
            
            ```python
            # Good
            def calculate_total_price(price, tax):
            		return price + (price * tax)
            # Bad
            def calc_price(p, t):
            		return p + (p * t)
            ```
            
        
        함수 이름 구성 요소
        
        - 동사 + 명사
            - `save_user()`
        - 동사 + 형용사 + 명사
            - `calculate_total_price`
        - get/set 접두사
            - `get_username()` , `set_username()`
        
        단일 책임 원칙(Single Responsibility Principle)
        
        - 모든 객체는 하나의 명확한 목적과 책임만을 가져야 함
        
        함수 설계 원칙
        
        1. 명확한 목적
            - 함수는 한 가지 작업만 수행
            - 함수 이름으로 목적을 명확히 표현
        2. 책임 분리
            - 데이터 검증, 처리, 저장 등을 별도 함수로 분리
            - 각 함수는 독립적으로 동작 가능하도록 설계
        3. 유지보수성
            - 작은 단위의 함수로 나누어 관리
            - 코드 수정 시 영향 범위를 최소화
        
        ```python
        # Bad
        def process_user_data(user_data):
        		# 책임 1: 데이터 유효성 검사
        		if len(user_data['password']) < 8:
        				raise ValueError('비밀번호는 8자 이상이어야 합니다')
        
        		# 책임 2: 비밀번호 암호화 및 저장
        		user_data['password'] = hash_password(user_data['password'])
        		db.users.insert(user_data)
        		
        		# 책임 3: 이메일 발송
        		send_email(user_data['email'], '가입을 환영합니다!')
        
        # Good
        def validate_password(password):
        """비밀번호 유효성 검사"""
        		if len(password) < 8:
        				raise ValueError('비밀번호는 8자 이상이어야 합니다')
        
        def save_user(user_data):
        		"비밀번호 암호화 및 저장'
        		user_data['password'] = hash_password(user_data['password'])
        		db.users.insert(user_data)
        
        def send_welcome_email(email):
        		"환영 이메일 발송
        		send_email(email, '가입을 환영합니다!')
        
        # 메인 함수에서 순차적으로 실행
        def process_user_data(user_data):
        		validate_password(user_data['password'])
        		save_user(user_data)
        		send_welcome_email(user_data['email'])
        ```
        
    - Packing & UnPacking
        
        패킹(Packing) 
        
        - 여러 개의 데이터를 하나의 컬렉션으로 모아 담는 과정
        - 기본 원리
            - 여러 개의 값을 하나의 튜플로 묶는 파이썬의 기본 동작
            - 한 변수에 `콤마(,)` 로 구분된 값을 넣으면 자동으로 튜플로 처리
            
            ```python
            packed_values = 1, 2, 3, 4, 5
            print(packed_values) # (1, 2, 3, 4, 5)
            ```
            
        - `'*'` 을 활용한 패킹(함수 매개변수 작성 시)
            - 남는 위치 인자들을 튜플로 묶기
            - `*` 를 붙인 매개변수가 남는 위치 인자들을 모두 모아 하나의 튜플로 만듦
                
                ```python
                def my_func(*args):
                		print(args) # (1, 2, 3, 4, 5)
                		print(type(args)) # <class 'tuple'>
                
                my_func(1, 2, 3, 4, 5)
                ```
                
        - `'**'` 을 활용한 패킹(함수 매개변수 작성 시)
            - 남는 키워드 인자들을 `dictionary` 로 묶기
            - `**` 를 붙인 매개변수가 남는 키워드 인자들을 모두 모아 하나의 `dictionary` 만듦
                
                ```python
                def my_func2(**kargs):
                		print(kwargs) # {'a': 1, 'b': 2, 'c': 3}
                		print(type(kwargs)) # <class 'dict'>
                my_fucn2(a=1, b=2, c=3)
                ```
                
        
        ---
        
        언패킹(Unpacking)
        
        - 컬렉션에 담겨있는 데이터들을 개별 요소로 펼쳐놓는 과정
        - 기본원리
            - 튜플이나 리스트 등의 객체의 요소들을 개별 변수에 할당
            - ‘시퀀스 언패킹(Sequence Unpacking)’ 또는 ‘다중 할당(Multiple Assignment)’ 라고 부름
                
                ```python
                packed_values = 1, 2, 3, 4, 5
                # (1, 2, 3, 4, 5) 튜플의 각 요소들이
                # a, b, c, d, e 변수에 순서대로 '언패킹'되어 할당
                a, b, c, d, e = packed_values
                print(a, b, c, d, e) # 1 2 3 4 5
                ```
                
            - `'*'` 을 활용한 패킹(함수 인자 전달)
                - 리스트나 튜플 앞에 `*` 를 붙여 각 요소를 함수의 개별 위치 인자로 전달
                    
                    ```python
                    def my_function(x, y, z):
                    		print(x, y, z)
                    
                    names = ['alice', 'jane', 'valo']
                    my_function(*names) # alice jane valo
                    ```
                    
            - `'**'` 을 활용한 언패킹(딕셔너리 → 함수 키워드 인자)
                - 딕셔너리 앞에 `**` 를 붙여 `{키:값}` 쌍 형태의 키워드 인자로 전달
                    
                    ```python
                    def my_function(x, y, z):
                    		print(x, y, z)
                    
                    my_dict = {'x' : 1, 'y': 2, 'z': 3}
                    my_function(**my_dict) # 1 2 3
                    ```
                    
        
        ---
        
        Packing & Unpacking 정리
        
        | 구분 | 상황 | `*` 연산자 | `**` 연산자 |
        | --- | --- | --- | --- |
        | 패킹 | 함수 정의 시 | 여러 위치 인자를 하나의 튜플로 받음 | 여러 키워드 인자를 하나의 딕셔너리로 받음 |
        | 언패킹 | 함수 호출 시 | 리스트/튜플을 개별 위치인자로 전달 | 딕셔너리를 개별 키워드 인자로 전달 |
    - 참고
        
        함수와 반환
        
        함수의 return, 반환의 원칙
        
        - 파이썬 함수는 언제나 단 하나의 값(객체)만 반환 가능
        - 여러 값을 반환하는 경우에도 하나의 튜플로 패킹하여 반환
            
            ```python
            def get_user_info():
            		name = 'Alice'
            		age = 30
            		# 콤마(,)로 반환하는 것처럼 보임
            		return name, age
            
            # 반환된 값을 user_data 변수에 담아 확인해보면
            user_data = get_user_info()
            
            # 단 하나의 튜플을 반환하는 것
            print(user_data_ # ('Alice', 30)
            ```
            
        
        람다 표현식(Lambda Expressions)
        
        - 익명 함수를 만드는 데 사용되는 표현식
        - 한 줄로 간단한 함수를 정의
        
        람다 표현식 구조
        
        - lambda 키워드
            - 람다 함수를 선언하기 위해 사용하는 키워드
        - 매개 변수
            - 함수에 전달되는 매개변수들
            - 여러 개의 매개변수가 있을 경우 쉼표로 구분
        - 표현식
            - 함수의 실행되는 코드 블록으로, 결과값을 반환하는 표현식으로 작성
        
        람다 표현식 예시
        
        - 간단한 연산이나 함수를 한 줄로 표현할 때 사용
        - 함수를 매개변수로 전달하는 경우에도 유용하게 활용
            
            ```python
            def addition(x, y):
            		return x + y
            >>>
            lambda x, y : x + y
            
            def addition(x, y):
            		return x + y
            		
            result = addition(3, 5)
            print(result) # 8
            >>>
            addition = lambda x, y: x + y
            result = addition(3, 5)
            print(result) # 8
            ```
            
        - 람다 표현식 활용(with map 함수)
            
            ```python
            numbers = [1, 2, 3, 4, 5]
            
            def square(x):
            		return x**2
            
            # lambda 미사용
            squared1 = list(map(square,numbers))
            print(squared1) # [1, 4, 9, 16, 25]
            
            # lambda 사용
            squared2 = list(map(lambda x: x**2, numbers))
            print(squared2) # [1, 4, 9, 16, 25]
            ```