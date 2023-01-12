# Q 러닝
## Q 러닝 <br>
모델없이 학습하는 강화학습 알고리즘
목표: 에이전트가 특정 상황에서 특정 행동을 하라는 최적의 정책을 배우는 것으로, 현재 상태로부터 시작하여 모든 연속적인 단계들을 거쳤을 때 전체 보상의 예측값을 극대화

## Q value <br>
- 어떤 상태 s에서 어떤 행동 a를 했을 때, 그 행동의 가치를 나타내는 Q(s,a) 함수를 사용
- 미래의 보상을 계산하기 위해 0~1 사이의 γ(Discount Factor)를 사용
- 현재 상태로 부터 Δt 시간이 흐른 후에 얻는 보상 r은 𝛾Δ𝑡만큼 할인된 𝑟 ∗ 𝛾Δ𝑡로 계산
- Q value는 어떤 시간 t에 따라 행동 a를 할 때 미래의 보상들의 총합의 기대값
<img width="675" alt="스크린샷 2023-01-13 오전 4 10 04" src="https://user-images.githubusercontent.com/121830114/212159144-a6a48a22-76bd-42b9-a2c9-a05e0636d756.png">

## Q algorithm
알고리즘이 시작되기 전에 Q 함수는 고정된 임의의 값을 갖는다. 그리고 매 time-step(𝑡)마다 Agent는 행동를 선택하게 되고, 보상 를 받으며 새로운 상태로 전이하고, Q 값이 갱신된다. 이 알고리즘의 핵심은 이전의 값과 새로운 정보의 가중합(weighted sum)을 이용하는 Value Iteration Update 기법이다.
