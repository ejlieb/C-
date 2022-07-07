# C++ Topic 5. 자료형

8bits = 1byte



1. Character Type

- char - At least 8 bits
- char16_t - At least 16 bits
- char_32_t - At least 32 bits
- wchar_t - can represent the largerst supported character set.



2. Integer types(signed) 괄호안은 생략가능

- signed char - At least 8 bits, char이 내부적으로 정수 형태로 저장되기 때문에 integer type에서도 사용되나 나중에 int로 변환해야 됌, 가장 작음
- (signed) short (int) - At least 16 bits
- (signed) int - At least 16 bits
- (signed) long (int) - At least 32 bits
- (signed) short (int) - At least 16 bits
- (signed) long long (int) -At least 64bits

3. Floating-point types

- float
- double
- long double

 	4. Boolean type

- bool

5. void type

- void

6. Null pointer

- decltype

7. unsinged Integer types(음의 정수가 포함이 안된다. 0은 포함 그러나 특정 연산에서 signed가 더 빠를 때가 있음)

signed와 같으나 unsinged를 앞에 붙인다.

ex) unsigned int

