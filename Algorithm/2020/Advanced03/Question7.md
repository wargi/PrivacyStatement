# 짝 맞추기 2 #

## 1. 문제
- 문장을 입력 받습니다.
- 문장은 숫자와 '<', '>'로 구성되어 있습니다.
- 열리는 꺽쇠가 나오면 꺽쇠가 닫혀야 합니다.
- 정상적으로 꺽쇠의 짝이 맞는지 판별하는 프로그램을 작성하시오.

```
예시)
<35<6<912>>10> -> 정상
56<7>>65 -> 비정상
>>15<< -> 비정상
612<>7<>91 -> 정상
```

## 2. 입력
- 문장을 입력 받습니다.

## 3. 출력
- 꺽쇠의 짝이 맞다면 "정상", 아니라면 "비정상"을 출력하세요.

## 4. 예제 입력
```
<<1234>><
```

## 5. 예제 출력
```
비정상
```

## 6. 예제 입력

```
<1<<2<<<3>>4>5>>>
```

## 7. 예제 출력

```
정상
```

## 8. 코드

```c++
#include <iostream>
#include <string>
using namespace std;

int main()
{
	string s;
	cin >> s;

	int cnt = 0;
	for (int i = 0; i < s.size(); i++) {
		if (s[i] == '<') cnt++;
		if (s[i] == '>') cnt--;
		if (cnt < 0) break;
	}

	if (cnt == 0) cout << "정상";
	else cout << "비정상";
}
```