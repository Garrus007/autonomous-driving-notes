[[Advanced, Contemporary Control.pdf]], p. 1213

## Заметки к статье
[[Autonomous delivery]]

Рассматривается аппаратное и программное устройство робота для доставки внутри помещений. В общем, ничего интересного и никакой конкретики.

Аппаратное устройство:
- Сенсоры: 1D [[LiDAR]], 2x Realsense D415 [[Depth camera]], ультразвуковые дальномеры
- Привод: всенаправленные колеса, DC-мотор-редукторы, энкодеры
- Управление: STM32, PWM, Polulu
- Питание: LiPo, 54 Ah, 24 V. Автономное время: 12-15 ч.
- Полезная нагрузка: 30 кг

Софт:
1. Построение карты:
используется [[SLAM]] gmapping с LiDAR. Построение либо вручную, либо автоматически, алгоритм Fronier Exploration.
2. Локализация: Kalman, LiDAR + wheel odometry
3. Робот может работать с лифтами и этажами. На кажлом этаже своя карта. Общая карта представлена как направленный граф, где узлы - этажи с картами, а ребра - возможность перемещения

Note: пдфка - тезисы с конференции, там просто дофига всего. И хардкорный матан, и антропоморфные, и слам с планированием, и всякий MPC итп.

