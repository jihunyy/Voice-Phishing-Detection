## 💡 Prototype
### 개체명 인식 기반 보이스피싱 탐지 모델
실시간 전화에서 개체명 인식을 통해 보이스피싱 위험도를 실시간으로 게재
![thevoice_prototype](https://user-images.githubusercontent.com/80081987/137754280-baed0f39-70a8-4def-b726-b4e499378685.png)

## 🚂 Pipeline
### 1. Data Crawling & Collecting
금융감독원 보이스피싱 지킴이 사이트에서 보이스피싱 텍스트 크롤링 및 전처리   
[AI Hub 상담 음성 데이터](https://aihub.or.kr/aidata/30711)에서 상담 데이터 수집 후 전처리 

### 2. ETRI NER Tagging
[ETRI NER API](https://aiopen.etri.re.kr/guide_wiseNLU.php)로 보이스피싱 및 콜센터 텍스트에서 단어들을 NER 태깅해 데이터 일관성을 확보

### 3. Sentence N-gram & Embedding
전화 맥락을 학습하고자 데이터를 문장 N-gram으로 변환했으며   
문장 표현력을 극대화하고자 Sentence Transformer 및 KoBERT 사용

### 4. Voicephishing Detection
비교적 적은 데이터에도 적합하는 머신러닝 분류모델 활용   
로지스틱 회귀, 나이브 베이즈, 랜덤포레스트로 실험 및 성능 평가
