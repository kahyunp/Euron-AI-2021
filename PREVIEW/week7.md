1. Fancier Optimization

이전시간에 SGD를 배움-> 여러 단점으로 실제로 사용하기 어려움

단점1. 

학습속도가 느림


세로: 경사 급함 가로: 경사 완만

=> 지그재그로 움직이게 됨

Neural Network has many parameters -> 학습속도가 매우 느려짐

단점2.

Global minima 가 아닌 local minima, saddle point 에서 정지할 수 있음 (grdient 값이 0이어서)

Local minima / saddle point 근처이면 gradient 0에 가까워짐

단점3. 

매 스텝마다 정확한 gradient를 담을 수 없음



개선방안 1.

SGD + Momentum



방안2.

Nesterov Momentum


velocity 먼저 이용해 계산

방안3.

AdaGrad


방안4.

RMSProp


방안5.

Adam (momentum +RMSProp)


Learning Rate Decay



Second Order Optimization


hessian 이용 -> quadratic approximation

gradient descent 이용 x. 직접 계산으로 구함

시간 복잡도 때문에 잘 사용하지 않음

2. Model Ensembles

같은 학습데이터로 여러 독립적 모델 학습시키고 test할때 모델의 결과의 평균치를 내는 작업 <-여러모델관리해야하고 학습속도 저하

3. Regularization

Dropout:

forward pass에서 랜덤하게 node을 골라 0으로 설정하고 학습 =>모델이 단순해짐

