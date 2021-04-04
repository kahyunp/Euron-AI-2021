“Loss function”: W에 대해 loss function을 보고 현재 classifier에서 가중치가 좋은지 아닌지 판단할 수 있음.
Loss over the dataset =  sum of loss over examples

linear classifier and it returns the prediction result (or prediction score) of the linear classifier.
SVM에서는 Hinge loss 사용. 특정 값이 나오거나 0

잘못된 카테고리들의 값을 더함
잘못된 카테고리와 올바른 카테고리를 비교하고 잘못된 카테고리보다 올바른 카테고리값이 충분히 크면 잘못된 카테고리보다 크다고 판단함
충분히 크다에 사용하느 개념safety margin)
질문 사항 정리 (구글링)
Why plus ‘1’ in the loss function? → impirical choice
We do not care the absolute score values, we only care the relative differences between the scores.
Minimum loss: zero (large differences for all classes), maximum loss: infinity (along with the hinge slope)
If initial weight W = 0, so all of the scores are zero. the 

 has a value of |class|-1 (it is because the 

 has the summation |class|-1 times, and if all scores from all class have similar value than each term outputs value ‘1’ .)
The reason excluding 

 term in the loss function is that, if we include the term, then, ‘1’ is always added in the 

. In order to make the minimum loss as zero, the term is excluded.
In the case we use mean instead of summation in the 

, that does not affect the term because the divider is always |class|-1, thus it is same with multiplying a constant at every time. (= rescaling). This is unnecessary because we do not care about the true value of the scores or of the loss.
If we use the squared term then, this would be a different classification problem.
W making L=0 is not unique. Imagine 2*W making L=0 also.
Regularization penalty (general machine learning)
L1 regularization(|W|)
L2 regularization (W^2)
Max norm regularization
Dropout
Batch normalization and stochastic depth 
L2 : prefers to spread that influence across all the different values in x.
 more robust
다양한 x 가 있을 때 특정 x 벡터에 의존하지 않고 전체 x 에 영향을 미침
L1  : W2< w1
L1 모델이 덜 복잡함
weight vector의 0의 개수로 복잡도를 판단
 => L1 L2중 뭘 쓸지는 문제 by 문제





Softmax classifier
Softmax function maps the final classification result into a probability space.
want to maximize the log-likelihood, or for a loss function to minimize the negative log-likelihood of the correct class:  

ex)  이미지의 정답이 고양이일때 :
the target probability distribution would put all of the probability mass on the cat class
cat class일 확률 -> 1 다른 클래스 ->0
What we want to do is encourage our computed probability distribution that’s coming out of this softmax function to match this target probability distribution to match this target probability distribution that has all the mass on the correct class.
 KL divergence, maximum likelihood 사용할 수 있음(what we really want is that the probability of the true class is high and as close to one.)
The loss in the softmax classifier 

Hinge loss and softmax (cross-entropy)


L1 regularization(|W|)


best W는 어떻게 찾을까?
Gradient method: follow the slope
x가 scalar 일때

multiple dimensions일 때
the gradient : vector of partial derivatives along each dimension=  Jacobian matrix
Numerical gradient method -naive 하고 approximation method
각 dimensiondml 아주 작은 h값을 빼
각 dimension에서 빼고 loss를 계산하는 과정을 반복함-> 엄청 느림
Analytic gradient method -defining gradient function and finding x
Gradient descent and stochastic gradient descent
Weights += -step_size * weights_gradient
Stochastic: sampling으로  gradient 구함
data_batch = sample(data, 256)
weights_gradient = evaluate_gradient (loss_func, data_batch, weights)
weights += -step_size * weights_gradient
