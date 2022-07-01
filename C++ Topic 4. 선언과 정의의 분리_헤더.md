## C++ Topic 4. 선언과 정의의 분리, 헤더

컴파일러는 기본적으로 위에서부터 코드를 읽는다.

```c++
#include <iostream>

using namespace std;

int main()
{
    cout << add(1, 2) << endl;
}

int add(int a, int b)
{
    return a + b;
}
```

이런식으로 하면 에러가 발생한다. 왜냐하면 main을 읽을 때 add를 모르기 때문이다.



하지만 전체 함수를 main위로 올리지 말고 add가 무엇인지(입,출력이 무엇인지를 알려준다면) 가능하다 ==> 이것을 프로토타입이라고 한다.

ex)

```c++
#include <iostream>

using namespace std;

int add(int a, int b); // forward declaration(전방선언)
int main()
{
    cout << add(1, 2) << endl;
}

// definition 정의
int add(int a, int b)
{
    return a + b;
}
```



이런식으로 선언과 정의가 분리되어 선언을 앞에서 하고 뒤에서 정의 가능하다.

---

#### 헤더와 파일 쪼개기

쪼개진 .cpp 파일들을 항상 선언하기 보다는 헤더파일에 모아놓고 include시킨다.



ex)

main.cpp

```c++
#include <iostream>
#include "add.h"

using namespace std;
int main()
{
    cout << add(1, 2) << endl;
    
    return 0;
}
```

add.cpp

```c++
int add(int a, int b)
{
    return a + b;
}
```

add.h(헤더파일)

```c++

int add(int a, int b);
```

---

#### 





