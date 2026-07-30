# 🧠 AI Model 종류

> **💡 Note:** 여러 AI 모델들을 경험하다 보니 정리가 필요

<br>

## 🗺️ Mindmap (Tree Structure)
```mermaid
flowchart LR
    %% [스타일 정의] 배경색, 글자색, 테두리, 폰트크기
    classDef rootStyle fill:#2c3e50,color:#ffffff,stroke:#34495e,stroke-width:3px,font-size:22px,font-weight:bold
    classDef branch1 fill:#d4efdf,color:#196f3d,stroke:#52be80,stroke-width:2px,font-size:18px,font-weight:bold
    classDef branch2 fill:#d6eaf8,color:#154360,stroke:#5dade2,stroke-width:2px,font-size:18px,font-weight:bold
    classDef leafStyle fill:#ffffff,color:#333333,stroke:#bdc3c7,stroke-width:1px,font-size:14px

    %% [루트 노드]
    Root(("AI Models")) ::: rootStyle

    %% [분류 1: 동작 원리 및 구조]
    Arch["Algorithm_Architecture<br/>(동작 원리 및 구조)"] ::: branch1
    Root --- Arch
    
    Rule["Rule_based"] ::: leafStyle
    Conn["Connectionist"] ::: leafStyle
    Prob["Probabilistic"] ::: leafStyle
    Rein["Reinforcement"] ::: leafStyle

    Arch --- Rule
    Arch --- Conn
    Arch --- Prob
    Arch --- Rein

    Conn --- C1["CNN / RNN"] ::: leafStyle
    Conn --- C2["Transformer"] ::: leafStyle
    Conn --- C3["SSM / GNN"] ::: leafStyle

    Prob --- P1["Diffusion"] ::: leafStyle
    Prob --- P2["GAN / VAE"] ::: leafStyle

    Rein --- R1["Agentic"] ::: leafStyle

    %% [분류 2: 대상 데이터 및 과업]
    Task["Task_and_Modality<br/>(대상 데이터 및 과업)"] ::: branch2
    Root --- Task

    Text["Text_NLP"] ::: leafStyle
    Vis["Vision"] ::: leafStyle
    Aud["Audio"] ::: leafStyle
    Multi["Multimodal"] ::: leafStyle
    Sci["Scientific_Bio"] ::: leafStyle

    Task --- Text
    Task --- Vis
    Task --- Aud
    Task --- Multi
    Task --- Sci

    Text --- T1["LLM"] ::: leafStyle
    Text --- T2["Code"] ::: leafStyle

    Vis --- V1["Image / Video"] ::: leafStyle
    Vis --- V2["3D / Spatial"] ::: leafStyle