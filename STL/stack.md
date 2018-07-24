std::stack
=====

LIFO(last in first out)의 방식으로 data를 저장한다.<bv>
stack을 직접 구현하는 경우 linkedlist 나 배열을 이용한 방법을 많이 사용한다.

간단하게 비교해보면<br>
linkedlist를 사용한경우 속도가 느리지만 stack의 크기가 가변적이라는 장점이 있다.<br>
array를 사용한 경우에는 속도는 빠르지만 stack의 크기가 고정적이다.  

cpp STL 에서는 stack을 vector를 사용함으로써 구현했다.

<br>

### Declaration

```
  #include <stack>

  stack<자료형> 객체이름;
  ex) stack<int> s;
```

<br>


<!--나중에 예제코드 넣어주면 아주좋을듯-->


### Fucntions
  1. **empty()**<br>
    if stack is empty return 1

  2. **size()**<br>
    return  the size of stack(length of stack)

  3. **top**<br>
    return last element of stack

  4. **push(value)**<br>
    insert element at end<br>
    (vector 를 사용하기 떄문에 end 라는 표현을 썻지만 우리가 생각하는 그림에서는 top에 insert하는겁니다.)

  5. **pop()**<br>
    erase last element<br>
    따로 값을 리턴하는것이 아닌 그냥 top에 있는 값을 지우는 것.

  6. **swap( stack_name )**<br>
     exchange contents with ( stack_name )<br>
     두 stack 의 data를 교환한다(개수 상관없이 이름이 바뀐다고 생각하면 쉽다).<br>

  7. **emplace()**<br>
    insert element at beginning (construct element in-place at the top)<br>
    emplace 계열 함수는 객체 생성자의 인자들을 넘겨, 컨테이너 내부에서 생성후 추가하는 방식을 사용한다.<br>
    따라서 <u>임시객체를 아예 생기지 않게 하거나</u>, <u>그 횟수를 줄일 수 있다</u>.<br>
    여기서 at beginning 의 의미는 stack 앞에 가 아닌 애초에 임시객체를 생성하지 않고 넣겠다. 라는 뜻같다.

<br>

### Operation
```
  1. ==
  2. !=
  3. <
  4. <=
  5. >
  6. >=


```
<br>




## 참고자료<br>
>http://www.cplusplus.com/reference/stack/stack/<br>
>https://www.geeksforgeeks.org/stack-in-cpp-stl/<br>
>https://ru.cppreference.com/w/cpp/container/stack<br>
