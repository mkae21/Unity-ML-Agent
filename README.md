# PathFinder

> 강화학습 기반 자율이동로봇(AMR)의 최적 경로 탐색 알고리즘 개발 프로젝트

## 프로젝트 개요

**PathFinder**는 Unity ML-Agents를 활용하여 자율이동로봇(AMR)이 장애물과 다른 AMR을 인식하고, 목적지까지 스스로 이동 경로를 학습하도록 구현한 강화학습 프로젝트입니다.

기존의 고정 경로 기반 이동 방식은 경로를 수동으로 설정해야 하고, 장애물이나 돌발 상황에 취약하며, 여러 AMR이 동시에 움직일 경우 교착 상태가 발생할 수 있습니다. 본 프로젝트에서는 이러한 문제를 해결하기 위해 강화학습을 적용하여 AMR이 환경을 관찰하고, 보상을 기반으로 목적지까지의 경로를 스스로 학습하도록 설계했습니다.

---

## 개발 기간 및 참여 인원

- 개발 기간: 2025.03 ~ 2025.06
- 참여 인원: 4명
- 담당 역할:
  - Unity ML-Agents 기반 학습 환경 구성
  - AMR Agent 이동 및 센서 구조 설계
  - Reward 설계 및 학습 결과 개선
  - Curriculum Learning을 통한 학습 난이도 조정

---

## 사용 기술

| 구분 | 기술 |
|---|---|
| Engine | Unity |
| ML Framework | Unity ML-Agents |
| Language | C# |
| Training | Python |
| Algorithm | PPO(Proximal Policy Optimization) |
| Sensor | Grid Sensor, Ray Sensor |
| Learning Method | Reinforcement Learning, Curriculum Learning |

---

## 시스템 구조

```text
Python Trainer
TensorFlow / Keras / PyTorch
        |
        | Action
        v
Unity ML-Agents
        |
        | State, Reward
        v
Unity Environment
