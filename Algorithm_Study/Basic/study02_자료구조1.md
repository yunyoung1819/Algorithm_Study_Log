# 자료구조1 (스택)


### 스택 (Stack)

- 한쪽 끝에서만 자료를 넣고 뺄 수 있는 자료구조
- 마지막으로 넣은 것이 가장 먼저 나오기 때문에 Last In First Out(LIFO)라고도 한다.
- push: 스택에 자료를 넣는 연산
- pop: 스택에서 자료를 빼는 연산
- top: 스택의 가장 위에 있는 자료를 보는 연산
- empty: 스택이 비어있는지 아닌지를 알아보는 연산
- size: 스택에 저장되어있는 자료의 개수를 알아보는 연산 


#### 스택의 구현

- 일차원 배열 하나로 구현할 수 있다.

```
int stack[10000];
int size = 0;   // 스택의 크기 size:5 (0~4번까지)

```

```
void push(int data) {
    stack[size] = data;
    size += 1;
}

```

```
int pop() {
    stack[size-1] = 0;
    size -= 1;
}
```

```
bool empty() {
    if (size == 0) {
        return true;
    } else {
        return false;
    }
}
```

```
int top() {
    if (empty()) {
        return -1;
    } else {
        return data[size-1];
    }
}
```


#### 스택을 이용한 문제

#### 단어 뒤집기 

- 단어 뒤집기 (https://www.acmicpc.net/problem/9093)

#### 괄호 

- 괄호 (https://www.acmicpc.net/problem/9012)
- 스택을 사용해서 올바른 괄호 문자열인지 아닌지를 알 수 있다.
- (가 나오면 스택에 (를 넣고
- )가 나오면 스택에서 하나를 빼서 (인지 확인한다.
- 또는 하나를 뺼 수 있는지를 확인한다. 


#### 스택 수열 

- 스택 수열 (https://www.acmicpc.net/problem/1874)
- 1부터 N까지의 수를 스택에 넣었다가 뽑아 놓음으로 하나의 수열을 만들 수 있다.
- push 하는 순서는 오름차순이다.
- 임의의 수열 A가 있을 때, 스택을 이용해 이 수열을 만들 수 있는지 없는지 구하는 문제
- A=[4,3,6,8,7,5,2,1] 이라면 ++++--++-++-----를 이용해서 만들 수 있다.


#### 에디터

- 에디터 문제 (https://www.acmicpc.net/problem/1406)