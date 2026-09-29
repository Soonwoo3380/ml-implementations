# Graph Neural Network Implementations

그래프 신경망의 구조와 학습 과정을 이해하기 위해
주요 GNN 모델과 그래프 클러스터링 방법을 구현하고 실험한 내용을 정리한 저장소입니다.

라이브러리를 단순히 적용하는 데 그치지 않고,
그래프의 노드와 엣지 정보가 어떻게 전달되고 집계되는지 살펴보며
각 모델의 구조와 동작 방식을 이해하는 데 초점을 두었습니다.

---

## Implementations

| Directory | Model / Topic | Description |
| --- | --- | --- |
| [`gcn`](./gcn) | GCN | Graph Convolutional Network 구현 및 실험 |
| [`gat`](./gat) | GAT | Attention을 활용한 Graph Attention Network 구현 및 실험 |
| [`dmon`](./dmon) | DMoN | Deep Modularity Networks 기반 그래프 클러스터링 실험 |
| [`GNN_pytorch_geo`](./GNN_pytorch_geo) | PyTorch Geometric | PyTorch Geometric을 활용한 GNN 모델 구현 및 실험 |

---

## 1. Graph Convolutional Network

GCN의 그래프 합성곱 과정을 구현하고 실험했습니다.

그래프에서 각 노드가 이웃 노드의 정보를 집계하고,
이를 바탕으로 새로운 노드 표현을 학습하는 과정을 확인하는 데 초점을 두었습니다.

**Key Points**

- 그래프의 노드 및 엣지 구조 처리
- 이웃 노드 정보 집계
- Graph Convolution 기반 노드 표현 학습
- GCN 학습 과정 구현 및 실험

Directory: [`gcn`](./gcn)

---

## 2. Graph Attention Network

그래프의 모든 이웃 정보를 동일하게 반영하는 대신,
각 이웃의 중요도를 학습하여 정보를 집계하는 GAT를 구현하고 실험했습니다.

GCN과 비교하며 attention mechanism이
이웃 노드의 정보를 선택적으로 반영하는 방식을 이해하는 데 초점을 두었습니다.

**Key Points**

- Graph Attention 구조 이해
- 이웃 노드별 attention weight 계산
- Attention 기반 node representation 학습
- GCN과 다른 message aggregation 방식 실험

Directory: [`gat`](./gat)

---

## 3. Deep Modularity Networks

그래프의 연결 구조를 바탕으로
노드들을 여러 커뮤니티로 구분하는 DMoN 기반 그래프 클러스터링을 실험했습니다.

노드 분류뿐 아니라 그래프 자체의 구조를 활용해
군집을 학습하는 방법을 이해하는 데 초점을 두었습니다.

**Key Points**

- Graph clustering
- Community detection
- Modularity 기반 그래프 구조 평가
- DMoN 기반 clustering 실험

Directory: [`dmon`](./dmon)

---

## 4. GNN with PyTorch Geometric

PyTorch Geometric을 활용하여
그래프 데이터를 구성하고 GNN 모델을 학습하는 과정을 실험했습니다.

직접 구현을 통해 확인한 GNN의 기본 구조를
그래프 학습 라이브러리에서는 어떻게 표현하고 활용하는지 비교하며 정리했습니다.

**Key Points**

- PyTorch Geometric 기반 그래프 데이터 처리
- GNN layer 구성
- 그래프 학습 파이프라인 구성
- 직접 구현 방식과 framework 기반 구현 비교

Directory: [`GNN_pytorch_geo`](./GNN_pytorch_geo)

---

## Research Connection

이 저장소에서 다룬 GCN과 DMoN은 이후
확률 정보와 임베딩 정보를 하나의 그래프에서 함께 활용하는
GNN 기반 토픽 모델 연구로 이어졌습니다.

연구에서는 임베딩을 노드 특성으로,
단어 간 확률 관계를 엣지로 표현한 그래프를 구성하고
GCN과 DMoN을 연결한 end-to-end 프레임워크를 설계했습니다.

관련 연구:

[Graph Neural Network-Based Topic Model](https://github.com/Soonwoo3380/gnn-topic-model)

---

## Tech Stack

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white"/>
  <img src="https://img.shields.io/badge/PyTorch%20Geometric-3C2179?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/NetworkX-2C7FB8?style=for-the-badge"/>
</p>

---

## Repository Structure

```text
ml-implementations/
├── gcn/
├── gat/
├── dmon/
├── GNN_pytorch_geo/
├── README.md
└── LICENSE
```
