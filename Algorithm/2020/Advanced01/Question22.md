# 사각도형의 좌표구하기

## 1. 문제

- 2차원 배열(4x5)이 있습니다.
- 사각 도형 블럭을 입력받고, 사각 도형의 시작점 좌표와 끝점 좌표를 구해서 출력하는 프로그램을 작성해주세요.
-  <img src="./Exam01.png" alt="Exam" style="zoom:77%;" />

```
ex)
input)
0 1 0 0 0
0 1 0 0 0
0 1 1 1 0
0 0 0 0 0

output)
(0,1)
(2,3)

ex)
input)
0 0 0 0 0
0 1 1 0 0
0 1 1 1 0
0 0 0 0 0

output)
(1,2)
(2,4)
```


## 2. 입력

- 첫 번째 줄: 사각도형이 포함된 2차원 배열(4x5)을 입력받습니다.

## 3. 출력

- 사각 도형의 시작점 좌표와 끝점 좌표를 구해서 출력해주세요.


## 4. 예제 입력
```
0 0 0 0 0
0 1 1 0 0
0 1 1 1 0
0 0 0 0 0
```

## 5. 예제 출력
```
(1,2)
(2,4)
```

## 6. 코드

```c++
#include <iostream>
using namespace std;

int main() {
	int sy = -1, sx = -1, ey, ex;
	int map[4][5] = { 0, };

	for (int i = 0; i < 4; i++) {
		for (int j = 0; j < 5; j++) {
			cin >> map[i][j];
		}
	}

	for (int i = 0; i < 4; i++) {
		for (int j = 0; j < 5; j++) {
			if (map[i][j] == 1) {
				if (sy == -1) {
					sy = i;
					sx = j;
				}
				ey = i;
				ex = j;
			}
		}
	}

	cout << "(" << sy << "," << sx << ")\n";
	cout << "(" << ey << "," << ex << ")";

	return 0;
}
```
