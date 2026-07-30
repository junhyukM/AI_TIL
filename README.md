# 🧠 AI Model Taxonomy (AI 모델 분류 사전)

> **💡 Note:** 이 문서는 AI 모델을 작동 방식(아키텍처)과 처리하는 데이터 형태(모달리티)에 따라 구조화한 TIL(Today I Learned) 맵입니다. 파란색 링크를 클릭하면 해당 개념으로 바로 이동합니다!

<br>

## 🗺️ 전체 시각화 지도 (Mindmap)
```mermaid
mindmap
  root((AI Models))
    Architecture<br/>(How it works)
      Rule_based
      Connectionist
        **CNN:**[CNN?](./docs/CNN.md) / RNN
        Transformer
        SSM / GNN
      Probabilistic
        Diffusion
        GAN / VAE
      Reinforcement
        Agentic
    Modality<br/>(What it processes)
      Text_NLP
        LLM
        Code
      Vision
        Image / Video
        3D / Spatial
      Audio
      Multimodal
      Scientific_Bio