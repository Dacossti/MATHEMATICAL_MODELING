---
## Front matter
title: "Презентация по лабораторной работе №7"
subtitle: "Модель распространения рекламы"
author: "Озьяс Стев Икнэль Дани"

## Generic otions
lang: ru-RU

## Formatting
toc: false
slide_level: 2
theme: metropolis
header-includes:
- \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
- '\makeatletter'
- '\beamer@ignorenonframefalse'
- '\makeatother'
aspectratio: 43
section-titles: true
---

# Информация

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Озьяс Стев Икнэль Дани
  * студент группы НКНбд-01-21
  * Российский университет дружбы народов
  * <https://github.com/Dacossti>

:::
::: {.column width="30%"}

![](./image/ava.jpg)

:::
::::::::::::::

# Цели и задачи работы

## Цель лабораторной работы
 
Будем рассматривать модель распространения рекламной кампании.  Построим график решения распространения информации о товаре путем платной
рекламы и с учетом «сарафанного радио».

## Задание к лабораторной работе

1. Построить график распространения рекламы о салоне красоты
2. Сравнить эффективность рекламной кампании при $\alpha_1(t) > \alpha_2(t)$ и $\alpha_1(t) < \alpha_2(t)$
3. Определить в какой момент времени эффективность рекламы будет иметь максимально быстрый рост (на вашем примере).


# Процесс выполнения лабораторной работы

## Теоретический материал 
Организуется рекламная кампания нового товара или услуги. Необходимо, чтобы прибыль будущих продаж с избытком покрывала издержки на рекламу. Вначале расходы могут превышать прибыль, поскольку лишь малая часть потенциальных покупателей будет информирована о новинке. Затем, при увеличении числа продаж, возрастает и прибыль, и, наконец, наступит момент, когда рынок насытиться, и рекламировать товар станет бесполезным.

## Теоретический материал
Модель рекламной кампании описывается следующими величинами. Считаем, что $\frac{dn}{dt}$ - скорость изменения со временем числа потребителей, узнавших о товаре и готовых его купить, t - время, прошедшее с начала рекламной кампании, $n(t)$ - число уже информированных клиентов. Эта величина пропорциональна числу покупателей, еще не знающих о нем, это описывается следующим образом: $\alpha_1(t)(N- n(t))$, где N - общее число потенциальных платежеспособных покупателей, $\alpha_1(t) > 0$ - характеризует интенсивность рекламной кампании (зависит от затрат на рекламу в данный момент времени).

## Теоретический материал
Помимо этого, узнавшие о товаре потребители также распространяют полученную информацию среди потенциальных покупателей, не знающих о нем (в этом случае работает т.н. сарафанное радио). Этот вклад в рекламу описывается величиной $\alpha_2(t)(t) n(t) (N- n(t))$, эта величина увеличивается с увеличением потребителей узнавших о товаре. Математическая модель распространения рекламы описывается уравнением:

<p align="center">
  $\frac{dn}{dt} = (\alpha_1(t) + \alpha_2(t) n(t)) (N- n(t))$
</p> 

При $\alpha_1(t) > \alpha_2(t)$ получается модель типа модели Мальтуса.


В обратном случае, при получаем уравнение логистической кривой.


## Решение

Постройте график распространения рекламы, математическая модель которой описывается
следующим уравнением:

## Решение

1. $\frac{dn}{dt} = (0.73 + 0.000013 n(t)) (N- n(t))$ 

![График распространения рекламы №1 (Julia)](image/image1.png)

## Решение

2. $\frac{dn}{dt} = (0.000013 + 0.73 n(t)) (N- n(t))$

![График распространения рекламы №2 (Julia)](image/image2.png)



**Момент времени в который скорость распространения рекламы будет иметь максимальное значение = 0.06216763889523805**

## Решение

3. $\frac{dn}{dt} = (0.55sin(t) + 0.33sin(5t) n(t)) (N- n(t))$

![График распространения рекламы №3 (Julia)](image/image3.png)


# Выводы по проделанной работе

## Вывод

В результате проделанной лабораторной работы мы познакомились с моделем распространения рекламной кампании. Проверили, как работает модель в различных ситуациях, построили графики распрострения рекламы при данных условиях.

# Список литературы

1. [Модель распространения рекламной кампании](https://anylogic.help/ru/tutorials/system-dynamics/12-promotion-strategy.html)