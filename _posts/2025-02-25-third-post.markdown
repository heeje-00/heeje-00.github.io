---
layout: post
title: "푸리에 변환"
date: 2025-02-25 10:00:00 +0900
categories: jekyll
mathjax: true
---

## 3. 푸리에 변환

안녕하세요 !
이번에는 푸리에 변환에 대해 가져왔습니다. 
푸리에 급수에서 주기함수라는 조건이 붙었습니다. 
하지만 주기함수가 아닌 함수도 푸리에 급수로 표현할 수 있을까요? 
주기를 이렇게 $ \lim_{T \to \infty} $ 무한으로 보내볼까요? 그러면 주기가 $ \infty $ 인 
즉 주기함수가 아닌 함수를 나타낼 수 있습니다. 이것이 바로 푸리에 변환입니다. 

---

### 푸리에 변환 유도하기 

$$
x(t) = \sum_{n=-\infty}^{\infty} C_{n}e^{in\omega t}
$$
$$
C_{n} = \frac{1}{T} \int_{0}^{T}x(t)e^{-in\omega t}dt = \frac{1}{T} \int_{-T/2}^{T/2}x(t)e^{-in\omega t}dt
$$

여기까지 오일러 공식을 이용한 푸리에 급수의 표현 방법입니다. 
이제 주기를 무한대로 극한값을 취해서 주기함수라는 조건을 없애볼까요?


$$
\lim_{T \to \infty} x(t) = \lim_{T \to \infty}\sum_{n = -\infty}^{\infty}\left[\frac{1}{T} \int_{-T/2}^{T/2}x(t)e^{-in\omega t}dt \right]e^{in\omega t}
$$

$$
\lim_{T \to \infty} x(t) = \lim_{T \to \infty}\sum_{n = -\infty}^{\infty}\left[\int_{-T/2}^{T/2}x(t)e^{-in\omega t}dt \right]e^{in\omega t}\frac{1}{T}
$$

대괄호 안에 있는 부분만 따로 떼어내서 새로운 함수로 정의해 보겠습니다.
그리고 $ \omega = 2\pi f $ 를 적용시키겠습니다.
$$
\lim_{T \to \infty}\int_{-T/2}^{T/2}x(t)e^{-i2\pi t\frac{n}{T}}dt
$$

$$
X(f) = \lim_{T \to \infty}\int_{-T/2}^{T/2}x(t)e^{-i2\pi t\frac{n}{T}}dt
$$

$$
X(f) = \int_{-\infty}^{\infty}x(t)e^{-i2\pi ft}dt
$$

$ X(f) $ 를 원래의 식에 대입해보겠습니다.
마찬가지로 $ \omega = 2\pi f $ 를 적용시키겠습니다.

$$
x(t) = \sum_{n = -\infty}^{\infty} \lim_{T \to \infty} X(f) e^{i2\pi t \frac{n}{T}}\frac{1}{T}
$$

$$
x(t) = \int_{-\infty}^{\infty}x(t)e^{i2\pi ft}df
$$

지금까지 $ x(t) $ 와 $ X(f) $를 유도해 봤는데요.
정리하자면 다음과 같이 푸리에 변환과 역변환을 나타낼 수 있습니다.

$$
\Large X(f) = \int_{-\infty}^{\infty}x(t)e^{-i2\pi ft}dt
$$

$$
\Large x(t) = \int_{-\infty}^{\infty}x(t)e^{i2\pi ft}df
$$

---

### 푸리에 변환의 수렴조건

하지만 모든 함수를 푸리에 변환시킬 수 있는 것은 아닙니다.
전체 적분을 했을때 특정값으로 수렴해야겠죠?
그래서 수렴조건이 붙습니다.

$$
X(f) = \int_{-\infty}^{\infty}x(t)e^{-i2\pi ft}dt\ \leq \int_{-\infty}^{\infty}x(t)dt\ \leq \int_{-\infty}^{\infty} |x(t)|dt\ < \infty
$$
 
