**How to compute the analytic gradient for arbitrarily complex function?**

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cded16d8-cde4-4d7f-b29c-67ef907333fb/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cded16d8-cde4-4d7f-b29c-67ef907333fb/Untitled.png)

input: x, W

hinge loss: compute data loss(Li)

L= regularization term+ data term

computational graph 로 function을 사용하는 이점?

- backpropagation을 사용할 수 있음
- chain rule을 이용해서 gradient를 계산할 수 있음

    ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a9437dcd-3221-4659-a223-1de3f121ca93/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a9437dcd-3221-4659-a223-1de3f121ca93/Untitled.png)

    - 복잡한 함수를 처리할 때 편리함 ex) CNN

**Backpropagation**

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/448e6ec1-cb13-470a-a37e-a9c6d980ce44/_2021-05-02__9.43.46.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/448e6ec1-cb13-470a-a37e-a9c6d980ce44/_2021-05-02__9.43.46.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5d414e01-3438-4de8-ad6f-47f70c0ed13a/_2021-05-02__9.44.33.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5d414e01-3438-4de8-ad6f-47f70c0ed13a/_2021-05-02__9.44.33.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/74fbccee-9637-46d4-bd24-746e7aace732/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/74fbccee-9637-46d4-bd24-746e7aace732/Untitled.png)

편미분 이용

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/df4b23ed-f588-4751-b786-2c0de72fc0d2/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/df4b23ed-f588-4751-b786-2c0de72fc0d2/Untitled.png)

위와 마찬가지로 거꾸로 수행→ chain rule

역으로 미분해가는 과정 backward pass

앞에서 부터 미분: forward pass

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/04001f39-6ab0-4911-ade6-5d9460b7cf62/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/04001f39-6ab0-4911-ade6-5d9460b7cf62/Untitled.png)

**sigmoid function

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6ac6fcc8-d420-47a6-a54d-f4bef8b817fa/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6ac6fcc8-d420-47a6-a54d-f4bef8b817fa/Untitled.png)

add gate: gradient 를 분배

mul gate: gradient를 숫자에 multiply→ switch

max gate: gradient= max

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bcde4561-59fc-486e-9426-c6993c3375bd/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bcde4561-59fc-486e-9426-c6993c3375bd/Untitled.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f3dc713d-dfcf-4373-9855-65a76dcbab50/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f3dc713d-dfcf-4373-9855-65a76dcbab50/Untitled.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6dbcdcdf-382b-4852-a181-1ec276806284/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6dbcdcdf-382b-4852-a181-1ec276806284/Untitled.png)
