---
layout: post
title: "테일러 급수"
date: 2025-02-24 14:00:00 +0900
categories: jekyll
mathjax: true
---

### 2. 테일러 급수

$안녕하세요 ! $

$블로그의 두번째 글로 테일러 급수를 가져왔습니다.$ 

$이제는 함수를 주기함수로 표현해 볼건데요!$

$다음과 같이 표현할 수 있습니다.$

$$
f(t) = a_{0} + \sum_{n=1}^{\infty} \left( a_n \cos(n{\omega}t) +b_n \sin n{\omega}t \right)
$$

$$
a_0 = \frac{1}{T} \int_{0}^{T} y(t) \,dt
$$

$$
a_n = \frac{2}{T} \int_{0}^{T} y(t)\cos(n\omega t)\,dt
$$

$$
b_n = \frac{2}{T} \int_{0}^{T} y(t)\sin(n\omega t)\,dt
$$

$ 자\ 여기서\ a_0\ 와\ a_n,\ b_n가\ 왜\ 저렇게\ 나왔는지\ 알아보겠습니다. $

$ 일단\ f(t)는\ 주기함수입니다.\ 따라서\ f(t + T)\ =\ f(t)가\ 성립하죠. $

$ 그래서\ 0에서\ T까지\ 한주기의\ 평균값을\ 구한게\ a_0가\ 되겠네요. $

$ 마찬가지로\ 0에서\ T까지\ 한주기의\ sin(nwt)이나\ cos(nwt)의\ 크기를\ 구한게\ a_n이나\ b_n이\ 되겠습니다. $

$ 직교성\ 때문에\ 다른\ 주파수\ 성분은\ 다\ 사라지고\ 본인의\ 주파수만\ 남게\ 됩니다. $


$ 여기서 \sin(\theta) 와 \cos(\theta)를\ 오일러\ 공식을\ 통해\ 나타내\ 볼까요? $

$$
\cos(\theta) = \frac{e^{i\theta} + e^{-i\theta}}{2}
$$

$$
\sin(\theta) = \frac{e^{i\theta} - e^{-i\theta}}{2i}
$$


$ 주기함수는\ 반복되므로 \theta = {\omega}t로\ 나타낼\ 수\ 있습니다. $

$ 여기서 \sin(n{\omega}t)와 \cos(n{\omega}t)를\ 오일러\ 공식을\ 통해\ 나타내\ 볼까요? $

$$
\cos(n{\omega}t) = \frac{e^{in{\omega}t} + e^{-in{\omega}t}}{2}
$$

$$
\sin(n{\omega}t) = \frac{e^{in{\omega}t} - e^{-in{\omega}t}}{2i}
$$

$ 위의\ 식을\ 푸리에\ 급수에\ 대입해서\ 오일러\ 공식을\ 이용해\ 푸리에\ 급수를\ 나타내보면\ 다음과\ 같습니다. $

\[
y(t) = \sum_{n=-\infty}^{\infty} C_n e^{in\omega t}
\]

\[
C_n = \frac{1}{T} \int_0^T y(t) e^{-in\omega t} dt 
\]


