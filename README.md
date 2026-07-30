# 🧠 AI Model 종류

> **💡 Note:** 여러 AI 모델들을 경험하다 보니 정리가 필요

<br>

## 🗺️ Mindmap
```mermaid
flowchart LR
    %% [1] 노드/줄 간격 조절 (더 촘촘하게 설정)
    linkStyle default stroke:#888888,stroke-width:1.5px;

    %% [2] 박스 배경/테두리를 없애고 글자 색상 및 폰트 설정
    classDef rootStyle fill:none,stroke:none,color:#2196F3,font-size:20px,font-weight:bold;
    classDef branch1 fill:none,stroke:none,color:#FF9800,font-size:16px,font-weight:bold;
    classDef branch2 fill:none,stroke:none,color:#4CAF50,font-size:16px,font-weight:bold;
    classDef leafStyle fill:none,stroke:none,color:#333333,font-size:14px;

    %% [3] 루트 노드
    Root["AI Models"]

    %% [4] 상단 브랜치 (Algorithm / Architecture)
    Arch["Algorithm_Architecture<br/>(동작 원리 및 구조)"]
    Root --- Arch
    
    Rule["Rule_based"]
    Conn["Connectionist"]
    Prob["Probabilistic"]
    Rein["Reinforcement"]

    Arch --- Rule
    Arch --- Conn
    Arch --- Prob
    Arch --- Rein

    C1["CNN / RNN"]
    C2["Transformer"]
    C3["SSM / GNN"]
    
    Conn --- C1
    Conn --- C2
    Conn --- C3

    P1["Diffusion"]
    P2["GAN / VAE"]
    
    Prob --- P1
    Prob --- P2

    R1["Agentic"]
    Rein --- R1

    %% [5] 하단 브랜치 (Task / Modality)
    Task["Task_and_Modality<br/>(대상 데이터 및 과업)"]
    Root --- Task

    Text["Text_NLP"]
    Vis["Vision"]
    Aud["Audio"]
    Multi["Multimodal"]
    Sci["Scientific_Bio"]

    Task --- Text
    Task --- Vis
    Task --- Aud
    Task --- Multi
    Task --- Sci

    T1["LLM"]
    T2["Code"]
    
    Text --- T1
    Text --- T2

    V1["Image / Video"]
    V2["3D / Spatial"]
    
    Vis --- V1
    Vis --- V2

    %% [6] 스타일 일괄 적용
    class Root rootStyle;
    class Arch branch1;
    class Task branch2;
    class Rule,Conn,Prob,Rein,C1,C2,C3,P1,P2,R1,Text,Vis,Aud,Multi,Sci,T1,T2,V1,V2 leafStyle;