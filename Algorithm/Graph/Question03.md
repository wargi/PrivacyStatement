# 파티

## 1. 문제
- 철수네 마을에는 N개의 집이 있으며, 각 집은 고유한 번호를 부여받는다.
- 각 번호는 1보다 크거나 같고, N보다 작거나 같다.
- 철수는 마을 K에 살고 있다.
- 집과 집 사이에는 단방향 도로가 존재하기 때문에, 이 도로를 통하여 서로 이동할 수 있다.
- 즉, N개의 마을은 그래프 구조를 이룬다.
- 편의상 각 집에는 한 사람만이 살고 있다고 가정하자.
- 크리스마스인 오늘, 철수는 본인의 집에서 파티를 열려고 한다.
- 따라서 다른 모든 사람들이 철수의 집에 모여 파티를 즐기고, 파티가 끝난 후에는 다시 본인의 집으로 돌아가려 한다.
- 사람들은 본인의 집에서 철수네 집까지 이동하기 위하여 항상 최단거리로 이동하기를 원하고, 마찬가지로 철수네 집에서 본인의 집에 갈 때도 최단거리로 이동하기를 원한다.
- 집의 개수와 두 집을 잇는 단방향 도로의 정보, 그리고 철수의 집 번호가 주어질 때, 마을 사람들이 파티를 즐기기 위해서 이동해야 하는 총 거리의 합을 출력하는 프로그램을 작성하시오.

## 2. 입력

- 첫째 줄에 정점의 개수 N과 간선의 개수 M, 그리고 철수의 집 번호 K가 주어진다.
- ( 1 ≤ N, K ≤ 1,000, 1 ≤ M ≤ 100,000 ) 둘째 줄부터 간선의 정보가 주어진다.
- 각 줄은 두 개의 숫자 a, b, c로 이루어져 있으며, 이는 정점 a에서 정점 b로 이동하는 데 시간이 c만큼 걸린다는 의미이다.
- 양방향 도로가 아님에 주의하자. 각 정점의 번호는 1번부터 N번까지이다.

## 3. 출력
- 마을 사람들이 파티를 즐기기 위해서 이동해야 하는 총 거리의 합을 출력한다.

## 4. 예제 입력
```
6 10 3
1 2 1
2 5 2
3 1 5
3 2 3
3 4 1
3 6 4
4 1 1
5 3 1
6 5 3
6 4 2
```

## 5. 예제 출력
```
32
```

## 6. 코드

```c++

```
