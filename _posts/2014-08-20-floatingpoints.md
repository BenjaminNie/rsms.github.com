---
title: "Floating Points in C"
layout: post
description: "Throughout my university days, C was often the programming language of choice in my courses.  Two variations of number representations showed up repeatedly... (cont'd)"
---

Throughout my university days, C was often the programming language that was used to teach programming principles.  Two variations of number representations showed up repeatedly - integers and floats.  Integers and floats can be 32 or 64 bit, depending on the system, but integers can only represent whole numbers within a (relatively) small range. Meanwhile, floating points can represent both astronomically large and miniscually small numbers, much larger in range in comparison to an integer occupying the same number of bits. My curiousity got the best of me, and I decided ttheir differences in detail.

The results were both surprising and incredibly interesting. In a 32 bit unsigned integer, each bit simply represents a power of 2. The 0th bit would represent 2^0, while the 31st bit would represent 2^31. If it were a signed integer, the 31st bit would represent whether the integer is positive or negative, and the magnitude of the integer would be represented by the 30th(2^30) to the 0th(2^0) bit.

In a 32 bit float, there are three different sections that are responsible for generating the value - the mantissa, the exponent, and the sign. Their visual representation and equational relationship are seen here:

![MSG equation](/res/mse-eqn.png)
![32 bit mantissa representation](/res/32-bit-rep.png)

As you can see, there is 1 bit for the sign, 8 bits for the exponent, and 23 bits for the mantissa. The mantissa holds all the digits present in the number. For example, though 2.313 and 0.02313 differ in value, they have the same digits in the same order, so their mantissas are identical. The 8 bit exponent means a maximum exponent of 256, explaining the reason why floats have a significantly higher maximum value than their counterpart integers. Lastly, let me give some numerical examples. Say the mantissa is 23, the exponent 1, and the sign -, then value of the floating point would be 23^-1. In another example, if the mantissa is 3, the exponent is 52, and the sign +, then the value of the floating point would be 3^52. This explains why floats can reach such an astronomically high value, and why you should think twice next time you decide between using an int and a float.
