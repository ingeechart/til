Deque
======
Deque는 Double ended queue 로서 큐의 양끝에서 삽입삭제가 일어나는 것을 의미한다.
이것은 벡터와 비슷하지만, 양끝에서 삽입삭제가 일어날 때 더 효율적이다. Deque는 vector와 달리 연속적인 스토리지 할당은 보장되지 않을 수도 있다.

deque는 list를 이용하여 구현하였다. (여기서는 initializer_list 를 사용하였는데 클래스 안에서 각종 멤버변수나 객체, 상속받은 클래스의 맴버변수등을 초기화 시킬때 사용하는것)<br>
<br>
## Declaration
~~~
#include <deque>

deque<자료형> 객체이름;
ex) deque<int> dq;

~~~
<br>


## Functions
1. **Iterator**<br>
 begin()<br>
 end() <br>
2. **capacity**<br>
 size()<br>
 max_size()<br>
 >현재 deque가 할당받고 있는 전체 size를 반환
 
 resize()<br>
 empty()<br>
 shrink_to_fit()<br>
 빈 공간을 다 지운다.

3. **Element access**<br>
[i]<br>
i번째 원소 access<br
at(i)<br>
i 번쨰 원소 반환 <br>
front()<br>
back()<br>
4. **Modifiers**<br>
 assign()<br>
 push_back(data)<br>
push_front(data)<br>
pop_back()<br>
pop_front()<br>
insert( iterator , value)<br>
특정위치에 원소 삽입<br>
erase(iterator)<br>
특정위치의 값을 지움<br>
erase(iterator , iterator) 하면 범위로 지울 수 있다.<br>
swap()<br>
  두 deque 사이 data 교환
clear()<br>
  deque 에 있는 모든 원소를 지운다.
emplace()<br>
emplace_front()<br>
emplace_back()<br>
