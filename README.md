# kobert_classification
기술스택: Python, Tensorflow, Pytorch, KoBERT
논문작성 "A Study of BERT-based Classification Performance of Text-based Health Counseling Data"
구현환경: Google Colab

텍스트 건강상담 데이터를 활용하여, KoBERT, CNN, RNN, LSTM, GRU의 성능을 비교하였습니다.

CNN
![image](https://user-images.githubusercontent.com/76803357/184536545-9138e78b-9994-4377-b042-41be90ddd2c4.png)
모델의 특징을 추출하여, 데이터를 분류한다.

RNN
![image](https://user-images.githubusercontent.com/76803357/184536557-a88aed3c-389f-4f1a-9d6d-1b779a6c789f.png)
해당 노드의 출력값을 다음노드의 입력으로 보내어, 순환하는 신경망

LSTM
![image](https://user-images.githubusercontent.com/76803357/184536561-42b9a1e9-e920-4565-9b6d-488d087b9940.png)
LSTM의 의존시간을 해결하기위하여, 정보를 기억하는 구조로 설계됨.

GRU
![image](https://user-images.githubusercontent.com/76803357/184536566-c1808974-2937-4729-aea7-c8b6d6f5f179.png)
LSTM의 구조를 단순화 시켰고, 학습속도가 LSTM보다 빠르며, 비슷한 성능을 보임.

BERT
![image](https://user-images.githubusercontent.com/76803357/184536902-f89829ec-1bfc-45a9-a60b-4b87a98dcfd7.png)
Masked LM, NSP 두 방식으로 사전학습함.
Masked LM 무작위 단어를 Masked 토큰으로 변환 후, Masking 된 토큰을 예측하는 방법으로 사전학습을 함.
NSP(Next Sentence Precision) 2개의 문장 
실험과정
데이터 수집: 네이버 지식in 건강상담 데이터 15958건(9개의 진료과목, Train set 12766건, Test set 3192건)을 크롤링하였습니다. 
데이터 전처리: 특수문자 및 공백제거 -> 불용어 제거 -> 형태소분석(Tokenize) -> 희소단어 제거
모델 구현: KoBERT, CNN, RNN, LSTM, GRU
모델 평가 검증: Accuracy, Precision, Recall, F1-Score를 통한 모델 검증
