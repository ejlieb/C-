## C++ Topic 3. C++의 구조

```c++
int main(void)
{
    return 0;
}
```

의 구조가 기본!

python과 다르게 세미콜론을 사용!!



##### C++ ==> 메모리!!!!!!! 중요하게 생각해야된다.





#### 변수

데이터 타입과 함께 선언해준다.

```c++
int main()
{
    int x = 123; // initialization
    x = 123; // assignment
    std:cout << x << std:endl;
    return 0;
}
```

assignment와 initialization을 분명하게 구분해야한다!!

초기화 매우 중요!!

---

#### 입출력 스트림

```c++
#include <iostream> // cout, cin, endl, ...
```

우선 사용하려면 include를 해야한다



##### 출력

```c++
int main() {
    std::cout << "내가 출력하고자 하는 문자열" << std::endl; // std라는 네임스페이스 안에 있는 cout
   
    return 0;
}
```



```c++
int main() {
    int x = 1024;
    std::cout << "I love this";
    std::cout << "x is" << x << std::endl;
}
```

위와 같은 경우 줄은 바뀌었지만 출력 자체는 다 붙어서 출력 된다.

`I love thisx is1024`



`\t` : 출력할 때 공백을 두고 줄맞춤을 할때 사용

`\n` : 줄바꿈



```c++
int main() {
    using namespace std;
    int x = 1024;
    cout << "I love this";
    cout << "x is" << x << endl;
}
```

이런식으로 using을 사용하면 그 중괄호 영역 안에서는 std:: 생략 가능

컴파일러가 알아서 그 네임스페이스로 찾아서 컴파일 해준다.

##### 입력(python input과 비슷)

```c++
int main() {
    using namespace std;
    
    int x;
    cin >> x;
    
    cout << "YOur input is " << x << endl;
}
```

---

#### 함수



##### 기본적인 함수구조

```c++
int addTwoNumbers(int num_a, int num_b) 
{
    int sum = num_a + num_b;
    return sum
}
```

함수는 메모리에 저장되어 있고, 메모리에 저장되 있는 함수를 가져옴



만약 함수를 호출한다면

```c++
int main()
{
    cout << multiplyTwoNumbers(1,2) << endl;
}
```

함수를 호출할 때 함수의 매개변수(parameter)로 들어오는 argument들을  통해 함수 안에 int num_a와 num_b가 최가화 됌





##### TIP : 이름짓기

1. 숫자로 시작하지 않는다.
2. 세미콜론 등으로 시작하지 않는다.
3. 단어는 기본적으로 Camel case or Pascal Case
   - ex) startProject, StartProject
4. 클래스나 구조체 같은 Type Name은 Pascal Case
5. 함수의 인자와 변수명은 Snake Case
6. 함수는 보통 Pascal Case
7. const, constexpr이 쓰이는 상수들은 보통 Camel Case를 따르되 앞자리에 접두어 k

---

#### 지역범위(Scope)



기본적으로 함수안에서 정의된 변수는 함수 안에서만 존재한다.

{} 중괄호를 기준으로 영역을 분리(scope가 다르다)



ex)

```c++
int main()
{
    int x = 0;
    {
        int x = 1;
    }
}
```

이런식으로 중괄호 하나를 하나의 스코프로 잡기 때문에 가능하다.

두 x의 메모리 주소값도 다르고 값도 다르다.



##### 지역변수는 기본적으로 영역을 벗어나면 사용할 수 없다. 지역변수가 차지하고 있던 메모리는 지역 변수가 영역을 벗어날 때 스택 메모리로 반납된다. 반납된 메모리는 다음 지역 변수가 사용할 수 있도록 대기한다.

