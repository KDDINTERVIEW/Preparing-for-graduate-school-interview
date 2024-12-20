# 인하대 인공지능대학원 면접 대비
---


## Interview Questions

<details>
<summary><a href="./answers/1-statistics-math.md"><strong>📈 통계/수학</strong></a></summary>


- 고유값(eigen value)와 고유벡터(eigen vector)이 무엇이고 왜 중요한지 설명해주세요.
```python
  행렬 A의 고유벡터는, 행렬 A에 의해 변환되었을 때 방향이 변하지 않고 단지 크기만 변하는 벡터를 말한다
  Av=λv에서 v (영벡터 아니어야 함)
  고유값은 λ (고유벡터 v가 변환될 때 그 크기가 얼마나 변하는지...)
```
- 샘플링(Sampling)과 리샘플링(Resampling)이 무엇이고 리샘플링의 장점을 말씀해주세요.
```python
  샘플링은 전체 모집단에서 데이터를 추출하는 거,특히나 모집단을 대표할 수 있도록 신중하게 선택되어야 함
  리샘플링은 기존의 샘플 데이터에서 새로운 샘플을 반복적으로 추출하여 통계적 분석을 수행하는 방식
  리샘플링에는 다음과 같은 방법이 있다
  - 교차 검증 (Cross Validation) : 모델의 성능 평가를 위해 데이터를 여러 번 분할하여 훈련과 테스트를 반복! 과적합 방지, 모델의 일반화 성능 평가
```
- 확률 모형과 확률 변수는 무엇인가요?
```python
  확률은 불확실성을 표현하는 수단, 이러한 불확실성을 확률로써 개량화하기 위해 확률함수로써 수학적으로 만든 모형이 확률 모형이다
  이는 어떤 실험이나 현상에서 가능한 모든 결과와 그 결과가 발생할 확률을 설명한다.
  확률 모형은 표본 공간, 확률 분포라는 두 가지 구성 요소로 이루어졌다!

  확률 변수는 확률 모형에서 정의된 함수
  쉽게 말하면 확률로 표현하기 위한 event를 정의하는 것
  어떤 것을 확률로 표현할 것인지에 대해 다양하게 정의가 가능하여 <변수>라는 용어를 사용한다
  (이산과 연속 확률 변수로 나뉨)
```
- 누적 분포 함수와 확률 밀도 함수는 무엇인가요? 수식과 함께 표현해주세요.
```python
  확률 밀도 함수는 연속 확률 변수의 분포를 설명하는 함수로, 특정 값에서의 확률 밀도를 나타낸다.
  누적 분포 함수는 확률 변수가 특정 값 이하일 확률을 타나내는 함수, 확률 밀도 함수를 적분하여 구할 수 있다
```
- 조건부 확률은 무엇인가요?
```python
   조건부 확률은 어떤 사건 A가 이미 일어난 상황에서 다른 사건 B가 일어날 확률을 의미한다
   즉 사건 B가 사건 A에 의해 영향을 받을 때의 확률을 계산할 것
```
- 공분산과 상관계수는 무엇일까요? 수식과 함께 표현해주세요.
```python
   공분산(Covariance)는 두 확률 변수 사이의 관계를 측정하는 지표로, 두 변수가 함께 어떻게 변하는지를 나타낸다
   즉 한 변수가 증가할 때 다른 변수가 증가하거나 감소하는 경향을 평가한다
   Cov(X,Y)=E[(X−E(X))(Y−E(Y))]

   상관계수는 공분산을 정규화하여 두 확률 변수 사이의 선형 관계를 1과 -1 사이의 값으로 표현한다
   상관계수는 공분산과 달리 단위에 의존하지 않기 때문에 비교적 직관적으로 두 변수의 관계 강도를 파악할 수 있다!
```
- 신뢰 구간의 정의는 무엇인가요?
```python
  신뢰구간은 모집단의 모수를 포함할 것으로 예상되는 값의 범위를 특정 신뢰 수준 하에 제시한 것이다
  즉 표본 데이터를 이용해 계산한 추정치가 모집단의 실제 값(모수)를 포함할 확률이 높은 구간을 의미한다
  보통 신뢰 수준과 함께 나타나며, 신뢰 수준은 이 구간이 모집단의 실제 모수를 포함할 확률을 의미한다.
```
- p-value를 모르는 사람에게 설명한다면 어떻게 설명하실 건가요?
```python
  신뢰구간은 모집단의 모수를 포함할 것으로 예상되는 값의 범위를 특정 신뢰 수준 하에 제시한 것이다
  즉 표본 데이터를 이용해 계산한 추정치가 모집단의 실제 값(모수)를 포함할 확률이 높은 구간을 의미한다
```
- R square의 의미는 무엇인가요?
```python
  R², 또는 결정계수(R-Squared)는 회귀 분석에서 사용되는 통계량으로,
  독립 변수가 종속 변수의 변동을 얼마나 잘 설명하는지를 나타낸다.
  즉, R²는 회귀 모델이 데이터를 얼마나 잘 설명하는지를 평가하는 지표이다.
```
- 평균(mean)과 중앙값(median)중에 어떤 케이스에서 뭐를 써야할까요?
```python
   평균은 데이터가 고르게 분포되어 있고 이상치가 없을 때 더 신뢰할 수 있다.
   하지만 이상치가 있으면 평균이 그 값에 의해 크게 영향을 받아 데이터의 중심을 제대로 반영하지 못할 수 있다.
   중앙값은 이상치나 비대칭 분포가 있는 경우 더 적절하다. 극단적인 값이 있더라도 중앙값은 그 영향을 받지 않기 때문에 데이터의 중심을 더 잘 나타낸다.
```
- 중심극한정리는 왜 유용한걸까요?
```python
   중심극한정리는 확률론에서 매우 중요한 개념으로, 표본 크기가 충분히 크면 어떤 분포를 따르는 모집단에서 표본을 추출하더라도,
   표본 평균의 분포가 정규분포에 가까워진다는 것을 의미한다!
   다시 말해, 모집단의 분포 형태에 관계없이 표본 평균의 분포는 표본 크기가 커질수록 점점 정규분포를 따르게 된다.
   중심극한정리는 다양한 형태의 모집단에서 표본을 추출해도, 표본 평균이 정규분포를 따르게 만들어 준다.
   이로 인해 모집단의 분포를 알지 못해도 표본 평균의 분포를 예측할 수 있습니다.
```
- 엔트로피(entropy)에 대해 설명해주세요. 가능하면 Information Gain도요.
```python
   엔트로피는 정보 이론에서 사용되는 개념으로, 불확실성 또는 혼란의 정도를 측정하는 지표이다.
   주로 확률 분포의 다양성을 측정하거나, 데이터의 예측 가능성을 평가하는데 사용된다.
   쉽게 말하면 데이터의 무질서도를 측정, 값이 높을 수록 불확실성이 커진다!

  정보 이득 (Information gain)
  정보이득은 결정 트리와 같은 알고리즘에서 특정 속성을 사용해 데이터 집합을 분할할 때, 엔트로피가 얼마나 감소하는지를 측정하는 지표이다
  즉 특정 속성을 기준으로 데이터를 나눴을 때 데이터의 불확실성이 얼마나 줄어드는지 나타낸다!
```
- 어떨 때 모수적 방법론을 쓸 수 있고, 어떨 때 비모수적 방법론을 쓸 수 있나요?
```python
   모수적 방법론은 모집단의 분포에 대해 특정한 가정을 하고 데이터를 분석하는 기법
   예를 들어 데이터가 정규분포를 따르는 것으로 가정하고 통계적 분석을 수행하는 경우가 대표적
   모수적 방법론은 데이터의 분포가 알려져 있을 때/ 표본 크기가 충분히 클 때/모집단의 분포에 대한 강한 가정이 성립할 때/ 등에서 사용

   비모수적 방법론은 데이터의 분포에 대한 가정이 필요하지 않은 분석 방법이다
   이 방법은 데이터가 특정한 분포를 따르지 않거나, 분포를 알 수 없을 때 유용하다
```
- “likelihood”와 “probability”의 차이는 무엇일까요?
```python
   확률(probability)은 주어진 모수에 대해 데이터가 발생할 확률
   가능도(Likellihood)는 주어진 데이터에 대해 모수가 그 데이터를 얼마나 잘 설명하는지를 평가
   예를 들어서 동전을 여러 번 던져 7번 중 5번 앞면이 나왔다고 가정하면
   확률은 5/7
   가능도는 특정한 모수 p가 주어졌을 때, 관측된 데이터 "7번 중 5번 앞면이 나옴"을 얼마나 잘 설명하는지를 평가
   L(p|X=5)
```
- 통계에서 사용되는 bootstrap의 의미는 무엇인가요.
```python
   부트스트랩은 통계적 추정의 신뢰성을 평가하기 위해 사용되는 비모수적 방법론
   특히 모집단의 분포에 대한 강한 가정을 하지 않고, 표본 데이터만을 사용해 모집단의 특성을 추정할 수 있는 강력한 기법이다.
   부트스트랩은 주어진 표본 데이터로부터 반복적으로 새로운 표본을 생성하여, 통계적 추정값(예: 평균, 분산, 신뢰구간 등)의 분포를 추정하는 방법이다.
```
- 모수가 매우 적은 (수십개 이하) 케이스의 경우 어떤 방식으로 예측 모델을 수립할 수 있을까요?
```python
   1. 간단한 모델 사용 : 선형 회귀, 로지스틱 회귀, k-최근접 이웃(KNN), 의사결정트리와 같은 단순한 모델을 사용하는 것이 좋습니다.
   2. 규제(Regularization) 기법 사용: 과적합을 방지하기 위해 L1, L2 규제 방법을 적용하여 모델의 복잡성을 줄일 수 있다
   3. 데이터 증강 : 데이터를 오히려 인위적으로 늘린다
```
- 검정력(statistical power)은 무엇일까요?
```python
   어떤 통계적 검정이 실제로 대립가설이 참일 때 이를 올바르게 검출할 확률을 의미한다.
   쉽게 말해, 검정력은 참인 효과를 감지할 수 있는 능력을 나타낸다.
   검정력의 의미: 검정력이 높을수록, 실제로 효과나 차이가 존재할 때 이를 발견할 가능성이 커진다.
```
- missing value가 있을 경우 채워야 할까요? 그 이유는 무엇인가요?
```python
   결측치가 있는 데이터를 그대로 사용하면 통계 분석, 머신러닝 모델링에서 왜곡된 결과를 초래할 수 있다
   특히 일부 알고리즘은 결측치를 허용하지 않기 때문에 데이터 전체가 무효화될 수 있다.
   결측치를 적절히 채우면 모델의 성능을 높일 수 있다. 결측치로 인해 모델이 학습할 수 있는 정보가 제한되거나, 예측의 정확도가 떨어질 수 있기 때문이다.
```
- 아웃라이어의 판단하는 기준은 무엇인가요?
```python
   아웃라이어는 데이터에서 다른 데이터 포인트와 비교해 극단적으로 벗어난 값을 의미한다.
   통계적 기준으로는 사분위 범위(IQR)에서 Q1-3*IQR보다 작거나, Q3+3*IQR보다 크면 보통 outlier라고 칭한다
   또는 데이터가 정규분포를 따른다고 가정할 떄, 평균에서 k개의 표준편차 이상 떨어진 값을 아웃라이어로 간주한다
```
- 필요한 표본의 크기를 어떻게 계산합니까?
```python
   표본 크기를 계산하는 방법은 연구의 종류에 따라 다르다
   평균의 차이를 비교할 때 : t 검정
   비율의 차이를 비교할 떄 : z 검정
   
```
- Bias를 통제하는 방법은 무엇입니까?
```python
   연구 설계 단계에서 Bias 통제 : 무작위 할당 (Randomization) - 실험군과 대조군에 참여자를 무작위로 배정해 그룹 간 차이 최소화, 무작위화는 선택 편향(Selection Bias)를 줄임
   데이터 수집 단계에서 Bias 통제 : 표준화된 측정 방법(Standardized Measurement) - 모든 데이터를 일관된 방식으로 수집해 측정 편향 (Measurement Bias)을 줄인다
   데이터 분석 단계에서의 Bias 통제 : 혼란 변수 (Confounding Variable) 통제 - 혼란 변수가 연구 결과에 영향을 미치지 않도록 다변량 분석, 공변량 분석을 사용해 통제
   
```
- 로그 함수는 어떤 경우 유용합니까? 사례를 들어 설명해주세요.
```python
   데이터가 크기 차이가 클 때나 지수적 증가가 있는 경우 유용하다.
   예를 들어서 금융 데이터를 분석할 때
   금융 분야에서는 기업의 매출, 시장 규모, 자산 등 다양한 변수가 매우 큰 범위를 가질 수 있다. 어떤 회사의 매출은 수백만 달러일 수 있지만, 또 다른 회사의 매출은 수십억 달러에 이를 수 있다
   로그 변환을 통해 이런 큰 차이를 줄이면 데이터가 더 균형 있게 분포되면, 분석하기 쉬워진다
   예를 들어 히스토그램을 그릴 때 로그 변환을 적용하면 극단적인 값들로 인해 왜곡되지 않은 분포를 볼 수 있다!
```
- 베르누이 분포 / 가우시안 정규 분포  / 카이제곱 분포 / 에 대해 설명해주세요.
```python
  베르누이 분포는 두 가지 결과(성공 혹은 실패)만 가능한 이산 확률 분포이다. 각각의 결과가 발생할 확률을 기반으로 한다. 베르누이 분포의 확률 변수 X는 1과 0만을 가질 수 있다
  가우시안 정규 분포는 연속 확률 변수로, 데이터가 평균값을 중심으로 종 모양의 대칭적인 분포를 따른느 경우를 설명한다. 이는 많은 자연현상에서 나타나는 일반적인 분포이다
  카이 제곱 분포는 연속 확률 분포로, 독립적인 표준 정규 분포 변수의 제곱의 합으로 정의된다. 카이제곱 분포는 자유도에 따라 모양이 달라진다.
```

</details>

<details>
<summary><a href="./answers/2-machine-learning.md"><strong>🤖 머신러닝</strong></a></summary>

- 알고 있는 metric에 대해 설명해주세요. (ex. RMSE, MAE, recall, precision ...)
```python
   RMSE는 회귀 모델의 성능을 측정하는 데 사용된다. 예측 값과 실제 값의 차이를 제곱한 평균의 제곱근을 계산한다.
   MAE는 예측 값과 실제 값의 차이의 절대값 평균을 계산한다. 회귀 모델의 성능을 측정하는 또 다른 지표이다.
   Precision은 모델이 True Positive로 예측한 것 중 실제로 True인 비율을 의미한다. 특히 양성 클래스에 대한 정확도를 측정하는 데 유용하다. TP / (TP+FP)
   Recall은 실제로 True인 것 중에서 모델이 True로 예측한 비율을 의미한다. TP / (TP + FN)
   F1 Score는 Precision과 Recall 사이의 균형을 평가하는 지표이다. precision과 recall의 조화 평균을 계산한다. F1 score = 2 * { (Precision X Recall) / (Precision + Recall) }
   R-squared(결정계수)는 회귀 분석에서 모델이 데이터를 얼마나 잘 설명하는지를 나타내는 지표이다. 0에서 1 사이의 값을 가지며, 1에 가까울수록 모델이 데이터를 잘 설명하는 것을 의미한다. 
```
- 정규화를 왜 해야할까요? 정규화의 방법은 무엇이 있나요? (🥲 내 논문 주제...)
```python
   머신러닝 알고리즘(특히 경사 하강법 기반 알고리즘)은 특성(feature) 값의 범위가 매우 다르면 학습이 제대로 이뤄지지 않을 수 있다.
   예를 들어 하나의 특성의 값이 0~1 사이인데, 다른 특성의 값이 0~10000 사이라면 큰 범위를 가진 특성이 모델 학습에 더 큰 영향을 미치게 되어 잘못된 가중치를 학습할 가능성이 있다.
   특히 경사 하강법 기반 알고리즘의 경우 정규화를 하면 학습 속도가 빨라지도 알고리즘이 더 잘 수렴하게 된다.
   정규화된 데이터는 최적의 해를 찾는 과정에서 균형 잡힌 경로로 수렴하도록 도와준다.
   심지어 일부 알고리즘은 특성의 크기 차이로 인해 성능이 저하될 수 있다. 정규화를 하면 이러한 문제를 방지하여 모델 성능이 향상될 수 있다.

   정규화 방법
   Min-Max 정규화 : 데이터를 (대체로) 0~1로 변환하는 방법. 최소값을 0, 최대값을 1로 변환하며, 나머지 값은 비례적으로 조정한다.
   Z-Score 정규화 : 데이터를 평균 0, 표준편차 1로 변환하는 방법. 데이터가 정규 분포를 따를 때 효과적!
   Robust 정규화 : median과 사분위 범위 (IQR)를 사용하여 정규화하는 방법이다. 이상치에 덜 민감하다.
```
- Local Minima와 Global Minimum에 대해 설명해주세요.
```python
   Global Minimum은 전역 최소값. 함수의 모든 가능한 값 중 가장 낮은 값, 최적화 문제에서 우리가 궁극적으로 찾고자 하는 지점!
   Local Minima는 특정 영역 내에서 가장 낮은 함수 값을 가지는 지점을 의미, but 다른 영역에 더 낮은 값이 존재할 수도 있다!
```
- 차원의 저주에 대해 설명해주세요.
```python
   차원의 저주는 고차원 공간에서 발생하는 여러 가지 문제를 의미한다. 데이터 분석 및 머신러닝에서 데이터의 차원이 증가할수록 발생하는 현상으로, 학습 및 일반화 성능에 부정적인 영향을 미칠 수 있다.
   쉽게 정리하자면 변수가 늘어남에따라 차원이 커지면서 분석을 위한 최소한의 필요 데이터 건수가 늘어나면서 예측이 불안정해지는 문
   차원의 저주가 발생하는 이유
   1. 데이터의 희소성 (Sparsity) : 차원이 증가할수록 데이터 포인트들이 서로 멀리 떨어져 분포하게 된다
   2. 거리 측정의 신뢰도 감소 : 머신러닝의 여러 알고리즘 (특히 K-최근접, K-means)은 거리 측정을 기반으로 동작한다. 그러나 차원이 높아지면 데이터 포인트들 간의 거리가 점점 비슷해져서 유사성 측정이 어렵다
   3. 데이터 필요량의 증가 : 차원이 증가할수록 고차원 공간을 대표하기 위해 필요한 데이터의 양이 기하급수적으로 증가한다
   4. 모델의 복잡도 증가 : 차원이 증가하면 모델의 복잡도가 증가하여 과적합(overfitting)의 위험이 커진다
```
- dimension reduction기법으로 보통 어떤 것들이 있나요?
```python
   차원 축소 기법은 고차원 데이터의 차원을 줄여 데이터 분석을 용이하게 하고, 계산 효율성을 높이는 데 사용된다.
   데이터의 특성 (feature) 수를 줄임으로써 과적합을 방지하고, 해석 가능성을 높이며, 계산 비용을 줄일 수 있다.

   ⭐️ PCA (주성분 분석) : 데이터의 분산을 최대한 보존하는 방향으로 새로운 축을 생성하여 고차원 데이터를 저차원으로 변환하는 선형 차원 축소 기법
      - 데이터의 공분산 구조를 분석하여 주성분을 생성한다
      - 첫 번째 주성분은 데이터의 분산이 가장 큰 방향을 나타내며, 그 다음 주성분은 직교하는 방향에서 두 번째로 큰 분산을 나타낸다
      - https://m.blog.naver.com/angryking/222480031842 여기 참고하면 단 번에 이해 가능!
   
```
- PCA는 차원 축소 기법이면서, 데이터 압축 기법이기도 하고, 노이즈 제거기법이기도 합니다. 왜 그런지 설명해주실 수 있나요?
```python
   차원 축소 기법은 위에서 설명
   PCA는 고차원 데이터를 적은 수의 차원으로 압축하면서도 대부분의 중요한 정보를 보존하기에 데이터 압축 기법이라고도 한다
   PCA는 결국 데이터를 분산이 큰 방향으로 투영하기 때문에, 노이즈와 같은 작은 변동을 무시하는 효과가 있다!
```
- LSA, LDA, SVD 등의 약자들이 어떤 뜻이고 서로 어떤 관계를 가지는지 설명할 수 있나요?
```python
   LSA (Latent Semantic Analysis) : 잠재 의미 분석, LSA는 문서와 단어 사이의 관계를 분석하여 텍스트 데이터를 저차원 의미 공간에 매핑하는 기법, 이 과정으로 문서와 단어간의 잠재적 의미 구조 발견
   주로 SVD를 사용하여 문서-단어 행렬을 분해하고 차원을 축소
   LDA (Latent Dirichlet Allocation) : 텍스트 코퍼스 내의 문서들이 잠재적인 주제들의 혼합으로 구성되어 있다고 가정하는 주제 모델링 기법이다. 문서 내의 단어 분포를 기반으로 주제를 추론하고,
   문서들이 어떤 주제들로 구성되어 있는지를 학습한다. 확률적 모델을 사용하여 문서와 단어의 주제 분포를 추정한다.
   SVD (Singular Value Decomposition) : 특이값 분해, 행렬을 세 개의 행렬로 분해하는 선형대수적 기법. 주어진 행렬을 U(왼쪽 특이벡터), Σ(특이값 대각 행렬), V^T(오른쪽 특이벡터)의 곱으로 분해한다!
```
- Markov Chain을 고등학생에게 설명하려면 어떤 방식이 제일 좋을까요?
```python
   일상적인 예시로 시작해서 개념을 단계별로 확장하는 것이 좋다.
   예를 들어, 오늘이 맑음이면 내일도 맑음일 가능성이 높지만, 비가 올 가능성도 있다. 날씨는 현재 상태에 따라 다음 상태가 결정되지만, 그 이전 날들의 날씨는 고려하지 않는다고 가정해 볼 수 있다.
   여기서 중요한 점은 현재 상태만으로 다음 상태가 결정된다는 것이며, 이를 Markov Preperty(마르코프 성질)라고 한다.
   이렇게 상태(state)가 현재 상황에만 의존해서 바뀌는 과정을 바로 Markov Chain이라고 한다!
```
- SVM은 왜 반대로 차원을 확장시키는 방식으로 동작할까요? SVM은 왜 좋을까요?
```python
  - 데이터의 선형 분리가 어려운 저차원 공간에서의 문제를 해결하기 위해서 고차원으로 차원을 확장한다.
  - 데이터의 일부(서포트 벡터)에만 의존하여 결정 경계를 형성하므로, 다른 데이터들에 대한 과도한 최적화를 방지해 과적합 가능성을 줄임
  - 고차원에서도 좋은 일반화 성능을 유지하는 데 도움이 됨
```

- 다른 좋은 머신 러닝 대비, 오래된 기법인 나이브 베이즈(naive bayes)의 장점을 옹호해보세요.
  ```python
    - 나이브 베이즈는 매우 단순한 알고리즘으로, 계산이 빠르고 메모리 소모가 적음
    - 비교적 적은 양의 데이터로도 학습 성능이 높음
    - 조건부 확률에 기반한 모델이므로, 예측 결과를 해석하기가 쉬움
  ```
  
- 회귀 / 분류시 알맞은 metric은 무엇일까?
```python
  - 우선 회귀 문제에서는 실제 데이터와 모델의 예측값 사이의 차이를 기반으로둔 Metric을 활용
  - MSE(Mean Square Error, 평균제곱오차), RSS(Residual sum of Square, 단순 오차 제곱합), MAE(Mean Absolute Error, 평균 절대값 오차) 등이 있음
  - MSE (Mean Square Error, 평균제곱오차): 오차에 제곱이 되어 이상치를 잡아내는데 효과적임
  - MAE (Mean Absolute Error, 평균 절대값 오차): 변동치가 큰 지표와 낮은 지표를 같이 예측하는데 효과적임
  - 위 두 경우 모두 데이터의 크기에 의존한다는 단점이 존재
```

- Association Rule의 Support, Confidence, Lift에 대해 설명해주세요.
```python
  - Association Rules 란, items 사이의 관계를 나타내는 법칙을 찾는 방법
  <Frequent>
  - itemsets를 확인할 수 있는 지표
  - Frequent itemsets에는 Support threshold(Minimum support) 라는 일종의 '한계값' 이 필요
  - item의 빈도가 threshold 값을 넘기면 Frequent 하다고 할 수 있음

  <Support>
  - 전체 경우에서 집합 X와 Y를 모두 구매하는 경우의 수를 의미하는 지표
  - n(X∪Y) / n(ALL)

  <Confidence>
  - 집합 X를 구매하는 경우에서 Y 도 구매하는 경우의 비율, 즉 조건부 확률을 의미
  - (X와 Y를 모두 포함하는 경우의 수) / (X를 포함하는 경우의수) = n(X∪Y) / n(X)
  - 일반적으로 Confidence가 높을수록 해당 Association rule이 유용할 가능성이 높다고 판단

  <Interest>
  - Y를 구매하는 경우의 수와 X->Y를 구매하는 경우의 수를 비교하여, X->Y가 얼마나 흥미로운지 나타내주는 지표
  - 모든 사람들에게 Y를 추천했을때에 비해, X를 구매한 사람에게만 Y를 추천했을때, Y를 구매할 확률이 증가되는 정도
  - |conf(X -> Y) - support(Y)| 

  <Lift>
  - 직접적으로 X와 Y의 관계를 나타내주는 지표
  - Lift값이 1보다 크면 X와 Y의 relationship이 강하다는 것을 의미
  - conf(X -> Y) / support(Y)

  - Association Rules 분석 알고리즘에는 A-priori algorithm, FP-growth algorithm, PCY algorithm 등이 있음
  - A-priori algorithm: 전체 item 중에서 어느 정도 연관이 있을법한 item들을 추려주어 보다 계산시간을 줄여줄 수 있음
```

- 최적화 기법중 Newton’s Method와 Gradient Descent 방법에 대해 알고 있나요?
- 인공신경망(deep learning이전의 전통적인)이 가지는 일반적인 문제점은 무엇일까요?
```python
  - 기울기 소실 문제(Gradient Vanishing Problem): 층이 깊어질수록 기울기가 점점 작아져 앞쪽 층의 가중치가 거의 업데이트되지 않는 문제가 발생, 신경망이 깊어질수록 학습이 어려워지며 모델 성능이 떨어짐
  - 과적합 문제(Overfitting): 데이터가 부족하거나 학습 데이터가 특정 패턴에 치우쳐 있을 때는 일반화 성능이 낮아져 테스트 데이터에 대한 예측 성능이 저하
  - 연산 비용: 신경망의 층이 많아질수록 연산량이 기하급수적으로 증가
 ```

- ROC 커브에 대해 설명해주실 수 있으신가요?
```python
  - ROC 커브는 정답이 아닌 것을 정답으로 추론하는 확률을 x축으로 두고 이를 0부터 1로 키워가면서 정답을 정답으로 맞추는 확률을 y축으로 하여 나타낸 그래프를 의미
  - 이 그래프는 y=x를 기준으로 멀리 떨어질 수록 모델의 성능이 좋다고 판단할 수 있으며, ROC 커브의 하단 영역을 AUC 값으로 하여 ROC-AUC Score로 계산함
```

- 여러분이 서버를 100대 가지고 있습니다. 이때 인공신경망보다 Random Forest를 써야하는 이유는 뭘까요?
```python
  - 독립적인 결정 트리들로 구성되어 각 트리를 여러 서버에 분산하여 병렬 처리하기 쉬움
  - 인공신경망은 아키텍처 설계와 하이퍼파라미터 튜닝이 복잡하지만, Random Forest는 기본 하이퍼파라미터 설정에서도 안정적인 성능을 제공
  - 서버가 많아도 데이터가 적은 경우라면 Random Forest가 적은 데이터에서 더 좋은 성능을 보이기 때문에 효과적
  
- K-means의 대표적 의미론적 단점은 무엇인가요? (계산량 많다는것 말고)
```python
  - 거리 계산 방식을 사용하기 때문에 연속형 변수에 가장 최적이고, 범주형 변수에는 좋지 않음
  - 클러스터 크기나 밀집도가 서로 다르거나 원형이 아닐 경우 잘 작동하지 않으
  - 노이즈와 아웃라이어에 매우 민감하여 성능에 영향을 미침
  - 랜덤하게 정해진 초기 중심점 때문에 결과가 매번 달라질 수 있어 일관성이 부족
```

- L1, L2 정규화에 대해 설명해주세요.
```python
  - 정규화란 모델 복잡도에 대한 일종의 패널티로, Overfitting 을 예방하고 Generalization(일반화) 성능을 높이기 위한 방법
  - 모델에서 학습을 진행할 때, 학습 데이터에 따라 특정 weight의 값이 커지게 될 수있다. 이렇게 되면 과적합이 일어날 가능성이 아주 높은데, 이를 방지하기 위한 방법으로 L1, L2 정규화가 있다
  - L1 Norm 은 벡터 p, q 의 각 원소들의 차이의 절대값의 합
  - L2 Norm 은 벡터 p, q 의 유클리디안 거리(직선 거리)
```

- 앙상블 방법엔 어떤 것들이 있나요?
```python
  <배깅>
  - 부트스트랩(bootstrap)은 통계학에서 사용하는 용어로, random sampling을 적용하는 방법을 일컫는 말
  - random sampling을 통해 training data를 늘릴 수 있음
  - 배깅(Bagging)은 부트스트랩(bootstrap)을 집계(Aggregating)하여 학습 데이터가 충분하지 않더라도 충분한 학습효과를 주어 높은 bias의 underfitting 문제나, 높은 variance로 인한 overfitting 문제를 해결하는데 도움을 줌
  - 대표적인 알고리즘 : 랜덤 포레스트

  <부스>
  - 배깅과는 다른점은, 순차적으로 학습이 진행되는 것
  - boosting은 이전 분류기의 학습 결과를 토대로 다음 분류기의 학습 데이터의 샘플 가중치를 조정해 학습을 진행하는 방법
  - 먼저 생성된 모델을 꾸준히 개선해 나가는 방향으로 학습이 진행
  - 일반적으로 오답에 대해 높은 가중치를 부여하므로 정확도가 높지만 outlier에 취약할 수 있음

  <스태킹>
  - 개별 모델이 예측한 데이터를 다시 meta data set으로 사용해서 학습한다는 컨셉
  - Base Learner들이 동일한 데이터 원본 데이터를 가지고 그대로 학습을 진행했기 때문에 overfitting 문제가 발생
  - Cross Validation으로 overhfitting 방지
```

- Cross Validation은 무엇이고 어떻게 해야하나요?
```python
  - Cross Validation은 주어진 문제에 대하여 Train, Validation Set으로 나누어 모델의 성능을 체크함에 있어 나누어진 집합에 편향성을 가질수 있는 문제를 해결하기 위한 방법
  - Cross Validation 기법의 가장 대표적인 예로 K-fold Cross Validation을 설명드리면 우선 Train 데이터 셋을 k등분 하여 그 중 하나를 Validation Set으로 하여 검증
  - 또 다른 하나를 Validation Set으로 하여 검증하는 식으로 k번 반복하도록 하고 이를 평균내어 그 편향성을 줄임
```

- XGBoost을 아시나요? 왜 이 모델이 캐글에서 유명할까요?
```python
  - 각 트리가 오류를 줄이도록 훈련하는 방식으로, 다른 부스팅 알고리즘보다 더 강력하고 정확한 예측을 제공
  - 특히 데이터가 복잡하고 비선형적인 경우에도 강력한 성능을 발휘
  - 병렬 처리와 캐싱을 활용해 빠르게 학습할 수 있으며, 정교한 메모리 관리와 데이터 불균형 최적화 등으로 훈련 속도가 크게 향상
  - L1 및 L2 정규화를 통해 모델이 과적합되지 않도록 효과적으로 제어할 수 있음
  - 커스텀이 유연함
  - 다양한 하이퍼파라미터를 제공하여 정밀한 튜닝이 가능
```
  
- feature vector란 무엇일까요?
```python
  - 데이터 샘플의 특성(Feature)들을 벡터 형태로 표현한 것
  - 데이터의 특징을 수치화하여 정리한 일련의 값들의 집합

  --- 활용 예시 ---
  - 이미지 분류: 각 이미지의 픽셀 값을 특성으로 설정하여 벡터로 표현하고, 이 벡터가 이미지 분류 모델의 입력으로 사용됨
  - 사용자 행동 분석: 고객의 나이, 구매 횟수, 선호도 등 여러 특성 값을 모아 벡터로 만들어, 이를 기반으로 추천 시스템 등을 구축
```
- 50개의 작은 의사결정 나무는 큰 의사결정 나무보다 괜찮을까요? 왜 그렇게 생각하나요?
```python
  -
```
- 스팸 필터에 로지스틱 리그레션을 많이 사용하는 이유는 무엇일까요?
```python
  - 모델이 간단하여 구현하기 쉽고 이해하기 쉬움
  - 계산 비용이 낮아 대규모 데이터셋에서도 빠르게 학습 가능
  - 해석이 쉬움
```

</details>

<details>
<summary><a href="./answers/3-deep-learning.md"><strong>🧠 딥러닝</strong></a></summary>

- 딥러닝은 무엇인가요? 딥러닝과 머신러닝의 차이는?
```python
 딥러닝은 인공지능과 머신러닝의 하위 분야로, 인공 신경망을 기반으로 데이터에서 패턴을 학습하는 방식이 딥러닝이다
 특히 딥러닝은 신경망의 여러 계층을 쌓아올려 복잡한 패턴을 학습하는 데 초점을 맞추고 있다
 '딥'이라는 용어는 신경망의 계층의 깊다는 의미에서 비롯된 것으로, 각 계층이 서로 다른 수준의 추상화를 통해 데이터의 복잡한 특징을 점진적으로 학습하게 된다

 머신러닝과 딥러닝의 차이점은
 머신러닝은 딥러닝에 비해 비교적 단순한 알고리즘으로 특정한 패턴을 학습하며, 사람이 특징을 직접 추출한다
 딥러닝은 모델이 복잡하고 파라미터 수가 많기 때문에 GPU나 TPU 같은 고성능 연산 자원이 필요하다. 연산 자원과 시간이 많이 소요되지만 최적화된 하드웨어를 사용하면 좋은 성능을 낼 수 있다!
```
- Cost Function과 Activation Function은 무엇인가요?
```python
    비용 함수는 Loss Function이라고도 불린다. 모델이 예측한 값과 실제 값 사이의 차이를 측정하는 함수이다.
    딥러닝 모델이 학습하는 과정에서 이 함수를 최소화하는 것이 목표이다.
    즉 모델이 예측하려는 값이 실제 값에 더 가까워지도록 모델의 가중치와 편향을 조정한다

    활성화 함수는 신경망의 각 뉴런에서 입력을 받아, 다음 층으로 전달할 출력을 결정하는 함수이다
    비선형성을 추가하여 신경망이 복잡한 패턴을 학습할 수 있도록 돕는다
    Activation Function이 신경망에서 중요한 이유는 선형 모델이 아닌 비선형 모델을 형성하여 복잡한 패턴을 학습할 수 있도록 하기 때문이다 
```
- Tensorflow, PyTorch 특징과 차이가 뭘까요?
```python
   동적 vs 정적 그래프
   TensorFlow: 정적 그래프 기반으로 처음 설계되었지만, TensorFlow 2.x부터는 Eager Execution을 통해 동적 그래프를 지원한다다. 다만 여전히 대규모 프로젝트나 배포 시 정적 그래프 모드를 사용하는 경우가 많다.
   PyTorch: 처음부터 동적 그래프를 사용하여 그래프가 즉시 생성되고 실행된다. 이로 인해 코드 작성이 유연하고 디버깅이 용이하다.

   성능 및 최적화
   TensorFlow: TensorFlow는 TPU(구글의 AI 가속기) 지원이 강력하며, 대규모 분산 훈련 및 최적화에 유리하다. 특히 대규모 데이터셋을 처리할 때 성능 최적화가 잘 되어 있다.
   PyTorch: GPU 지원이 강력하며, 다양한 커스터마이징이 쉬워 연구 및 실험에 적합하다. PyTorch도 최근 TPU를 지원하기 시작했지만, TPU 최적화 측면에서는 아직 TensorFlow가 유리하다.
```
- Data Normalization은 무엇이고 왜 필요한가요?
```python
   데이터 정규화는 데이터의 크기와 범위를 조정하여 모든 특성(Feature)이 동일한 스케일을 갖도록 하는 과정이다. 일반적으로 정규화는 값의 범위를 0과 1로 압축하거나, 평균이 0이고 표준편차가 1인 정규 분포로 변환하는 방식으로 이뤄진다
   목적은 데이터를 구성하는 각 특성들이 서로 다른 스케일을 가지면, 거리 기반 알고리즘이나 그래디언트 기반 알고리즘이 특정 특성에 더 큰 영향을 받는다
   또한 정규화된 데이터는 모델이 더 빠르게 수렴하도록 도와준다. 이는 특히 경사하강법과 같은 최적화 알고리즘에서 중요하며, 학습 과정의 안정성도 개선된다
```
- 알고있는 Activation Function에 대해 알려주세요. (Sigmoid, ReLU, LeakyReLU, Tanh 등)
```python
  sigmoid: Sigmoid 함수는 입력값을 0과 1 사이의 값으로 변환
  출력 값이 항상 0과 1 사이로 제한되어 확률을 예측하는 문제에 적합하다
  입력이 작을 때는 거의 0에 가깝고, 입력이 클 때는 거의 1에 가까워지는 형태로 출력된다
  이진 분류 문제에서 확률 값을 나타내는 데 적합하다

  ReLU
  ReLU 함수는 0 이하의 입력에 대해서는 0을 출력하고, 0보다 큰 값에 대해서는 그대로 반환
  간단하면서도 매우 효율적인 비선형 함수이다
  계산량이 적고, 많은 네트워크에서 학습 속도를 개선하는 역할을 한다
  Gradient Vanishing 문제를 해결하여 학습 속도를 빠르게 한다
  입력값이 양수일 경우, 그래디언트가 일정하게 유지되어 깊은 네트워크에서 효과적이다

  Leaky ReLU
  Leaky ReLU는 ReLU 함수의 변형으로, 음수 입력에 대해 작지만 일정한 기울기를 갖도록 한다
  ReLU의 Dying ReLU 문제를 개선하려고 고안
  입력이 음수일 때에도 일정한 기울기를 갖기 때문에 뉴런이 "죽지" 않는다

  Tanh
  Tanh 함수는 입력 값을 -1과 1 사이로 변환
  출력이 -1에서 1 사이에 위치하여, 값이 0을 중심으로 대칭적이다
  Sigmoid 함수와 비슷하지만, 출력 범위가 -1에서 1로 더 넓어 Gradient Vanishing 문제가 약간 완화된다
  여전히 Gradient Vanishing 문제를 완전히 해결하지는 못하며, 깊은 신경망에서는 성능이 저하될 수 있다
```
- 오버피팅일 경우 어떻게 대처해야 할까요?
```python
     1. 더 많은 데이터 수집 : 학습 데이터가 부족할 경우, 모델이 데이터의 패턴을 과도하게 학습할 가능성이 크다. 더 많은 데이터가 있다면 모델이 데이터의 분포를 잘 학습할 수 있다!
                         따라서 데이터 수집을 통해 학습 데이터를 늘리거나, 데이터 증강(Data Augmentation) 기법을 사용하여 기존 데이터를 다양하게 변형해 데이터의 양을 늘린다
     2. 데이터 증강 : 이미지나 텍스트 등의 데이터에 변형을 가해 새로운 학습 데이터를 생성하는 기법이다
                   데이터의 다양성을 높여 모델이 특정 패턴에 과도하게 의존하지 않도록 돕는다

     3. 정규화 기법 : 모델의 가중치를 제한하여 과도한 학습을 방지하는 방법이다. 대표적인 정규화 기법에는 L1, L2 정규화가 있다
                   L2 정규화 : 가중치 제곱의 합을 손실 함수에 추가하여 가중치 크기를 줄이는 효과가 있다
                   L1 정규화 : 가중치의 절댓값 합을 손실 함수에 추가하여 일부 가중치 값을 0으로 만들어 모델을 간소화한다

     4. 드롭아웃: 학습 과정에서 일부 뉴런을 무작위로 제거(비활성화)하여 모델이 특정 뉴런에 의존하지 않도록 하는 기법이다
                드롭아웃 레이어를 네트워크 중간에 삽입하고, 학습 시 무작위로 선택된 비율의 뉴런을 비활성화한다.

     5. Early Stopping : 학습을 진행하다 보면, 일정 에폭 이후에 검증 손실이 더 이상 감소하지 않고 오히려 증가하는 현상이 발생할 수 있다. 이를 방지하기 위해 학습을 조기 종료하는 방법이다

     6. 교차 검증 (corss validation): 데이터를 여러 개의 폴드로 나누고, 각 폴드를 검증 세트로 사용하여 모델을 여러 번 학습시키는 방법이다. 이를 통해 모델이 데이터에 과적합되는지 점검할 수 있다
                                    대표적인 방법으로 K-Fold Cross Validation이 있다
                                    데이터를 K개의 폴드로 나눈 후, 각 폴드에 대해 학습과 검증을 수행하여 평균 성능을 측정한다
```
- 하이퍼 파라미터는 무엇인가요?
```python
     하이퍼파라미터는 크게 모델 하이퍼파라미터와 학습 하이퍼파라미터로 나눌 수 있다
     1. 모델 하이퍼파라미터
        모델의 구조나 복잡성응ㄹ 결정하는 하이퍼파라미터로 모델의 설계와 직접적으로 관련이 있다
        예시) 신경망의 레이어 수, 각 레이어의 뉴런 수, 활성화 함수, 커널 크기 및 필터 수
     2. 학습 하이퍼파라미터
        모델이 학습하는 방식을 제어하는 하이퍼파라미터로 학습의 효율성과 결과에 영향을 미친다
```

- Weight Initialization 방법에 대해 말해주세요. 그리고 무엇을 많이 사용하나요?
```python
     가중치 초기화는 신경망 학습에서 중요한 단계로, 모델의 가중치를 처음 설정하는 방법이다.
     올바른 가중치 초기화는 모델의 수렴 속도를 높이고, 과적합과 과소적합 문제를 방지하며
     Gradient Vanishing과 Exploding Gradient 문제를 완화하는 데 도움이 된다
     1. Zero Initialization: 모든 가중치를 0으로 초기화하는 방법이다
                             모든 뉴런이 동일한 출력을 생성하므로, 학습 과정에서 뉴런들이 서로 동일하게 업데이트되며 구별되지 않는 뉴런이 된다. 학습이 제대로 이루어지지 않다 -> 일반적으로 사용하지 않는다!
     2. Random Initialization : 가중치를 무작위로 초기화하는 방법으로, 모델이 특정 패턴에 편향되지 않도록 한다
                                단순히 랜덤한 값만으로 초기화하면, 활성화 함수의 비선형성에 따라 기울기 소실이나 폭발이 발생할 수 있다
                                특히 딥러닝 모델에서 층이 깊어질수록 이러한 문제가 심각해질 수 있다
     3. Xavier Initialization : 가중치를 신경망의 입력과 출력 뉴런 수에 따라 적절하게 분산시키는 방법이다.
                                Xavier 초기화는 주로 Sigmoid와 Tanh와 같은 대칭적 활성화 함수에 적합하다
     4. He Initialization : Xavier 초기화와 유사하지만, ReLU와 같이 비대칭적인 활성화 함수에 최적화된 방식이다. ReLU와 같은 함수는 활성화되는 뉴런이 일부에 불과하기 때문에, Xavier 초기화의 분산보다 더 큰 분산이 필요하다!
```
- 볼츠만 머신은 무엇인가요?
```python
    볼츠만 머신은 딥러닝이 한참 입에 오르내리기 전, 표현 학습 (Representation Learning)의 선조격 역할을 한 확률 모형이다
    에너지/엔트로피 개념을 비지도 학습과 융합
    상기 분류/회귀 모델은 추론 결과와 이미 알려져 있는 정답간의 차이를 줄이는 데 목표를 두지만, 볼츠만 머신은 생성 모델의 일종으로
    정답에 대한 확률 분포를 추정하는 비지도학습 모델이다!
```

- 뉴럴넷의 가장 큰 단점은 무엇인가? 이를 위해 나온 One-Shot Learning은 무엇인가?
```python
   뉴럴넷의 단점, 신경망은 많은 데이터가 있어야 한다. 그래야 일반화 성능이 높아진다
   데이터가 충분하지 않으면 과적합이 되어 새로운 데이터에 대한 성능이 저하된다
   이러한 단점을 극복하기 위해 나온 것이 one-shot learning이다
   One-shot learning은 매우 적은 적은 데이터만으로도 학습을 진행할 수 있는 기법을 의미한다
   One-shot learning의 핵심 아이디어
   1. 사전 학습된 특성 사용 : 모델이 미리 학습한 특성을 사용하여 새로운 클래스에 대해 빠르게 적응할 수 있도록 한다
   2. 거리 기반 학습 : 새로운 샘플이 주어지면 기존에 학습한 샘플과의 거리를 측정하여 유사한 클래스를 찾는 방식으로 학습한다
   3. 메타 러닝 : 모델이 학습하는 방법 자체를 학습하여 새로운 과제에 빠르게 적응하도록 하는 접근법이다
     
```
- 요즘 Sigmoid 보다 ReLU를 많이 쓰는데 그 이유는?
```python
     요즘 Sigmoid 함수보다 ReLU 활성화 함수를 많이 사용하는 주된 이유는 학습 효율성과 성능 향상 때문이다
     ReLU를 많이 사용하는 이유!
     1. 기울기 소실 문제
        Sigmoid와 같은 S자 형태의 활성화 함수는 입력값이 매우 크거나 작을 경우 츨력이 0 또는 1에 수렴하면서 미분값이 거의 0에 가까워지는 기울기 소실 문제가 발생한다
        이로 인해 역전파시 기울기가 점점 작아져서, 깊은 층에서는 거의 학습이 이루어지지 않는 문제가 생긴다
        ReLU는 입력이 양수일 때 기울기가 1로 일정하게 유지되므로, 기울기 소실 문제가 상대적으로 적어 깊은 신경망에서 효과적인 학습이 가능하다!
        따라서 ReLU는 더 빠른 수렴 속도를 보인다. 이는 기울기가 사라지지 않기 때문에 각 층이 더 빨리 학습할 수 있기 때문이다
```
  - Non-Linearity라는 말의 의미와 그 필요성은?
  ```python
     Non-Linearity(비선형성)란, 함수나 모델이 선형적이지 않음을 의미한다.
     즉, 입력과 출력 간의 관계가 직선이 아닌 곡선으로 표현되는 것을 뜻한다.
     신경망에서 Non-Linearity는 주로 활성화 함수를 통해 구현되며, ReLU, Sigmoid, Tanh 같은 활성화 함수들이 이러한 비선형성을 제공한다.

     그럼 왜 필요한가?
     현실 세계의 데이터는 선형적이지 않은 경우가 많다. 비선형성은 이러한 복잡한 관계를 학습할 수 있게 하여, 심층 신경망이 더 높은 표현력을 갖도록 한다
     만약 각 층이 선형 변환만 수행한다면, 여러 층을 쌓아도 결국 하나의 선형 변환으로 단순화된다. 즉 층을 쌓는 의미가 사라진다
     그러나 각 층에 비선형성을 추가하면, 각 층이 서로 다른 특징을 학습할 수 있게 되어 다층 구조의 장점을 제대로 활용할 수 있다
  ```
  - ReLU로 어떻게 곡선 함수를 근사하나?
  ```python
     ReLU는 개별적으로는 선형적이지만, 여러 개의 ReLU 뉴런을 조합하고 층을 쌓아 심층 구조를 이루면 비선형 함수를 근사할 수 잇다. 이를 통해 복잡한 곡선과 형태를 표현할 수 있게 된다
     심층 신경망에서는 각 층이 이전 층의 출력을 입력으로 받아 새로운 특징을 학습한다. ReLU 뉴런이 여러 층에 걸쳐 쌓여 있으면,
     각 층에서 입력을 다양한 선형 함수로 변환하고 다시 ReLU를 적용하면서 비선형성이 점차 강해진다
  ```
  - ReLU의 문제점은?
  ```python
     ReLU의 가장 큰 문제 중 하나는 Dying ReLU이다.
     이는 입력값이 0 이하인 경우 출력이 0이 되어 뉴런이 비활성화되는 문제이다
     역전파 과정에서 가중치가 조정되다가 일부 뉴런이 계속해서 0을 출력하게 되면, 해당 뉴런은 학습에 기여하지 않게 된다. 이 상태가 지속되면 뉴런이 죽은 상태로 남아버리고
     결국 해당 뉴런은 더 이상 활성화되지 않으므로 네트워크의 표현력이 떨어진다 -> 해결은 Leaky ReLU
  ```
  - Bias는 왜 있는걸까?
  ```python
     Bias는 신경망에서 각 뉴런에 더해지는 상수 값으로, 모델의 유연성을 높이고 더 복잡한 관계를 학습할 수 있도록 돕는다
     Bias는 모델이 데이터의 패턴을 더 잘 잡아낼 수 있도록 하고, 단순히 입력 가중치의 선형 조합만으로는 설명할 수 없는 데이터의 특성을 포착하도록 만들어 준다
  ```
- Gradient Descent에 대해서 쉽게 설명한다면?
```python
   함수의 최솟값을 찾는 방법으로, 기울기를 이용해 점차 내려가는 과정이다.
   이를 통해 모델의 오류를 최소화하고 최적의 매개변수를 찾을 수 있다
   현재 위치에서 주변 기울기를 확인
   기울기 방향으로 한 걸음 내려간다
   최솟값에 가까워질 때까지 반복한다
```
  - GD 중에 때때로 Loss가 증가하는 이유는?
  ```python
     Gradient Descent 과정에서 Loss가 때때로 증가하는 이유는 여러 가지 요인에 기인할 수 있다
     학습률이 너무 큰 경우 : 학습률이 지나치게 큰 경우, 매 스텝마다 가중치가 너무 크게 업데이트된다. 이로 인해 모델이 최적의 손실 값에 점진적으로 접근하기보다는 Loss함수에서 최소값을 지나쳐 오히려 증가하게 된다
     불안정한 가중치 초기화 : 가중치가 잘못 초기화되면 학습 초기에 Loss가 불안정하게 변동될 수 있다
  ```
  - Back Propagation에 대해서 쉽게 설명 한다면?
  ```python
    역전파는 신경망이 예측한 결과와 실제 값 사이의 차이를 계산하고, 그 차이를 최소화하기 위해 신경망의 가중치와 바이어스를 조정하는 과정이다
  ```
- Local Minima 문제에도 불구하고 딥러닝이 잘 되는 이유는?
```python
     고차원 공간의 특성 : 딥러닝 모델은 매우 고차원 공간에서 최적화가 진행된다. 차원이 높을수록 로컬 미니마가 아니라 안장점(saddle point)가 많아진다
     확률적 경사 하강법 : 딥러닝에서는 대부분 확률적 경사 하강법이나 미니배치 경사 하강법을 사용한다. 이러한 방법은 데이터 샘플에 따라 경사도가 조금씩 달라지는 특성을 이용하기 때문에, 모델이 로컬 미니마에 갇힐 확률을 줄여준다
```
  - GD가 Local Minima 문제를 피하는 방법은?
  ```python
     확률적 경사 하강법 이용 : 확률적 경사 하강법(SGD)는 전체 데이터셋이 아닌 미니배치 단위로 가중치를 업데이트한다. 미니배치 샘플이 랜덤하게 선택되기 때문에 경사도가 조금씩 달라지고, 이로 인해 경사 하강 경로에 노이즈가 추가
     이 노이즈 덕분에 로컬 미니마에 도달하더라도 노이즈의 영향을 받아 탈출할 가능성이 높아진다
     즉 SGD는 학습 과정에서 미세하게 경로를 흔들어주기 때문에 로컬 미니마보다 더 나은 방향으로 모델을 이동시킬 수 있다
  ```
  - 찾은 해가 Global Minimum인지 아닌지 알 수 있는 방법은?
  ```python
     학습이 충분히 진행된 후 손실 함수 값이 매우 낮고, 업데이트할 때마다 손실 값의 변화가 거의 없다면, 모델이 어느 정도 최적화된 지점에 도달했다고 추정할 수 있다
     학습이 수렵하면서 손실 함수의 변화율이 거의 0에 가까워진다면 이 지점이 최소값일 가능성이 높다 
  ```
- Training 세트와 Test 세트를 분리하는 이유는?
```python
  Training 세트와 Test 세트를 분리하는 이유는 모델의 일반화 성능을 평가하기 위해서이다
  구체적으로 모델이 새로운 데이터에 대해 얼마나 잘 작동하는지 확인하기 위함이다
```
  - Validation 세트가 따로 있는 이유는?
  ```python
     validation 세트를 따로 두는 이유는 모델의 최적화와 평가 과정에서 객관성을 유지하면서 하이퍼파라미터 튜닝과 모델 선택을 하기 위해서이다
     만약 Test 세트를 직접적으로 사용해 하이퍼파라미터를 튜닝하면 Test 세트에 과도하게 맞춰진 최적화가 이뤄질 수 있다
     Validation 세트를 활용하면 과적합을 방지할 수 있다 -> Early stopping
  ```
  - Test 세트가 오염되었다는 말의 뜻은?
  ```python
     Test 세트가 오염되었다는 말은 Test 세트의 데이터나 정보가 모델 학습 과정에 직,간접적으로 사용된 상황
     즉, Test 세트는 모델이 학습 중 한 번도 본 적이 없어야 하는데, 모델이 Test 세트에 포함된 정보에 노출되어 모델 성능이 과대평가될 위험이 있는 상태
  ```
  - Regularization이란 무엇인가?
  ```python
     정규화는 모델이 과적합되는 것을 방지하고, 새로운 데이터에 대해서도 좋은 성능을 유지할 수 있도록 하는 기법이다.
     과적합이 발생하는 이유는 모델이 학습 데이터의 노이즈나 불필요한 세부 패턴까지 과하게 학습하기 때문이다
     정규화는 이러한 불필요한 학습을 억제하여 모델이 더 단순하고 일반적인 패턴만을 학습하도록 유도한다
     L1 정규화 : Loss 함수에 가중치의 절댓값 합을 패널티로 추가
     L2 정규화 : Loss 함수에 가중치의 제곱 합을 추가
  ```
- Batch Normalization의 효과는?
```python
     배치 정규화는 각 층의 입력을 정규화하여 학습 과정에서 발생하는 내부 공변량 변화를 줄인다
     내부 공변량 변화는 네트워크의 파라미터가 업데이트되면서 각 층의 입력 분포가 바뀌는 현상을 의미한다
    정규화를 통해 각 층의 입력 분포가 일정하게 유지되므로, 모델이 새로운 데이터 분포에 적응하는 부담이 줄어들고 학습이 안정적으로 진행된다
```
  - Dropout의 효과는?
  ```python
     DropOut은 학습 과정에서 무작위로 일부 뉴런을 비활성화하여 모델이 특정 뉴런에 지나치게 의존하지 않고 다양한 경로로 학습하도록 유도한다
  ```
- SGD, RMSprop, Adam에 대해서 아는대로 설명한다면?
```python
     셋 다 딥러닝 모델을 학습시키기 위해 사용하는 최적화 알고리즘들로, 각기 다른 방식으로 모델의 가중치를 업데이트하여 손실을 최소화하는 방향으로 학습을 돕는다
     SGD는 확률적 경사 하강법 위에서 말함
     RMSprop는 적응형 학습률 알고리즘, 각 파라미터마다 학습률을 다르게 조정하여 학습의 효율성을 높인다
     Adam은 모멘텀과 RMSprop의 장점을 결합한 최적화 알고리즘, 현재 가장 널리 사용
     - 이동 평균을 통해 기울기 정보를 효율적으로 보정
     - 1차 모멘트와 2차 모멘트를 각각 기울기의 이동 평균으로 계산
     - 1차 모멘트는 변화의 방향을 반영하며, 2차 모멘트는 기울기의 크기를 반영
```
  - SGD에서 Stochastic의 의미는?
  ```python
     SGD에서 "Stochastic"이라는 용어는 무작위성(randomness) 또는 확률적 선택을 의미
     일반적인 경사 하강법(Gradient Descent)은 전체 데이터셋의 모든 샘플을 사용하여 손실 함수의 기울기를 계산하고 이를 바탕으로 모델의 가중치를 업데이트하는 방식
     그러나 이러한 방식은 데이터셋이 클 경우 계산량이 많아 학습 속도가 느려질 수 있다.
     반면, Stochastic Gradient Descent(SGD)는 전체 데이터셋을 사용하는 대신 데이터셋에서 임의의 하나의 샘플(혹은 작은 배치)을 무작위로 선택하여 그에 대한 기울기를 계산하고 가중치를 업데이트한다.
     이 방식은 각 업데이트가 데이터셋의 작은 일부만을 기반으로 하기 때문에, 가중치 업데이트에 무작위성이 더해진다!

      SGD의 무작위성(stochasticity)은 다음과 같은 몇 가지 특징을 제공한다:
        계산 효율성: 전체 데이터셋을 사용하는 대신 일부 샘플만으로 기울기를 계산하기 때문에 계산 비용이 낮아진다.
        국소 최적해 탈출 가능성: 무작위성이 추가되기 때문에 특정 지역의 최적점에 갇히지 않고, 더 나은 최적점을 찾을 가능성이 생긴다.
  ```
  - 미니배치를 작게 할때의 장단점은?
  ```python
     장점 : 메모리 사용량 감소, 빠른 업데이트 및 초기 수렴 가능성, 국소 최적해에서 탈출 가능성 증가
     단점 : 학습률 설정이 어려움
      - 계산 비용 증가 : 미니배치 크기를 줄이면 가중치 업데이트가 더 자주 발생하므로, 동일한 에포크(epoch)를 완성하는 데 더 많은 업데이트가 필요
  ```
  - 모멘텀의 수식을 적어 본다면?
  ```python
       모멘텀(Momentum) 최적화 알고리즘은 기울기 업데이트 과정에 이전 단계의 기울기를 반영하여, 진동을 줄이고 더 빠르게 최적점에 도달하도록 돕는 방법이다.
       모멘텀을 사용하는 경우, 매번 단순히 기울기만을 이용하는 대신 기울기의 지속적인 누적 효과를 반영해 가중치를 업데이트한다
  ```

- CNN, RNN, LSTM, GRU, tranformer (self-attention)에 대해 설명하시오!
```python
     CNN : 합성곱 레이어와 풀링 레이어를 쌓아 특징을 추출하고, 마지막에 Fully Connected 레이어로 분류 수행
       - 합성곱 연산을 통해 국소적인 특징을 추출, 이미지에서 중요한 패턴을 학습
     RNN: 순차적 데이터(시계열, 자연어) 처리
       - 이전 단계의 은닉 상태 (hidden state)를 다음 단계로 전달하여, 순차적인 데이터의 문맥과 흐름을 학습
       - 단점 : 기울기 소실 문제가 발생할 수 있으며, 긴 시퀀스 처리에 효율 떨어짐

     LSTM: 긴 시퀀스 데이터를 처리하고 장기 의존성을 학습
       - RNN의 변형으로 cell state와 게이트 구조 (입력 게이트, 출력 게이트, 망각 게이트)를 사용하여 장기적인 정보와 단기적인 정보 동시에 처리
       - 게이트 구조를 통해 필요 없는 정보를 걸러내고 중요한 정보만 저장하여 기울기 소실 문제 완화
     GRU : LSTM과 유사하게 긴 시퀀스 처리 but 구조가 더 단순하여 계산 비용이 낮다
        - 업데이트 게이트와 리셋 게이트를 사용하여 정보를 저장하고 삭제, Cell state가 없고 은닉 상태만을 사용
     Transformer : 시퀀스 데이터를 병렬로 처리하며 장기 의존성을 효과적으로 학습
          - self.attention과 feed forward network로 이루어진 인코더-디코더 구조, RNN을 사용하지 않으면서 시퀀스 데이터의 문맥과 관계 학습
          - 어텐션 점수는 각 단어가 다른 단어와 상호작용하는 정도, 이를 기반으로 중요도 조정하여 정보 통합. self attention으로 멀리 떨어진 단어 간의 의존성도 효과적으로 학습!
```

</details>


<details>
<summary><a href="./answers/5-network.md"><strong>🌐 네트워크</strong></a></summary>

- TCP/IP의 각 계층을 설명해주세요.
```python
   L1: 네트워크 엑세스 계층 - 실제 데이터 전송이 이루어지는 물리적인 계층 (이더넷, Wi-Fi 등의 네트워크 인터페이스로 전달)
   L2: 인터넷 계층 - 데이터 패킷을 목적지까지 전달하는 역할(IP 프로토콜 사용)
   L3: 전송 계층 - 데이터의 신뢰성 보장하는 계층(TCP와 UDP 프로토콜 사용)
   L4: 응용 계층 - 웹 브라우저, 이메일 등 사용자와 직접 상호 작용하는 애플리케이션 있는 계층(HTTP, FTP 프로토콜 사용)
```
</details>


<details>
<summary><a href="./answers/7-data-structure.md"><strong>🗂 자료구조</strong></a></summary>

- linked list
  - single linked list
  - double linked list
  - circular linked list
- hash table
- stack
- queue
  - circular queue
- graph

</details>

<details>
<summary><a href="./answers/8-algorithm.md"><strong>🔻 알고리즘</strong></a></summary>

- 시간, 공간 복잡도
- Sort Algorithm
  - Bubble Sort
  ```python
    인접한 두 요소를 비교하여 큰 값을 뒤로 보내는 방식으로 배열을 정렬한다.
    복잡도: O(n^2)
    특징: 구현이 간단하지만 효율성이 떨어져 잘 사용하지 x
  ```
  - Selection Sort
  ```python
     매번 배열에서 가장 작은 요소를 선택해 순서대로 배치한다.
     복잡도: O(n^2)
     특징: 간단하지만 대규모 데이터에서는 비효율적
  ```
  - Insertion Sort
  ```python
     배열의 요소를 하나씩 가져와서 정렬된 부분에 삽입하는 방식으로 정렬
     복잡도: O(n^2)
     특징: 거의 정렬된 배열에서는 효율적이며, 적은 데이터에 적합하다
  ```
  - Merge Sort O(nlogn) 
  ```python
     배열을 반으로 나누어 각각의 재귀적으로 정렬한 후, 병합하여 전체를 정렬
     복잡도: O(nlogn)
     특징: 안정적이며, 큰 데이터셋에 적합. Divide and Conquer 방식의 알고리즘이다
  ```
  - Heap Sort O(nlogn)
  ```python
     힙 자료구조를 이용하여 정렬하는 방식으로, 최대 힙이나 최소 힙을 이용한다
     복잡도: O(nlogn)
     특징: 제자리 정렬이 가능하지만, 안정적이지는 x
  ```
  - Quick Sort O(nlogn)
  ```python
     기준 요소(pivot)을 정해 이를 기준으로 작은 요소는 왼쪽, 큰 요소는 오른쪽으로 분할하여 재귀적으로 정렬한다
     복잡도: 평균은 O(nlogn), 최악 O(n^2)
     특징: 일반적으로 매우 빠르며, Divide and conquer 알고리즘
  ```
  - Counting Sort
  ```python
     값의 범위가 정해진 배열에서 각 값의 빈도를 세어 정렬한다
     1. 각 숫자가 몇 번 등장하는지 세어준다
     2. 등장 횟수를 누적합으로 바꿔준다
     복잡도: O(n+k)
     특징: 특정 범위에서만 사용 가능하며, 메모리 사용량이 크지만 안정적이다.
  ```
- Divide and Conquer
```python
   분할 정복은 작은 단위로 나누어 해결한 뒤, 이를 합쳐서 전체 문제의 해결책을 도출하는 알고리즘 설계 패턴이다. Divide -> Conquer -> Combine
   예시로는 Merge Sort, Quick sort, Binary Search 
```
- Dynamic Programming
```python
   Dynamic programming은 복잡한 문제를 작은 하위 문제로 나누어 해결하고, 이를 저장하여 중복 계산을 줄이는 방식으로 문제를 효율적으로 해결하는 알고리즘 설계 기법이다. 특히 최적화 문제에서 자주 사용된다!
   Optimal Substructure: 문제의 최적 해결책이 그 하위 문제들의 최적 해결책으로부터 만들어질 수 있는 구조를 말한다
   Overlapping Subproblems: 큰 문제를 작은 문제로 나눌 때 동일한 하위 문제가 여러 번 반복해서 등장한다
   Top-down, Bottom-up 방식으로 해결할 수 있다
   피보나치 수열 예시로 수업 때 설명하심!
```
- Greedy Algorithm
```python
   문제를 해결할 때 각 단계에서 가장 최선의 선택을 하는 방식으로 최종 해답을 찾아가는 알고리즘 설계 방법
   그리디 알고리즘은 전체적인 최적해를 보장하지는 않지만, 일부 문제에서는 빠르고 간단하게 최적해를 구할 수 있는 방법을 제공한다
```
- Graph
  - Graph Traversal: BFS
  ```python
   BFS는 시작 노드에서 인접한 노드들을 먼저 방문하고, 그 다음으로 인접 노드들의 인접 노드들을 차례로 탐색하는 방식이다.
   작동 방식:
   1. 탐색을 시작할 노드를 큐에 추가한다
   2. 큐에서 노드를 하나씩 꺼내어 해당 노드와 연결된 인접 노드들을 큐에 추가한다
   3. 큐가 빌 때까지 이 과정을 반복하며, 방문한 노드는 다시 탐색하지 않는다
   최단 경로: BFS는 최단 경로를 보장한다.
   시간 복잡도 : O(V+E)
  ```
  - Graph Traversal: DFS
  ```python
   DFS는 한 노드에서 시작하여 가능한 깊이까지 내려가며 탐색을 진행하고, 더 이상 갈 곳이 없으면 다시 돌아와 다른 경로를 탐색하는 방식이다.
   작동 방식:
   1. 탐색을 시작할 노드를 스택에 추가한다.
   2. 스택에서 노드를 하나씩 꺼내고, 해당 노드의 인접 노드를 다시 스택에 추가하여 깊이 탐색을 진행한다.
   3. 스택이 빌 때까지 이 과정을 반복하며, 방문한 노드는 다시 탐색하지 않는다.
   경로 탐색: DFS는 특정 경로를 탐색하거나, 특정 상태에 도달했을 때의 조건을 검사하는 데 유용하다.
   시간 복잡도 : O(V+E)
   스택을 사용하여 재귀 호출을 진행하여, 최대 깊이만큼 메모리 필요!
  ```
  - Shortest Path
    - Dijkstra
    ```python
      다익스트라 알고리즘은 가중치가 있는 그래프에서 하나의 시작 정점으로부터 다른 모든 정점까지의 최단 경로를 찾는 알고리즘이다.
      1. 초기화
       - 모든 정점에 대해 시작 정점으로부터의 최단 거리를 무한대로 설정. 시작 정점은 거리를 0으로 설정
       - 방문하지 않은 정점들의 집합인 우선순위 큐를 생성한다
      2. 정점 선택
       - 현재 방문하지 않은 정점들 중에서 시작 정점으로부터의 거리가 가장 짧은 정점을 선택한다
      3. 거리 업데이트
       - 선택된 정점의 인접한 이웃 정점들을 확인한다
       - 각 인접 정점에 대해, 시작 정점으로부터 현재 정점을 거쳐서 이웃 정점으로 가는 경로의 거리를 계산한다
       - 계산된 거리가 현재 저장된 시작 정점으로부터 이웃 정점까지의 거리보다 작으면, 해당 거리를 업데이트한다
      4. 방문 완료 처리
       - 선택된 정점을 방문 처리하고 우선순위 큐에서 제거한다
       - 모든 정점을 방문할 때까지 2~4단계를 반복한다!
    ```
    - Floyd-Warshall
    ```python
      Floyd Warshall은 모든 정점 쌍 간의 최단 경로를 찾는 알고리즘으로, 동적 계획법을 사용하여 그래프의 최단 경로 문제를 해결한다.
      이 알고리즘은 특히 음수 가중치를 가진 간선을 포함한 그래프에서도 최단 경로를 찾을 수 있으며, 음수 사이클도 감지할 수 있다.
    ```
    - Bellman-Ford
    ```python
      벨만 포드 알고리즘은 하나의 시작 정점에서 모든 다른 정점까지의 최단 경로를 찾는 알고리즘으로, 특히 음수 가중치 간선이 포함된 그래프에도 최단 경로를 구할 수 있는 특징이 있다.
      벨만 포드 알고리즘은 모든 간선을 최대 V-1번 반복하여 최단 경로를 갱신해 나간다. 이때 V는 정점의 개수이다.
    ```
  - Minimum Spanning Tree
    - Prim
    ```python
      Prim 알고리즘은 최소 신장 트리 (MST)를 찾기 위한 알고리즘으로, 정점 중심 방식으로 트리를 점진적으로 확장해 가며 MST를 구축하는 방식이다.
      MST는 모든 정점을 포함하면서 간선의 가중치 합이 최소가 되는 트리를 의미한다.
      1. 시작 정점 선택 : 임의의 시작 정점을 선택하여 초기 트리를 시작한다
      2. 가장 작은 가중치의 간선 선택 : 트리에 포함된 정점에서 연결된 간선 중 가중치가 가장 작은 간선을 선택한다. 이 간선의 도착 정점을 트리에 추가하여 트리를 확장한다.
      3. 트리의 확장: 현재의 MST에 포함된 정점 집합과 연결된 간선 중에서 가장 작은 가중치를 가진 간선을 선택하여 트리에 추가한다.
      4. 반복: 모든 정점을 포함할 때까지 즉 MST가 완성될 때까지 2~3 단계를 반복한다. 
    ```
    - Kruskal
    ```python
      Kruskal 알고리즘은 그래프에서 최소 신장 트리를 찾기 위한 알고리즘이다. 이 알고리즘은 간선 중심으로 동작하며, 모든 간선을 가중치 순으로 정렬한 후, 사이클을 형성하지 않는 간선을 하나씩 추가하여 MST를 구성하는 방식이다.
      1. 간선 정렬: 그래프의 모든 간선을 가중치의 오름차순으로 정렬한다
      2. 간선 선택 및 사이클 검증 : 가중치가 가장 작은 간선부터 하나씩 선택하여, 사이클이 발생하지 않는 경우에만 MST에 추가한다.
         2-1. 사이클이 발생하는지 확인하기 위해 Union-Find 자료구조를 사용한다.
              - Find 연산 : 두 정점이 같은 집합에 속하는지 확인한다.
              - Union 연산 : 두 정점을 같은 집합으로 병합하여, 동일한 트리로 연결되었음을 표시한다.
      3. 반복: 간선을 추가하여 MST에 포함된 간선의 수가 (정점 수 - 1)이 될 때까지 반복한다.
              - MST는 연결 그래프이므로 간선의 수는 정점 수 - 1이 된다.
    ```
  - Union-find
  ```python
      Union Find는 서로소 집합을 관리하는 자료구조이다. 서로소 집합 자료구소는 여러 개의 집합을 효율적으로 관리하고, 각 원소가 어느 집합에 속하는지 확인하거나, 두 집합을 하나로 합치는 연산을 빠르게 수행할 수 있도록 설계되었다.
      Union-Find 자료구조는 그래프에서의 사이클 검출, 최소 신장 트리 구성(Kruskal 알고리즘) 등 다양한 알고리즘에서 활용된다.
  ```
  - Topological sort 위상정렬
  ```python
     위상정렬은 유향 비순환 그래프 DAG(Directed Acyclic Graph)에서 정점들을 선행 순서에 맞춰 정렬하는 방법이다. DAG는 순환이 없는 방향 그래프로, 위상 정렬은 주로 작업 간의 우선 순위가 있는 작업 스케줄링 등에서 사용된다.
     위상 정렬은 다음과 같은 조건을 만족하는 정렬 방식이다.
     - 정점 u에서 v로 가는 간선이 존재한다면, 정렬 결과에서 u는 항상 v보다 앞에 위치해야 한다
     위상 정렬은 두 가지 방식으로 구현할 수 있다.
     - Kahn's Algorithm (BFS 기반)
     - DFS 기반 방법
  ```
</details>


<details>
<summary><a href="./answers/1-statistics-math.md"><strong> 🧑🏻‍🏫 Dr. Target Question </strong></a></summary>
  
- 선형대수에서 선형과 비선형에 대해 설명해주세요.
```python
  선형(Linear)이란 집합 A의 원소들에 대하여 각각 선형결합의 형태로 나타낼 수 있는 것
  즉, 집합 A의 원소 x1, x2, x3, ... xn에 대하여 각각 상수 a1, a2, a3, ..., an을 곱하여 더한 a1x1 + a2x2 + ... + anxn이 집합 A에 속하는 경우를 말함

  1차함수와 벡터 등은 선형을 나타내는 선형함수
  반대로, 2차 이상의 함수, 삼각 함수 등은 비선형함수
```

- 선형 독립과 선형 종속에 대해서 설명하세요.
```python
  <선형 독립>
  벡터 집합이 선형 독립이라는 것은, 집합에 포함된 어떠한 벡터도 다른 벡터들의 선형 조합으로 표현될 수 없다는 것을 의미한다.
  쉽게 말해: 벡터들이 선형 독립이라면, 그들 중 어느 벡터도 나머지 벡터들의 선형 조합으로 만들어질 수 없다
  의미: 선형 독립인 벡터들은 각기 다른 독립된 방향을 가리키며, 이 벡터들로 이루어진 공간에서 그 이상의 정보나 방향을 제공하지 않는 중복된 벡터가 포함되지 않았음을 나타낸다
 
  벡터 집합이 선형 종속이라는 것은, 집합에 포함된 적어도 하나의 벡터가 다른 벡터들의 선형 조합으로 표현될 수 있다는 의미이다.
  쉽게 말해: 벡터들이 선형 종속이라면, 어떤 벡터는 다른 벡터들의 선형 조합으로 만들어질 수 있다. 즉, 벡터 중 하나 이상이 다른 벡터에 의해 표현 가능한 중복된 정보나 방향을 제공한다.
  의미: 선형 종속인 벡터들은 독립적인 방향을 가지지 않으며, 공간에서 중복된 방향을 제공하는 벡터가 포함되어 있음을 나타낸다

  왜 이 개념이 중요?
  선형 독립인 벡터들로 기저 (basis)를 생성
  벡터 공간의 차원을 정의하는 데 필수
```

- tree
```python
  트리는 노드로 이루어진 자료구조
  루트 노드는 0개 이상의 자식 노드를 갖고 있다
  그 자식 노드 또한 0개 이상의 자식 노드를 갖고 있고, 이는 반복적으로 정의된다
  노드들과 노드들을 연결하는 간선(edge)로 구성되어 있다
  - 트리에는 사이클이 존재할 수 없다
```

  - binary tree
  ```python
  이진 트리는 각 노드가 최대 두 개의 자식 노드를 갖는 트리이다
  - 왼쪽 자식 노드(left child)와 오른쪽 자식 노드(right child)를 구분하여, 각 노드는 두 개 이하의 자식 노드를 갖는다
  - 이진 트리는 다양한 형태로 활용할 수 있으며, 특정한 성질을 갖는 이진 트리들이 존재한다
  ```
  - full binary tree
  ```python
  포화이진트리는 모든 노드가 정확히 두 개의 자식 노드를 갖거나, 자식이 없는 리프 노드로 구성된 이진 트리이다
  - 모든 리프 노드는 동일한 깊이 또는 레벨에 위치하며, 트리의 모든 노드가 꽉 차 있는 구조이다
  ```
  - complete binary tree
  ```python
   완전 이진 트리는 모든 레벨이 꽉 차 있는 상태로, 마지막 레벨을 제외하고 모든 레벨이 채워져 있다.
   - 마지막 레벨의 경우 노드들은 왼쪽에서 오른쪽 순으로 채워져 있다
   - 힙 자료구조는 일반적으로 완전 이진 트리 구조를 갖고 있다
  ```
  - bst(binary search tree)
  ```python
   이진 탐색 트리는 탐색과 정렬을 위해 사용되는 이진 트리이다. 각 노드는 다음과 같은 조건을 만족한다
   1. 왼쪽 자식 노드의 값은 부모 노드의 값보다 작다
   2. 오른쪽 자식 노드의 값은 부모 노드의 값보다 크다
   3. 이러한 규칙을 통해, 빠르게 값을 검색, 삽입, 삭제할 수 있다
  ```
  - AVL tree
  ```python
    AVL 트리는 스스로 규형을 맞추는 이진 탐색 트리로, 노드 간 균형을 유지하여 효율적인 연산을 보장한다
    - 각 노드의 왼쪽 및 오른쪽 서브트리 높이 차이는 1 이하로 유지된다
    - 만약 노드 삽입이나 삭제로 균형이 깨질 경우, 회전(rotation) 연산을 통해 트리의 균형을 맞춘다
    - AVL 트리는 이진 탐색 트리의 성능을 최적화하여 연산의 시간 복잡도는 O(logn)으로 유지한다
  ```
- heap(binary heap)
```python
 힙은 완전 이진 트리 형태의 자료구조로, 각 노드의 값이 특정 규칙을 만족하는 구조이다. 주로 최댓값 또는 최솟값을 빠르게 추출하기 위해 사용된다
```
  - min heap
  ```python
    최소 힙은 부모 노드의 값이 자식 노드의 값보다 작거나 같은 완전 이진 트리이다
    루트 노드는 트리 전체에서 가장 작은 값을 가지며, 자식 노드 또한 이 규칙을 따른다
    최소 힙은 최솟값을 빠르게 추출하는 데 유용하다
  ```
  - max heap
  ```python
    최대 힙은 부모 노드의 값이 자식 노드의 값보다 크거나 같은 완전 이진 트리이다
    루트 노드는 트리 전체에서 가장 큰 값을 가지며, 자식 노드 또한 이 규칙을 따른다
    최대 힙은 최댓값을 빠르게 추출하는 데 유용하다
  ```
- <b>RedBlack Tree</b> 🌲
```python
    Red-Black Tree는 이진 탐색 트리의 일종으로,
    삽입 및 삭제 시 트리의 균형을 유지하기 위해 각 노드를 빨간색 또는 검은색으로 색칠하여, 특정 규칙을 따라 높이가 균형 잡히도록 보장하는 트리입니다.
    1. 모든 노드는 빨간색 혹은 검은색이어야 합니다.
    2. 루트 노드는 검은색이다.
    3. 모든 NIL은 검은색이다. (NIL : null leaf, 자료를 갖지 않고 트리의 끝을 나타내는 리프 노드)
    4. 빨간색 노드의 자식은 반드시 검은색이다.
    5. NIL에서 루트 노드까지 가는 경로에서 만나는 검은색 노드의 개수가 같다.
```
- b+ tree
```python
    B+ 트리는 데이터베이스와 파일 시스템에서 널리 사용되는 트리 구조의 인덱스 자료구조이다
    B-트리의 변형으로, 효율적인 데이터 검색과 삽입/삭제를 위해 설계되었다
    B+ 트리의 특징

    노드의 구조
    B+ 트리는 내부 노드와 리프 노드로 구성된다
    내부 노드는 키만을 포함하고 자식 노드를 가리키는 포인터를 가지며, 실제 데이터는 포함하지 않는다
    리프 노드만이 데이터를 포함하며, 각 리프 노드는 정렬된 키와 데이터 값을 가지거나 포인터를 가진다

    리프 노드의 연결
    B+ 트리의 리프 노드들은 링크드 리스트처럼 연결되어 있습니다. 이를 통해 순차적으로 데이터를 탐색할 수 있다
    리프 노드에선 빠른 범위 탐색(range search)이 가능하다


    균형 트리 구조
    B+ 트리는 항상 균형을 유지하며, 모든 리프 노드는 같은 깊이에 위치한다
    새로 키를 삽입하거나 삭제할 때 트리의 균형을 유지하기 위해 노드를 분할하거나 병합할 수 있다

    효율성
    B+ 트리는 디스크 읽기/쓰기를 최소화하기 위해 설계되었다
    한 노드에 다수의 키를 저장할 수 있어 트리의 높이를 낮추고, 검색을 위해 필요한 디스크 접근 횟수를 줄인다

    탐색 과정
    검색 시, 루트 노드에서 시작해 내부 노드의 키를 비교하며 하위 노드로 내려간다
    최종적으로 리프 노드에 도달하면, 필요한 데이터나 키 값을 찾을 수 있다

```
- Validation
```python
  혹시 몰라서: 보안의 3대 요소는 무엇인가?
              CIA 트라이어드(CIA Triad)의 세 글자는 기밀성(Confidentiality), 무결성(Integrity) 및 가용성(Availability)을 의미

  컴퓨터 보안에서 Validation은 컴퓨터 시스템에서 입력된 데이터나 요청이 예상되는 형식, 값, 조건을 충족하는지 확인하는 과정이다
  보안 측면에서 validation은 시스템에 유효하지 않거나 악의적인 데이터가 유입되는 것을 방지해 보안을 강화하는 중요한 역할을 한다

  Validation의 주요 목적
  1. 입력 데이터의 무결성 보장
  2. 악성 데이터 차단, 보안 강화 : 올바르지 않은 입력을 차단하여 SQL Injection, XSS(크로스 사이트 스크립팅) 공격을 예방한다
  3. 시스템 안정성 유지

  Validation 기법
  1. 입력 길이 제한 : 입력 데이터의 길이를 제한해, 예외적으로 긴 데이터나 악성 스크립트가 포함될 가능성을 줄인다
  2. 데이터 형식 검증 : 데이터 형식을 정하고, 예상되는 형식과 일치하지 않는 경우 거부한다. 예를 들어, 이메일 주소나 전화 번호와 같은 특정 형식에 대한 검증을 수행
  3. 화이트리스트 기반 필터링 : 허용할 값의 목록(화이트리스트)을 정의하고, 그 값 이외의 입력은 거부한다
  4. 문자열 인코딩/이중 인코딩 방지 : 공격자가 특정 문자를 인코딩해 우회하려는 시도를 막기 위해 문자열을 일관된 방식으로 처리한다

  
```

</details>


---
