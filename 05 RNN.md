- NLP is full of sequential data
- Long-distance Dependencies in Language

##### Recurrent Neural Network (Elman 1990)
- 정보를 기억하기 위한 툴
- 시간별로 펼쳐 볼 수 있음
- 파라미터들 공유 -> Training이 어려움: BPTT (backpropagation through time)

##### RNN으로 할 수 있는 것
- Sentence Representation을 얻음: 전체 문장을 읽어 예측에 활용
  - Sentence classification (Intent), Conditioned generation, Retrieval, ...
- Context Representation (예: Word 단위)를 얻음: 그 때까지의 데이터를 읽어 예측에 활용
  - Tagging, Language Model, Parsing, ...
- Bi-RNNs (Bidirectional RNN): 양방향으로 RNN을 돌림

##### RNN의 문제점과 해결책
- Vanishing Gradient: 곱하기로 계산, 단계가 지나갈 수록 Gradient가 너무 작아짐
- 해결책: LSTM (Long Short-term Memory, Hochreiter and Schmidhuber 1997)
  - update/input/output 게이트를 통해 정보를 Control
- GRU (Gated Recurrent Units, GRUs; Cho et al. 2014)
  - take input, update state
  
##### RNN에서 Mini Batching은 어떻게?
- RNN에서 쉽지 않음: 각 단어가 이전 단어에 의존적, Sequence가 가변적
- Mask를 두어서 계산
- Bucketing/Sorting: 같은 batch에 비슷한 길이의 단어들 포함

##### Long~ Long~ Sequences 다루기 (예, Document)
- GPU 메모리 부족 ㅠㅠ
- Truncated BPTT: Segment로 나눠서, Segment 단위로 BP / 대신 State는 Segment간 전달

##### Pre-training / Transfer for RNNs
- 장점: Powerful and flexible
- 단점: 많은 데이터 필요, 문장 끝까지 전달하면서 시그널이 약해짐
- Transfer: 하나 테스크에 훈련한 뒤 그 Network을 다른 문제 푸는 데 활용
  - Pretrain: Big data, 쉽게 학습
  - Main task: Small data, 학습 어려움
  - LM -> Sentence Classifier (Elmo / Bert!)



