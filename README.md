# 🧠 AI Model 종류

> **💡 Note:** 여러 AI 모델들을 경험하다 보니 정리가 필요

<br>

## 🗺️ Mindmap (Tree Structure)
```mermaid
flowchart LR
    %% [1] 스타일 정의
    classDef rootStyle fill:#2c3e50,color:#ffffff,stroke:#34495e,stroke-width:3px,font-size:22px,font-weight:bold
    classDef branch1 fill:#d4efdf,color:#196f3d,stroke:#52be80,stroke-width:2px,font-size:18px,font-weight:bold
    classDef branch2 fill:#d6eaf8,color:#154360,stroke:#5dade2,stroke-width:2px,font-size:18px,font-weight:bold
    classDef leafStyle fill:#ffffff,color:#333333,stroke:#bdc3c7,stroke-width:1px,font-size:14px

    %% [2] 노드 정의 및 연결
    Root(("AI Models"))

    %% 분기 1: Algorithm_Architecture
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

    %% 분기 2: Task_and_Modality
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

    %% [3] 클래스(스타일) 일괄 적용 (호환성 문제를 위한 가장 안전한 방법)
    class Root rootStyle;
    class Arch branch1;
    class Task branch2;
    class Rule,Conn,Prob,Rein,C1,C2,C3,P1,P2,R1,Text,Vis,Aud,Multi,Sci,T1,T2,V1,V2 leafStyle;