<div align="right">
  <a href="https://github.com/BoostUpStudy/MySmallDataStructure">
      <img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https://github.com/BoostUpStudy/MySmallDataStructure&count_bg=%233D61C8&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false"/></a>
</div>

# MySmallDataStructure
자료구조 내용을 짧은 시간 내에 빠르게 정리할 수 있도록 하기 위한 레포지토리입니다!

## Table

- [작성자](#작성자)
- [재귀](#재귀)
- [링크드리스트](#링크드리스트)
- [스택](#스택)
- [큐](#큐)


## 작성자

<div>
  <table align="center">
    <tr>
      <td>  
        <a href="https://github.com/alittlekitten">
          <img src="https://avatars.githubusercontent.com/alittlekitten" width="100"/>
        </a>
      </td>
    </tr>
    <tr>
      <td align="center">
        <a href="https://github.com/alittlekitten">
          alittlekitten
        </a>
      </td>
    </tr>
  </table>
</div>

<br/>

## 재귀
- 자기 자신을 호출하는 것을 의미한다.
- `General case`일 때 자기 자신을 호출하고 `Base case`일 때 함수가 종료된다.
- `Base case`를 향해 접근해야 재귀함수가 정상적으로 종료될 수 있다.
- `Recursion`으로 표현할 수 있는 내용은 `Iteration(for문, while문)`으로도 표현할 수 있다.

<br />

## 링크드리스트
- `Data Field`와 `Link Field`로 나뉘고, 두 Field를 합쳐서 `Node Vertex`라고 부른다.
- 요소를 추가하고 삭제할 때 데이터의 위치를 변경하지 않아도 된다.
- `Singly Linked List(단일 연결 리스트)`는 뒤로 돌아가지 못하기 때문에 이 단점을 해결하기 위해 `Doubly Linked List(이중 연결 리스트)`와 `Circular Linked List(원형 연결 리스트)`가 등장했다.
- `Doubly Linked List`는 오늘날 Linked List의 대부분을 차지하고 있고, 뒤로 이동하면서 탐색이 가능하지만 추가적인 메모리가 필요하다.
- `Circular Linked List`는 `Singly Linked List`에서 맨 뒤와 맨 앞을 연결만 하면 되기 때문에 구현하기 쉽지만 한칸 뒤로 이동하기 위해 모든 요소를 돌아야 하는 단점이 있다.

<br />

## 스택
- `LIFO(Last In First Out)` 특성을 가지는 자료구조이다.
- 스택 안에 요소를 넣는 작업을 `Push`, 요소를 빼는 작업을 `Pop`이라고 부르고, 두 작업 모두 O(1)시간이 걸린다.
- 실행취소, 혹은 재귀함수의 실행에 스택이 사용된다.
- 기본적으로 크기가 정해져있고, 빈 스택에서 무언가를 빼내려 하면 `StackUnderflow`가 발생하고, 꽉 찬 스택에 무언가를 넣으려 하면 `StackOverflow`가 발생한다.

<br />

## 큐
- `FIFO(First In First Out)` 특성을 가지는 자료구조이다.
- 스택 안에 요소를 넣는 작업을 `Enqueue`, 요소를 빼는 작업을 `Dequeue`라고 부르고, 두 작업 모두 O(1)시간이 걸린다.
- 들어온 순서대로 작업이 실행되어야 하는 경우에 큐가 사용된다.
- 기본적으로 크기가 정해져있고, 빈 큐에서 무언가를 빼내려 하면 `QueueUnderflow`가 발생하고, 꽉찬 큐에 무언가를 넣으려 하면 `QueueOverflow`가 발생한다.
- 스택과는 다르게 메모리 사용 문제때문에 원형으로 많이 사용한다. 이 때 맨 앞과 맨 뒤의 구분을 위해 Reserved 공간을 마련해두어야 한다.

<br />
