# Traversability
"Проходимость". Разные способы определять, где робот может пройти, а где нет. 

Определение проходимости для неплоской поверхности (см. [[Sidewalks robot]], [[Autonomous delivery]]). 

Классификация:
- Classification (можно проехать/нельзя)
- Regression (стоимость или иная метрика проезда)

1. Строим 3D модель поверхности, используем регрессию или классификацию классическими методами: определяем наклон, высоту, stddev [1]. Тут нам нужна большая разрешающая способность (?)  трехмерной карты. Классический [[LiDAR]] не подойдет. [[LiDAR Solid State]], [[Depth camera]] или стерео/моно [[Depth DNN]]?
2. Всякий machine learning

## Opens
- Нужна ли нам регрессия или хватит классификации?

## References:

