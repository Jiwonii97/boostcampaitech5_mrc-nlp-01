# level2_mrc-nlp-01
### 해당 프로젝트는 네이버 커넥트재단 주최한 부스트캠프 AI Tech 5기 NLP 트랙 교육 과정 중 진행된 대회 프로젝트 입니다.

---

### 랩업 리포트  

상세한 프로젝트 내용은 랩업 리포트를 참고해주세요!!  
[Wrap up](./MRC_NLP_01_Wrapup_Report.pdf)

---

# 1. 프로젝트  개요

### A. 프로젝트 주제

<blockquote>
💡 Open-Domain Question Answering (ODQA)
</blockquote>

- **Question Answering (QA)**은 다양한 종류의 질문에 대해 대답하는 인공지능을 만드는 연구 분야입니다.
- 다양한 QA 시스템 중 ODQA는 주어지는 지문이 따로 존재하지 않고 사전에 구축되어있는 Knowledge resource 에서 질문에 대답할 수 있는 문서를 찾는 과정이 추가되기 때문에 더 어려운 문제입니다.
- 질문에 관련된 문서를 찾아주는 "retriever" 와 관련된 문서를 읽고 적절한 답변을 찾거나 만들어주는 "reader"를 구현하여 질문에 대한 원하는 답변을 얻을 수 있습니다.

### B. 데이터셋

- **데이터 유형 (Source)** : `wikipedia_documents` (약 57,000개)
- **Train_dataset 데이터 개수 : train (**3,952), **validation** (240)
- **Test_dataset 데이터 개수** : **validation** (600)

### C. 평가지표

- **Exact Match (EM)** : 모델의 예측과, 실제 답이 정확하게 일치할 때만 점수가 주어지는 평가방식
- **F1 Score** : 일치하지 않더라도 겹치는 단어도 있는 것을 고려해 부분 점수가 주어지는 평가방식

![image](https://github.com/Jiwonii97/boostcampaitech5_mrc-nlp-01/assets/79522982/4bfc5e99-397a-4d8c-854e-458bd5c9ac6b)


제공된 학습 데이터셋 구성

# 2. 프로젝트  팀  구성  및  역할

- 김효연 : Haystack, Elasticsearch(Retrieval), DPR(Retrieval)
- 서유현 : 데이터 전처리/후처리, Question Generation, PEFT
- 손무현 : 데이터 증강 (BackTranslation), Retrieval 실험 및 앙상블, PEFT
- 이승진 : 데이터 전처리, Haystack, BM25(Retrieval), Reranker, DAPT-TAPT-Fine tuning(twice)
- 최규빈 : 프로젝트 서칭, Base-code 작성, Curriculum learning
- 황지원 : PM, 데이터 증강 (Hanspell), 데이터 샘플링 및 전처리, Bigbird(Reader), DPR(Retrieval)
