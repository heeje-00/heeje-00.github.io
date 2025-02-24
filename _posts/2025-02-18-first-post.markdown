---
layout: post
title: "오일러 공식"
date: 2025-02-18 11:00:00 +0900
categories: jekyll
mathjax: true
---

## 1. 오일러 공식

안녕하세요!  

블로그의 첫 번째 글로 **오일러 공식**을 가져왔습니다.  
오일러 공식을 다루는 이유는 **주기함수를 나타내는 데 필요한 기본적인 공식이기 때문**입니다.  
우리는 앞으로 **푸리에 변환**을 통해 일반적인 함수를 **주기함수로 변환**시키고,  
더 나아가 **주파수 영역에서 함수를 표현**할 것입니다.  

따라서, **오일러 공식이 무엇인지 알아보고 이를 이용해 함수를 주기함수 형태로 변환**해 보겠습니다.  

---

### **오일러 공식**

$$ 
\Large e^{i\theta} = \cos(\theta) + i\sin(\theta)
$$

이 공식은 복소평면 위에서 **원의 방정식을 한 번 미분하여 쉽게 증명**할 수 있습니다.  

### **오일러 공식 증명**

![복소평면](/assets/images/O1.jpg)

복소평면에서 다음과 같은 식을 정의합시다.

$$
z = \cos(\theta) + i\sin(\theta)
$$

이를 한 번 미분하면:

$$
\frac{dz}{d\theta} = -\sin(\theta) + i\cos(\theta)
$$

여기서 \( z \)와 \( \frac{dz}{d\theta} \)의 관계를 정리하면:

$$
\frac{dz}{d\theta} = iz
$$

이제 양변을 적분해 줍니다.

$$
\frac{dz}{z} = i d\theta
$$

$$
\int \frac{dz}{z} = \int i d\theta
$$

$$
\ln(z) = i\theta + C
$$

$$
z = z_0 e^{i\theta}
$$

여기서 \( \theta = 0 \)일 때, \( z = 1 \)이므로 \( z_0 = 1 \) 입니다. 따라서:

$$
\Large z = e^{i\theta} = \cos(\theta) + i\sin(\theta)
$$

---

### **오일러 공식의 직관적인 의미**

오일러 공식의 의미를 직관적으로 이해하기 위해 **자연상수 \( e \)의 정의**를 먼저 살펴보겠습니다.

$$
e = \lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n
$$

여기서 \( e^x \)는 다음과 같이 정의됩니다.

$$
e^x = \lim_{n \to \infty} \left(1 + \frac{x}{n}\right)^n = \left[ \lim_{{n \to \infty}} \left( 1 + \frac{x}{n} \right)^{n/x} \right]^x
$$

이제 \( x \)를 \( i \)로 바꿔보면:

$$
e^i = \lim_{n \to \infty} \left(1 + \frac{i}{n}\right)^n
$$

이제 우리는 **오일러 공식이 복소평면을 이해하는 데 핵심적인 역할을 하며, 주기함수를 편리하게 나타내는 강력한 도구**가 된다는 것을 알 수 있습니다! 
