### Отчет 2. 
### Исследование метода Q-learning в среде Frozen Lake 

### 1. Исследование алгоритма `tabular Q learning`

В базовой версии алгоритма при GAMMA = 0.9 и ALPHA = 0.2 сходимость (mean reward > 0.80) достигается в среднем за 9086 итераций (Standard Deviation = 2718.0601).
<img src="imgs/determined.png"/>

В рандомизированной версии алгоритма при GAMMA = 0.9 и ALPHA = 0.2 сходимость (mean reward > 0.80) достигается в среднем за 4633.6 итераций (Standard Deviation	s =	1694.6481). Таким образом, рандомизированная версия оказалась болле робасной и быстро сходящейся.
<img src="imgs/determined-random.png"/>

В рандомизированной версии алгоритма при GAMMA = 0.9 и ALPHA = 0.1 сходимость (mean reward > 0.80) достигается в среднем за 12451.6 итераций (Standard Deviation	s =	8629.1679).
<img src="imgs/determined-random-alpha-01.png"/>

В рандомизированной версии алгоритма при GAMMA = 0.9 и ALPHA = 0.3 сходимость (mean reward > 0.80) достигается в среднем за 6609 итераций (Standard Deviation	s =	1607.4316).
<img src="imgs/determined-random-alpha-03.png"/>

В рандомизированной версии алгоритма при GAMMA = 0.9 и ALPHA = 0.5 сходимость (mean reward > 0.80) достигается в среднем за 4084.8 итераций (Standard Deviation	s =	1865.2507).
<img src="imgs/determined-random-alpha-05.png"/>

В рандомизированной версии алгоритма при GAMMA = 0.9 и ALPHA = 0.7 сходимость (mean reward > 0.80) достигается в среднем за 7549.4 итераций (Standard Deviation	s =	7119.8189).
<img src="imgs/determined-random-alpha-07.png"/>

**Вывод:** Таким образом, по полученным экспериментальным данным оптимальное значение параметра ALPHA = 0.5. 