# DDPG
###### 논문: https://arxiv.org/pdf/1509.02971.pdf

## 1. 공부시 유의할점
#### soft update
target network 는 main critic 의 학습 목표가 흔들리지 않도록 하기 위한 수단이다.
DQN 에서는 target network를 고정시켜두고 그 방향으로 main network 학습을 진행하며 일정 step 마다 한번씩 main network의 w를 target network로 그대로 복사하는데, DDPG 에서는 매 step 마다 soft update 한다. 이 soft update로 인해 target network의 w는 main network w 방향으로 매 step 조금씩 이동한다.

## 2. DDPG in one page
![ddpg](https://user-images.githubusercontent.com/9976453/51683122-724fe800-202c-11e9-8e72-97eb538584b2.png)

#### 참고하면 좋은 사이트
* https://github.com/170928/-Review-Continuous-Control-With-Deep-Reinforcement-Learning
* https://reinforcement-learning-kr.github.io/2018/06/26/3_ddpg/
