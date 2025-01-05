# [Silver III] 1로 만들기 - 1463

## 📍 [문제 및 풀이 코드 링크](https://github.com/Jinyshin/Algorithm/tree/main/%EB%B0%B1%EC%A4%80/Silver/1463.%E2%80%851%EB%A1%9C%E2%80%85%EB%A7%8C%EB%93%A4%EA%B8%B0)

## 📍 풀이 방법

- 시간 제한과 입력값 범위로 인해 브루트포스 방식으로 풀이 불가능
- dp를 사용해서 중복되는 계산을 없애고 시간을 줄이자!

### pseudo code

- N을 입력받는다.
- dp 배열 선언(dp[i]는 숫자 i를 1로 만드는데 필요한 최소 횟수)
- dp[1] = 0 (1은 이미 최소 상태)
- for i: 2 ~ N:

  - dp[i] = dp[i-1] + 1 (1을 뺀 경우)
  - if i % 2 == 0
    dp[i] = min(dp[i], dp[i/2] + 1)
  - if i % 3 == 0
    dp[i] = min(dp[i], dp[i/3] + 1)

- sout dp[N]
