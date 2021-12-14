<div align="right">
  <a href="https://github.com/BoostUpStudy/MySmallDataStructure">
      <img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https://github.com/BoostUpStudy/MySmallDataStructure&count_bg=%233D61C8&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false"/></a>
</div>

# MySmallDataStructure
자료구조 내용을 짧은 시간 내에 빠르게 정리할 수 있도록 하기 위한 레포지토리입니다!

<br/>

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

## Table

- [재귀](#재귀)
- [링크드리스트](#링크드리스트)
- [스택](#스택)
- [큐](#큐)
- [힙](#힙)
- [우선순위큐](#우선순위큐)

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

## 힙
- 트리 형태로 쌓인 데이터를 의미한다.
- `최댓값(Max-Heap)`이나 `최솟값(Min-Heap)`을 빠르게 찾기 위해 만들어진 `완전이진트리` 형태의 자료구조이다.
- 꼭지점에 위치한 값들을 확인하는데 걸리는 시간은 단 `O(1)`이다.
- 힙에 요소를 `삽입(reHeapUp)`하거나 `제거(reHeapDown)`할 때 걸리는 시간은 `O(logN)`이다. (단 제거는 반드시 꼭지점에서만 이루어진다.)
- 일반적으로 `배열`을 이용해서 Heap을 구현한다. (`Linked List`의 경우 요소를 찾기 위해 순회하는 과정이 필요하지만 `Array`는 인덱스를 이용하면 바로 찾을 수 있기 때문이다.)

<br />

## 우선순위큐
- 데이터에 우선순위를 부여하여 들어간 순서와 관계없이 우선순위가 높은 데이터를 추출하기 위한 자료구조이다.
- 일반적으로 가장 효율적인 `Heap`을 이용하여 우선순위큐를 만든다. (다른 자료구조로도 만들 수 있다!!) 
- 다른 자료구조로 만든 우선순위큐는 데이터의 삽입과 삭제에 최악의 경우 `O(N)`이 걸리지만, 오직 Heap만이 최악의 경우에도 `O(logN)`이 걸린다.

<br />
