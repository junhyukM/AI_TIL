# 🧠 AI Model Taxonomy (AI 모델 분류 사전)

> **💡 Note:** 이 문서는 AI 모델을 작동 방식(아키텍처)과 처리하는 데이터 형태(모달리티)에 따라 구조화한 TIL(Today I Learned) 맵입니다. 파란색 링크를 클릭하면 해당 개념으로 바로 이동합니다!

<br>

## 🗺️ 전체 시각화 지도 (Mindmap)
```mermaid
mindmap
  root((AI Models))
    Architecture<br/>(How it works)
      Rule_based("`[Rule-based](#통계-및-규칙-기반-statistical--rule-based)`")
      Connectionist("`[Connectionist](#연결주의-기반-connectionist---deep-learning)`")
        CNN_RNN("`[CNN / RNN](#연결주의-기반-connectionist---deep-learning)`")
        Transformer("`[Transformer](#어텐션-기반-transformer-계열)`")
        SSM_GNN("`[SSM / GNN](#연결주의-기반-connectionist---deep-learning)`")
      Probabilistic("`[Probabilistic](#확률-및-생성-기반-probabilistic--generative)`")
        Diffusion("`[Diffusion](#확산-모델-diffusion-models)`")
        GAN_VAE("`[GAN / VAE](#확률-및-생성-기반-probabilistic--generative)`")
      Reinforcement("`[Reinforcement](#강화-및-에이전트-기반-reinforcement--agentic)`")
        Agentic("`[Agentic](#강화-및-에이전트-기반-reinforcement--agentic)`")
    Modality<br/>(What it processes)
      Text_NLP("`[Text_NLP](#텍스트-text--nlp)`")
        LLM("`[LLM](#거대-언어-모델-llm)`")
        Code("`[Code](#코드-code)`")
      Vision("`[Vision](#이미지비디오-vision)`")
        Image_Video("`[Image / Video](#이미지비디오-vision)`")
        3D_Spatial("`[3D / Spatial](#3d-및-공간-spatial)`")
      Audio("`[Audio](#오디오음성-audio--speech)`")
      Multimodal("`[Multimodal](#멀티모달-multimodal---융합)`")
      Scientific_Bio("`[Scientific_Bio](#과학-및-로보틱스-scientific--embodied)`")