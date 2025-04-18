# ✔️ 이진탐색트리(Binary Search Tree)

## 트리를 정의해보세요.
트리는 사이클이 없고, 모든 정점이 간선으로 연결된 자료구조입니다.
사이클이 없어야 하기 때문에 간선의 개수는 항상 정점의 개수보다 하나 적습니다.

<br>

## 이진트리를 탐색하는 세가지 방법에 대해서 설명해 보세요.
전위순회, 중위순회, 후위순회 세가지 방법으로 탐색할 수 있습니다.<br>
전위 순회는 부모노드를 먼저 체크하고 자녀 노드의 서브트리를 체크합니다.
중위 순회는 좌측 자녀노드의 서브트리를 체크하고 더 이상 탐색이 불가능 할 때 부모 노드를 체크한 뒤 우측 자녀노드의 서브트리를 탐색합니다.
후위 순회는 좌측 서브트리, 우측 버스트리를 모두 체크한 뒤에 부모 노드를 체크합니다.

<br>

## 완전이진트리를 설명해 보세요.
완전이진트리는 최대 두 개의 자녀노드를 가지는 이진트리로 마지막 레벨을 제외한 모든 레벨에 노드가 채워져있고, 
마지막 레벨은 왼쪽부터 빈 노드 없이 채워져 있어야 합니다.

<br>

## 이진탐색트리를 설명해 보세요.
이진탐색트리는 정렬된 트리입니다.<br>
어느 노드를 선택하든 해당 노드의 좌측 서브트리에는 그 노드보다 작은 값을 지닌 노드들로만 이루어져 있고,
우측 서브트리에는 그 노드의 값보다 큰 값을 지닌 노드들로만 이루어져 있는 이진 트리입니다.

<br>

## 이진탐색트리의 삭제 연산을 설명해 보세요.
이진탐색트리에서 노드를 삭제하기 위해서는 세 가지 경우를 고려해야 합니다.<br>
첫째, 삭제하려는 노드의 자녀 노드가 없는 경우에는 제거 대상을 탐색해 제거하면 됩니다.<br>
둘째, 제거 대상이 하나의 자녀 노드를 가지는 경우에는 제거 대상의 자녀노드를 제거 대상의 부모 노드와 연결한 뒤에 제거합니다.<br>
마지막으로, 제거 대상이 두 개의 자녀 노드를 가지는 경우입니다.
이 경우는 삭제하려는 노드의 자녀 서브트리에서 좌측을 사용한다면 최댓값을, 
우측을 사용한다면 최솟값을 제거 대상의 자리에 대체하고 해당 자녀 노드를 삭제합니다.

<br>

## 이진탐색트리의 삽입 연산을 설명해 보세요.
새로운 노드의 값을 기준으로 더 이상 자녀노드가 없을 때까지 탐색을 진행하다가 마지막 노드의 자녀 노드로 새로운 노드를 연결짓습니다.

<br>

## 이진탐색트리 연산의 시간복잡도를 설명해 보세요.
삽입과 삭제 모두 탐색 연산을 사용해야 하고, 탐색은 각 노드를 대소비교하며 진행하기 때문에 트리의 높이만큼의 시간이 요구됩니다.
즉, n개의 노드에 대해서 O(log N)의 시간복잡도를 갖습니다.

<br>

## 이진탐색트리의 worst case와 해결 방법에 대해 설명해 보세요.
완전히 편향된 트리에서는 모든 노드를 전부 탐색해야 하기 때문에 O(n)의 시간복잡도가 발생합니다.<br>
이를 해결하기 위해서는 스스로 균형을 맞추는 트리 구조를 사용해야 하며 AVL 트리, Red-Black 트리 등이 있습니다.

<br>

## AVL 트리에 대해서 설명해 보세요.
트리의 블균형을 막기 위한 트리 구조 중 하나로,
새로운 노드가 트리에 추가될 때마다 좌측 서브트리의 높이와 우측 서브트리의 높이의 차를 사용해 균형을 맞추는 트리입니다.

<br>

## AVL 트리의 시간복잡도를 이진탐색트리와 비교해 보세요.
AVL 트리는 이진탐색트리와 달리 트리의 재조정을 통해 균형을 유지하기 때문에 항상 O(log N)의 시간복잡도를 갖습니다.

<br>

## Red-Black 트리가 가지는 특징을 말해보세요.
다음의 다섯 가지 조건을 만족하는 트리를 레드-블랙 트리라고 합니다.<br>
- 모든 노드는 레드 혹은 블랙이다.
- 루트 노드는 항상 블랙이어야 한다.
- 리프 노드는 항상 블랙이어야 한다.
- 레드 노드의 자녀 노드는 항상 블랙이어야 한다. 즉, 연속된 레드 노드는 있을 수 없다.
- 루트 노드에서 어떤 리프노드까지의 경로에 있는 블랙 노드의 수는 모두 동일하다.

<br>

## 레드-블랙 트리의 삽입과정을 설명해 보세요.
새로운 노드 값을 기준으로 더 이상 갈 수 있는 자녀노드가 없는 노드까지 이동한 뒤 새로운 노드를 레드로 설정해 추가합니다.
이후 레드-블랙 트리의 규칙에 따라 트리를 재조정합니다.<br>
1. 부모가 블랙이면 아무 조정 하지 않고 삽입을 완료합니다.
2. 부모가 레드면 다시 세가지 경우로 나누어 재조정합니다. 부모의 형제노드를 삼촌노드라고 했을 때,
   - 삼촌도 레드면 부모와 삼촌을 블랙으로, 조부모를 레드로 변경한 뒤 조부모를 대상으로 재조정합니다.
   - 삼촌 노드가 블랙, 방향이 삼각형 형태면 부모를 기준으로 회정하여 일직선으로 바꾼 뒤 재조정합니다.
   - 삼촌 노드가 블랙, 방향이 일직선 형태면 부모를 블랙, 조부모를 레드로 변경한 뒤 조부모를 기준으로 회전합니다.
3. 마지막으로 루트를 블랙으로 변경한 뒤 마무리합니다.

<br>

## AVL트리와 레드블랙트리를 비교해 보세요.

| | 레드블랙트리 | AVL 트리 |
| - | --- | ---- |
| 이진탐색트리 | Yes | Yes |
| 삽입/삭제/탐색 시간복잡도 | worst case에서도 O(log N) | worst case에서도 O(log N) |
| 삽입/삭제 성능 | 빠른 편 | 느린 편 |
| 검색 성능 | 느린 편 | 빠른 편 |
| 균형을 잡는 방식 | 레드블랙 속성을 만족시키도록 | balance factor가 {-1, 0, 1}에 속하도록 |
| 응용 사례 | 리눅스 커널 내부, 자바 TreeMap, C++의 std::map | dictionary, 한 번 만들어 두고 삽입 삭제는 적고, 탐색이 대부분인 상황에서 사용 |
