<div align="right">
  <a href="https://github.com/BoostUpStudy/MySmallDataStructure">
      <img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https://github.com/BoostUpStudy/MySmallDataStructure&count_bg=%233D61C8&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false"/></a>
</div>

# MySmallDataStructure
자료구조 내용을 짧은 시간 내에 빠르게 정리할 수 있도록 하기 위한 레포지토리입니다!

**최신 업데이트 날짜 : `2021.12.16`**

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
- [해시](#해시)
- [그래프](#그래프)
- [트리](#트리)
- [이진트리](#이진트리)
- [이진탐색트리](#이진탐색트리)

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

## 해시
- 인덱스에 해시값을 사용하는 자료구조이다.
- 인덱스에 해시값을 넣으면 데이터를 바로 찾을 수 있기 때문에 일반적인 경우 검색 속도가 O(1)이다.
- 해시값은 특정한 해시함수를 통해 생성된다.
- 해시값의 충돌을 피하기 위해 별도의 방법을 사용해서 다른 칸에 데이터를 넣는 `Open addressing` 방식과 해당 칸의 크기를 수평적으로 늘리는 `Seperate Chaining` 방식이 존재한다.

<br />

## 그래프
- 여러 노드(혹은 Vertex)들이 서로 다양하게 연결되어 있는 것을 표현하는 자료구조이다.
- 양방향과 단방향 그래프가 존재할 수 있고, 가중치가 존재할 수 있다.
- `2차원 Array` 형태로 표현할 수도 있고, `Array`와 `Linked List`를 이용할 수도 있다.
- 숫자가 아닌 데이터를 담은 그래프를 표현하기 위해 `1차원 array` 형태로 데이터를 넣어둔 후 숫자로 치환해서 인덱스로 사용할 수 있다.

## 트리
- 계층적인 자료를 표현할 때 사용하는 자료구조이다.
- 하나의 트리는 여러 서브트리로 구성될 수 있다.
- 자식 노드가 없는 노드를 `단말 노드(leaf node)`, 자식 노드가 있는 노드를 `비단말 노드(internal node)`라고 부른다.
- 트리의 높이는 해당 트리의 최대 레벨을 의미한다.

<br />

## 이진트리
- 0~2개의 자식 노드를 가지는 트리 자료구조를 이진 트리라고 부른다.
- 트리 중 가장 흔하게 쓰이는 트리로, 각각의 서브트리도 이진 트리로 구성된다.
- 왼쪽과 오른쪽으로 구분될 수 있기 때문에 서브트리간 순서도 의미가 있을 수 있다. (순회에서 사용된다)
- 이진 트리는 형태에 따라 `포화 이진 트리(full binary tree)`와 `완전 이진 트리(complete binary tree)`로 구분될 수 있다. (포화 이진 트리 ⊂ 완전 이진 트리 ⊂ 일반 이진 트리)
- 필요에 따라 `Preorder(전위 순회)`, `Inorder(중위 순회)`, `Postorder(후위 순회)`, `Level-order(레벨 순회)` 방식으로 순회할 수 있다.

<br />

## 이진탐색트리
- 오름차순으로 정렬되어 있는 이진 트리를 의미한다.
- 각각의 하위 트리들도 이진 탐색 트리이다.
- 중복된 키는 허용하지 않는다.
- 요소를 찾고, 삽입하고, 삭제하는데에 `O(logN)`이 걸린다.

<br />
