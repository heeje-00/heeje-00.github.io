---
layout: post
title: "오일러 공식"
date: 2025-02-18 11:00:00 +0900
categories: jekyll
mathjax: true
---

### 1. 오일러 공식

안녕하세요 ! 

블로그의 첫번째 글로 **오일러 공식**을 가져왔습니다.
오일러 공식을 가져은 이유는 주기함수를 나타내는데 필요한 기본적인 공식이기 때문입니다.
우리는 앞으로 푸리에 변환을 통해 일반적인 함수를 주기함수로 변환시키고
더 나아가 주파수 영역에서 함수를 표현할 것입니다.

따라서 오일러 공식이 무엇인지 알아보고 함수를 주기함수 형태로 나타내 보겠습니다. 

#### 오일러 공식 

$$ 
\Large e^{i\theta} = \cos(\theta) + i\sin(\theta)
$$

위 공식은 복소평면 위에서 정의된 원의 방정식을 한번 미분해주면 쉽게 증명할 수 있습니다. 

![복소평면](/assets/images/O1.jpg)

$$
z = \cos(\theta) + i\sin(\theta)
$$

z를 한번 미분해준다

$$
\frac{dz}{d\theta} = -\sin(\theta) + i\cos(\theta)
$$


여기서 z와 z'의 관계를 구하면 어떻게 될까?


$$
\frac{dz}{d\theta} = iz
$$


적분하기 위해 정리해주면

$$
\frac{dz}{z} = id\theta
$$


$$
\int \frac{dz}{z} = \int id\theta
$$


$$
ln(z) = i\theta + C
$$


$$
z = z_{0}e^{i\theta}
$$


따라서 $\textstyle \theta 가 0일때 z = 1 이므로 z_{0} = 1 $


$$
\Large z = e^{i\theta} = \cos(\theta) + i\sin(\theta)
$$

여기서 끝내지 말고 직관적인 오일러 공식의 의미를 보면 좋을 것 같습니다.

먼저 자연상수 e의 정의를 봅시다.

$$
e = \lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n
$$

여기서 자연상수 e에 x승이라는 것은 무엇을 의미하는지 봅시다.

$$
e^x = \lim_{n \to \infty} \left(1 + \frac{x}{n}\right)^n = \left[ \lim_{{n \to \infty}} \left( 1 + \frac{x}{n} \right)^{n/x} \right]^x
$$

따라서 x를 i로 바꿔주면

$$
e^i = \lim_{n \to \infty} \left(1 + \frac{i}{n}\right)^n
$$

오일러 공식은 복소평면을 이해하는데 기본적인 공식이 되고 주기함수를 편하게 나타낼 수 있게 됩니다 !