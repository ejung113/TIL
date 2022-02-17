# 딥러닝

## 1. 퍼셉트론

- 다수의 신호를 입력받아 하나의 신호를 출력
- 최적의 가중치를 학습하는 알고리즘



## 2. 신경망

- Multi layer perceptron(MLP) - 입력층, 은닉층, 출력층으로 이루어짐

1\) 소프트맥스(softmax)

- 지수함수의 output이 양수인 것을 이용하여 출력값을 0~1 사이의 값으로 출력 - 확률로 해석 가능

```python
def softmax(x):
  exp_x = np.exp(x)
  sum_exp_x = sum(exp_x)
  y = exp_x/sum_exp_x
  return y
```

2\) 에폭(epoch)과 배치(batch)

- 학습데이터가 많은 경우 한꺼번에 데이터 학습 가능하게 함
- 에폭은 데이터 전체를 한번에
- 배치는 묶음 데이터 단위로 나누어 학습

에폭(epoch)

```python
accuracy_cnt = 0
for i in range(len(x_test)):
  y = predict(model,x_test[i])
  p = np.argmax(y)
  if p == y_test[i]:
    accuracy_cnt += 1

print("Accuracy : {}".format(accuracy_cnt/len(x_test)))
```

배치(batch)

```python
network = init_network()
accuracy_cnt = 0
batch_size = 100

for i in range(0,len(x_train), batch_size):
  x_batch = x_train[i:i+batch_size]
  y_batch = predict(network,x_batch)

  p = np.argmax(y_batch,axis = 1)
  accuracy_cnt += np.sum(p ==y_train[i:i+batch_size])

print("Accuracy : {}".format(accuracy_cnt/len(x_train)))
```

