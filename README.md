# KLUE

문장의 단어에 대한 속성과 관계를 예측하는 Task

관계를 나타내는 class는 총 42개이고 각 sentence마다 이에 맞는 entity1과 entity2의 관계를 분류하는 문제.

## Final Score

- LB accuracy score: 81.2000%
- Ranking 8 / 136

## Ensemble

1. xlm-roberta-large 모델로 Stratified-kfold 진행.
    - 각 fold별로 validation accuracy를 기준으로 best model을 찾고 결과에 대해 단순 평균 앙상블을 진행.
    - 5-fold, 10-fold 두 번 진행 했을 때 성능이 각각 79.6%, 80.2%가 나옴.

2. 일반 k-fold 사용 시 성능이 더 내려감 72.8%