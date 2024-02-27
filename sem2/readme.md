### Задание 1
Для тестирования были использованы следующие заначения параметра `hidden_state` : [32, 64, 128, 256] \
`hidden_state=32` - Сходимость достигается в среднем за ~66 итерации\
`hidden_state=64` - Сходимость достигается в среднем за ~53 итерации\
`hidden_state=128` - Сходимость достигается в среднем за 39 итераций\
`hidden_state=256` - Сходимость достигается в среднем за 28 итераций\
Таким образом, при увеличении количества параметров модели, необходимое для сходимости количество итераций уменьшается.\
![alt text](https://github.com/pgkgone/rl_course/blob/main/sem2/imgs/layer_size_relation.png)
### Задание 2
`256x256`
Сходимость достигается в среднем за ~37 итераций\
```
nn.Linear(obs_size, hidden_size),
nn.ReLU(),
nn.Linear(hidden_size, hidden_size),
nn.ReLU(),
nn.Linear(hidden_size, n_actions)
```
`lstmx256`
Сходимость достигается в среднем за ~47 итераций\
```
nn.LSTM(obs_size, hidden_size, batch_first=True)
nn.Sequential(
  nn.Linear(hidden_size, hidden_size),
  nn.ReLU(),
  nn.Linear(hidden_size, n_actions)
)
```
`lstmx256x256`
Сходимость достигается в среднем за ~52 итерации\
```
nn.LSTM(obs_size, hidden_size, batch_first=True)
nn.Sequential(
  nn.Linear(obs_size, hidden_size),
  nn.ReLU(),
  nn.Linear(hidden_size, hidden_size),
  nn.ReLU(),
  nn.Linear(hidden_size, n_actions)
)
```
Таким образом, наиболее эффективной является однослойная полносвязная модель.
![alt text](https://github.com/pgkgone/rl_course/blob/main/sem2/imgs/models_architecture.png)
### Задание 3

https://github.com/pgkgone/rl_course/assets/22062599/e14014e5-ab14-47ec-a867-7815dcb33279

