---
layout: post
title: "푸리에 변환"
date: 2025-02-25 10:00:00 +0900
categories: jekyll
mathjax: true
---

## **3. 푸리에 변환**

안녕하세요!  

이번에는 **푸리에 변환**에 대해 알아보겠습니다.  

푸리에 급수에서는 **주기함수**라는 조건이 있었습니다.  

하지만 **주기함수가 아닌 함수도 푸리에 급수로 표현할 수 있을까요?**  

만약 **주기를 무한대로 보내면** 어떨까요?  

즉,  $ lim_{T \to \infty} $

라고 극한을 취하면, 주기가 $ \infty $ 인 즉, **주기함수가 아닌 함수도 표현할 수 있습니다.**  

이것이 바로 **푸리에 변환**입니다. 🎯  

---

## **🔹 푸리에 변환 유도하기**

푸리에 급수는 다음과 같이 표현됩니다.

$$
x(t) = \sum_{n=-\infty}^{\infty} C_{n}e^{in\omega t}
$$

푸리에 계수 $ C_n $ 은 다음과 같이 정의됩니다.

$$
C_{n} = \frac{1}{T} \int_{0}^{T}x(t)e^{-in\omega t}dt = \frac{1}{T} \int_{-T/2}^{T/2}x(t)e^{-in\omega t}dt
$$

여기까지는 **푸리에 급수의 기본 공식**입니다.  

이제 **주기를 무한대로 극한을 취하여 주기함수라는 조건을 없애보겠습니다.**  

### **1️⃣ 주기를 무한대로 보내기**

$$
\lim_{T \to \infty} x(t) = \lim_{T \to \infty} \sum_{n = -\infty}^{\infty} [ \frac{1}{T} \int_{-T/2}^{T/2}x(t)e^{-in\omega t}dt ] e^{in\omega t}
$$

$$
\lim_{T \to \infty} x(t) = \lim_{T \to \infty} \sum_{n = -\infty}^{\infty} \left[ \int_{-T/2}^{T/2}x(t)e^{-in\omega t}dt \right] e^{in\omega t} \frac{1}{T}
$$

여기서 **대괄호 안의 항을 새로운 함수로 정의**하겠습니다.  

그리고 $ \omega = 2\pi f $ 를 적용합니다.

$$
\lim_{T \to \infty} \int_{-T/2}^{T/2}x(t)e^{-i2\pi t\frac{n}{T}}dt
$$

이를 정의하면,

$$
X(f) = \lim_{T \to \infty} \int_{-T/2}^{T/2}x(t)e^{-i2\pi t\frac{n}{T}}dt
$$

이제 극한을 적용하면, 푸리에 변환의 일반적인 형태가 나옵니다.

$$
X(f) = \int_{-\infty}^{\infty}x(t)e^{-i2\pi ft}dt
$$

---

### **2️⃣ 역변환 유도**

이제 $ X(f) $ 를 원래의 식에 대입해봅시다.  

마찬가지로 $ \omega = 2\pi f $ 를 적용합니다.

$$
x(t) = \sum_{n = -\infty}^{\infty} \lim_{T \to \infty} X(f) e^{i2\pi t \frac{n}{T}}\frac{1}{T}
$$

극한을 적용하면,

$$
x(t) = \int_{-\infty}^{\infty} X(f) e^{i2\pi ft} df
$$

---

## **🔹 푸리에 변환과 역변환 정리**

지금까지 $ x(t) $ 와 $ X(f) $ 를 유도했습니다.  

정리하면, **푸리에 변환과 역변환**은 다음과 같이 표현됩니다.  

### **푸리에 변환**
$$
\Large X(f) = \int_{-\infty}^{\infty} x(t)e^{-i2\pi ft} dt
$$

### **역푸리에 변환**
$$
\Large x(t) = \int_{-\infty}^{\infty} X(f)e^{i2\pi ft} df
$$

---

## **🔹 푸리에 변환의 수렴조건**

하지만 **모든 함수가 푸리에 변환될 수 있는 것은 아닙니다.**  

전체 적분이 **유한한 값으로 수렴**해야 합니다.  

그래서 **푸리에 변환이 존재하려면 다음 수렴 조건을 만족해야 합니다.**  

$$
X(f) = \int_{-\infty}^{\infty} x(t)e^{-i2\pi ft} dt \leq \int_{-\infty}^{\infty} x(t) dt \leq \int_{-\infty}^{\infty} |x(t)| dt < \infty
$$

즉,  
$$
\int_{-\infty}^{\infty} |x(t)| dt < \infty
$$
라면 푸리에 변환이 **존재**할 수 있습니다.

---

## **🚀 정리**

- **푸리에 급수는 주기함수만 표현 가능**하지만, 주기를 **무한대로 보내면 비주기 함수도 변환 가능**하다.

- 이를 통해 **푸리에 변환(Fourier Transform)이 정의**된다.

- **푸리에 변환 공식**

  $$
  X(f) = \int_{-\infty}^{\infty} x(t)e^{-i2\pi ft} dt
  $$
- **역푸리에 변환 공식**

  $$
  x(t) = \int_{-\infty}^{\infty} X(f)e^{i2\pi ft} df
  $$

- **푸리에 변환이 존재하려면** 

$$
\int_{-\infty}^{\infty} |x(t)| dt < \infty 
$$
