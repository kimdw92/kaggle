# [책]카카오 아레나 데이터 경진대회 1등 노하우
상품 카테고리 분류 대회 1등 코드를 읽고 필사한 self-study 내용입니다.  
Reference: https://github.com/lime-robot/categories-prediction

## 학습 요약:
- 문제 유형 : 상품명과 상품이미지를 이용해 상품 카테고리를 분류하는 문제
- PyTorch 경험
- 텍스트 정보는 BERT 모델로 벡터화한다 -> Transformer, BERT, GPT 등 관련된 최신 NLP 모델들을 개념위주로 추가 공부
- Python 딥러닝 코드 모듈화 공부: 모델파일과 학습파일 분리/ CFG 클래스로 hyper-param 관리/ argparse 사용

## file 용도:
1. preprocess.ipynb : 학습 데이터 전처리
2. my_cate_model.py : BERT 등 딥러닝 모델 구현 파일
3. my_cate_dataset.py : torch의 DataLoader로 넘기기 위해 전처리된 데이터를 가공
4. train.py : 위의 모델과 데이터셋 인스턴스를 생성해서 학습하고 모델 저장
5. inference.py : 학습된 모델을 불러와서 Dev 데이터셋으로 대회 제출용 파일 생성
