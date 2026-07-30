# 🧠 AI Model 종류

> **💡 Note:** 여러 AI 모델들을 경험하다 보니 정리가 필요

<br>

## 🗺️ Mindmap
```mermaid
%%{
  init: {
    'flowchart': {
      'nodeSpacing': 5,      %% 위아래 노드 간격 (기본값 약 50 -> 5로 축소)
      'rankSpacing': 20,     %% 좌우 단계 간격 (기본값 약 50 -> 20으로 축소)
      'padding': 2           %% 박스 내부 여백 최소화
    }
  }
}%%
flowchart LR
    %% [1] 선 두께 및 색상
    linkStyle default stroke:#aaa,stroke-width:1px;

    %% [2] 스타일 정의 (폰트 크기 축소 및 간격 최소화)
    classDef rootStyle fill:none,stroke:none,color:#2196F3,font-size:15px,font-weight:bold;
    classDef branch1 fill:none,stroke:none,color:#FF9800,font-size:13px,font-weight:bold;
    classDef branch2 fill:none,stroke:none,color:#4CAF50,font-size:13px,font-weight:bold;
    classDef leafStyle fill:none,stroke:none,color:#333333,font-size:12px;

    %% [3] 노드 정의 및 연결
    Root["AI Models"]

    Arch["Algorithm_Architecture (동작 원리 및 구조)"]
    Root --- Arch
    
    Rule["Rule_based"]
    Conn["Connectionist"]
    Prob["Probabilistic"]
    Rein["Reinforcement"]

    Arch --- Rule & Conn & Prob & Rein

    C1["CNN / RNN"]
    C2["Transformer"]
    C3["SSM / GNN"]
    Conn --- C1 & C2 & C3

    P1["Diffusion"]
    P2["GAN / VAE"]
    Prob --- P1 & P2

    R1["Agentic"]
    Rein --- R1

    Task["Task_and_Modality (대상 데이터 및 과업)"]
    Root --- Task

    Text["Text_NLP"]
    Vis["Vision"]
    Aud["Audio"]
    Multi["Multimodal"]
    Sci["Scientific_Bio"]

    Task --- Text & Vis & Aud & Multi & Sci

    T1["LLM"]
    T2["Code"]
    Text --- T1 & T2

    V1["Image / Video"]
    V2["3D / Spatial"]
    Vis --- V1 & V2

    %% [4] 스타일 적용
    class Root rootStyle;
    class Arch branch1;
    class Task branch2;
    class Rule,Conn,Prob,Rein,C1,C2,C3,P1,P2,R1,Text,Vis,Aud,Multi,Sci,T1,T2,V1,V2 leafStyle;