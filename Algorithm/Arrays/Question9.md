# Array 2 #

## 1. 문제
- N*M의 2차원 배열이 주어지고, 주어진 2차원 배열에는 어떠한 값이 있는지 출력하는 프로그램을 작성해보자.

## 2. 입력
- 첫째 줄: 자연수 행의 개수 N,열의 개수 M이 주어진다. ( 1 <= N, M <= 100 )
- 둘째 줄: N*M의 배열이 주어지고, 마지막 줄에는 A,B가 주어진다. ( 0 <= A < N, 0 <= B < M )

## 3. 출력
- 첫째 줄에 N*M배열의 값을 출력한다.

## 4. 예제 입력
```
3 4
1 2 3 4
5 6 7 8
9 10 11 12
1 1
```

## 5. 예제 출력
```
6
```

## 6. 예제 입력

```
4 3
1 2 3
4 5 6
7 8 9
10 11 12
3 2
```

## 7. 예제 출력

```
12
```

## 8. 코드

```c++
#include <stdio.h>

int main() {
  int n, m, a, b, i, j;
  
  scanf("%d %d", &n, &m);
  int numArr[n][m];
  
  //Please Enter Your Code Here
  for(i = 0; i < n; i++) {
    for(j = 0; j < m; j++) {
      scanf("%d ", &numArr[i][j]);
    }
  }
  
  scanf("%d %d", &a, &b);
  printf("%d", numArr[a][b]);
  
  return 0;
}
```
