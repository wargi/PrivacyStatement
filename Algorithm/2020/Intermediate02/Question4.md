# 배열의 남은 곳 채우기 #

## 1. 문제
```
1. 2차원 배열(4x4)를 만들고 좌표 (0, 0) ~ (2, 2)까지 숫자 9개를 입력 받습니다.
ex)
input)
1 2 1
2 3 4
3 2 1

2차원 배열 상태)
1 2 1 0
2 3 4 0
3 2 1 0
0 0 0 0

2. 남은 빈칸(0인 상태인 곳) 가로줄인 곳은 가로줄의 합을,
   세로줄인 곳은 세로줄의 합을 채우고,
   (3, 3)에는 대각선의 합을 채우고 2차원 배열(4x4)의 최종상태를 출력해주세요.
   
위의 예제 결과
output)
1 2 1 4
2 3 4 9
3 2 1 6
6 7 6 5
```

## 2. 입력
- 좌표 (0, 0) ~ (2, 2)까지 숫자 9개를 입력 받습니다.

## 3. 출력
- 2차원 배열(4x4)의 최종상태를 출력해주세요.

## 4. 예제 입력
```
1 1 1
2 2 2
3 3 3
```

## 5. 예제 출력
```
1 1 1 3
2 2 2 6
3 3 3 9
6 6 6 6
```

## 6. 예제 입력

```
1 2 3 6
4 5 6 15
7 8 9 24
12 15 18 15
```

## 7. 예제 출력

```
lev0:2
lev1:4
lev2:0
lev3:0
```

## 8. 예제 입력

```
1 3 1
2 4 2
3 5 3
```

## 9. 예제 출력

```
1 3 1 5
2 4 2 8
3 5 3 11
6 12 6 8
```

## 10. 코드

```c++
#include<iostream>
using namespace std;

int map[4][4] = { 0 };

int main() {
	for (int i = 0; i < 3; i++) {
		for (int j = 0; j < 3; j++) {
			cin >> map[i][j];
		}
	}


	map[3][3] = map[0][0] + map[1][1] + map[2][2];
	for (int i = 0; i < 3; i++) {
		map[i][3] = map[i][0] + map[i][1] + map[i][2];
		map[3][i] = map[0][i] + map[1][i] + map[2][i];
	}

	for (int i = 0; i < 4; i++) {
		for (int j = 0; j < 4; j++) {
			cout << map[i][j] << " ";
		}
		cout << "\n";
	}

	return 0;
}
```