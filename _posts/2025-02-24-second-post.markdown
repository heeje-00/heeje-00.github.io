---
layout: post
title: "푸리에 급수"
date: 2025-02-24 14:00:00 +0900
categories: jekyll
mathjax: true
---

## 2. 푸리에 급수

안녕하세요!

블로그의 두 번째 글로 **푸리에 급수**를 가져왔습니다.

이제 **함수를 주기함수로 표현하는 방법**을 알아보겠습니다.

다음과 같이 표현할 수 있습니다.

$$
f(t) = a_{0} + \sum_{n=1}^{\infty} \left( a_n \cos(n\omega t) + b_n \sin(n\omega t) \right)
$$

$$
a_0 = \frac{1}{T} \int_{0}^{T} y(t) \,dt
$$

$$
a_n = \frac{2}{T} \int_{0}^{T} y(t) \cos(n\omega t) \,dt
$$

$$
b_n = \frac{2}{T} \int_{0}^{T} y(t) \sin(n\omega t) \,dt
$$

---

### **푸리에 급수 계수 유도**

자, 여기서 $ a_0 $, $ a_n $, $ b_n $ 이 왜 저렇게 나왔는지 알아보겠습니다.

- 일단 $ f(t) $ 는 **주기함수**이므로, $ f(t + T) = f(t) $ 가 성립합니다.
- 따라서, $ a_0 $ 는 **주기 $ T $ 에서 한 주기의 평균값**을 구한 것입니다.
- 마찬가지로, 한 주기의 $ \sin(n\omega t) $ 이나 $ \cos(n\omega t) $ 의 크기를 구한 것이 $ a_n $ 과 $ b_n $ 이 됩니다.
- **직교성(orthogonality) 원리**에 의해 **다른 주파수 성분은 모두 사라지고 해당 주파수만 남습니다.**

---

### **오일러 공식과 삼각함수 표현**

오일러 공식에 따라, $ \sin(\theta) $ 와 $ \cos(\theta) $ 는 다음과 같이 나타낼 수 있습니다.

$$
\cos(\theta) = \frac{e^{i\theta} + e^{-i\theta}}{2}
$$

$$
\sin(\theta) = \frac{e^{i\theta} - e^{-i\theta}}{2i}
$$

주기함수의 성질을 이용하면 $ \theta = \omega t $ 로 놓을 수 있습니다.  
따라서, $ \sin(n\omega t) $ 와 $ \cos(n\omega t) $ 를 오일러 공식으로 변환하면:

$$
\cos(n\omega t) = \frac{e^{in\omega t} + e^{-in\omega t}}{2}
$$

$$
\sin(n\omega t) = \frac{e^{in\omega t} - e^{-in\omega t}}{2i}
$$

---

### **복소형 푸리에 급수 표현**

위의 식을 푸리에 급수에 대입하여 **오일러 공식**을 이용하면, 푸리에 급수는 다음과 같이 정리됩니다.

$$
y(t) = \sum_{n=-\infty}^{\infty} C_n e^{in\omega t}
$$

$$
C_n = \frac{1}{T} \int_0^T y(t) e^{-in\omega t} dt
$$
