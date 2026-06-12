---
title: '5! ಅಂದ್ರೆ ಗೊತ್ತು, ಆದರೆ $\frac{1}{2}!$'
date: 2025-02-01
draft: false
math: true
---

ನಾವು ಶಾಲೆಯಲ್ಲಿ [ಫ್ಯಾಕ್ಟೋರಿಯಲ್](https://simple.wikipedia.org/wiki/Factorial) (Factorial) ಕಲಿತಿದ್ದೇವೆ.

$$5! = 5 \times 4 \times 3 \times 2 \times 1 = 120$$

$$4! = 24$$

$$3! = 6$$

ಇದು [ಸ್ವಾಭಾವಿಕ ಸಂಖ್ಯೆಗಳಿಗೆ](https://en.wikipedia.org/wiki/Natural_number) (Natural Numbers) ಚೆನ್ನಾಗಿ ಕೆಲಸ ಮಾಡುತ್ತದೆ. ಆದರೆ ಒಂದು ಕ್ಷಣ ಯೋಚಿಸಿ... $\frac{1}{2}!$ ಎಂದರೆ ಏನು? $2.7!$ ಎಂದರೆ? $-\frac{1}{2}!$ ಎಂದರೆ? ಇವುಗಳಿಗೆ ಅರ್ಥ ಇದೆಯೇ?

ಫ್ಯಾಕ್ಟೋರಿಯಲ್‌ನ ಒಂದು ಮುಖ್ಯ ಗುಣಲಕ್ಷಣ:

$$n! = n \times (n-1)!$$

ಉದಾಹರಣೆಗೆ,

$$5! = 5 \times 4!$$

$$4! = 4 \times 3!$$

ಗಣಿತಜ್ಞರ ಪ್ರಶ್ನೆ ಏನಂದರೆ:

> "ಈ ನಿಯಮವನ್ನು ಉಳಿಸಿಕೊಂಡೇ, ಫ್ಯಾಕ್ಟೋರಿಯಲ್ ಅನ್ನು ಸ್ವಾಭಾವಿಕ ಸಂಖ್ಯೆಗಳ ಹೊರಗೂ ವಿಸ್ತರಿಸಬಹುದೇ?"

ಅಂದರೆ,

$F(x+1)=xF(x)$ ಎಂಬ ಗುಣಲಕ್ಷಣವನ್ನು ಹೊಂದಿರುವ ಒಂದು "ಸತತ" (continuous) [ಫಂಕ್ಷನ್](https://simple.wikipedia.org/wiki/Function_(mathematics)) ಸಿಗಬಹುದೇ?

**ಈ ಪ್ರಶ್ನೆಗೆ ಉತ್ತರವಾಗಿ ಬಂದದ್ದು [ಗಾಮಾ ಫಂಕ್ಷನ್](https://simple.wikipedia.org/wiki/Gamma_function)** (Gamma Function). **ಇಲ್ಲಿಂದ ಮುಂದೆ ಓದಲು ನಿಮಗೆ [limit/ಲಿಮಿಟ್](https://simple.wikipedia.org/wiki/Limit_(mathematics)), [differentiation/ಡಿಫರೆನ್ಷಿಯೆಶನ್](https://simple.wikipedia.org/wiki/Derivative_(mathematics)), [integration/ಇಂಟಿಗ್ರೇಷನ್](https://simple.wikipedia.org/wiki/Integral) ಇತ್ಯಾದಿ ಗೊತ್ತಿರಬೇಕು ಆದರೂ ಸರಳವಾಗಿ ಇದೆ ಸ್ವಲ್ಪ ಗಣಿತ ಗೊತ್ತಿದ್ದರೆ ಕಷ್ಟ ಇಲ್ಲ.**

ಅದನ್ನು ಹೀಗೆ ವ್ಯಾಖ್ಯಾನಿಸಲಾಗುತ್ತದೆ:

$$\Gamma(x)=\int_0^\infty t^{x-1}e^{-t}dt$$

ಮೊದಲ ನೋಟಕ್ಕೆ ಇದು ಫ್ಯಾಕ್ಟೋರಿಯಲ್‌ಗೆ ಸಂಬಂಧವೇ ಇಲ್ಲದಂತೆ ಕಾಣಬಹುದು. ಆದರೆ ಇದರ ಅದ್ಭುತ ಗುಣಲಕ್ಷಣ

$$\Gamma(x+1)=x\Gamma(x)$$

$$n! = n \times (n-1)!$$

ಗಮನಿಸಿ!

ಇದು ಫ್ಯಾಕ್ಟೋರಿಯಲ್‌ನ ನಿಯಮದಂತೆಯೇ ಇದೆ. ಇದರಿಂದ $\Gamma(n+1)=n!$ ಎಂಬುದು ಸಾಬೀತಾಗುತ್ತದೆ. ಇದನ್ನು ಮುಂದೆ ನೋಡೋಣ ಮೊದಲು $\Gamma(x+1)=x\Gamma(x)$ ಇದು ಹೇಗೆ ಸಾಧ್ಯ ಎಂದು ನೋಡೋಣ….

$$\Gamma(x+1) = \int_0^\infty t^{(x+1)-1}e^{-t} \, dt = \int_0^\infty t^x e^{-t} \, dt$$

**ಇದಕ್ಕೆ [Integration by Parts](https://tutorial.math.lamar.edu/classes/calcii/integrationbyparts.aspx)/ಇಂಟಿಗ್ರೇಷನ್ ಬೈ ಪಾರ್ಟ್ಸ್ ಎಂಬ ವಿಧಾನ ಬಳಸಬೇಕು.**

$$\int u \, dv = uv - \int v \, du$$

u ಮತ್ತು dv ಕೆಳಗಿನಂತೆ

* $u = t^x \implies du = x t^{x-1} \, dt$
* $dv = e^{-t} \, dt \implies v = -e^{-t}$

ಮುಂದೆ ಏನು ನೀವು ಆಲೋಚಿಸಿ ;)

ಅಂದರೆ ಗಾಮಾ ಫಂಕ್ಷನ್ ಹೊಸದೊಂದು ವಸ್ತುವಲ್ಲ. ಇದು ಫ್ಯಾಕ್ಟೋರಿಯಲ್‌ನ ವಿಸ್ತಾರ ರೂಪ. ಅಂದರೆ

$$\Gamma(n+1) = n!$$

ಗಣಿತದಲ್ಲಿ ಪ್ರತಿಯೊಂದಕ್ಕೂ ಆಧಾರ/proof ಬೇಕು. $\Gamma(n+1)$ ಇದನ್ನು ಸಾಧಿಸಲು **[Mathematical Induction](https://simple.wikipedia.org/wiki/Mathematical_induction)/ಮ್ಯಾಥಮೆಟಿಕಲ್ ಇಂಡಕ್ಷನ್** ಎಂಬ ವಿಧಾನ ಬಳಸಬೇಕು ಇದು ಸ್ವಲ್ಪ ಬೇರೆ ಹಾದಿಯಲ್ಲಿ ಸಾಗುತ್ತದೆ ಅದಕ್ಕೆ $\Gamma(x+1) = x\Gamma(x)$ ಇದನ್ನು ಬಳಸಿ ಒಂದು ರೀತಿಯಲ್ಲಿ ಇದು ಹೇಗೆ ಸತ್ಯ ಎನ್ನುವುದರ ಕಲ್ಪನೆ(Intuition) ಬೆಳೆಸೋಣ.

$$\Gamma(n+1) = n \cdot \Gamma(n)$$

$$\Gamma(n+1) = n \cdot (n-1) \cdot \Gamma(n-1)$$

$$\Gamma(n+1) = n \cdot (n-1) \cdot (n-2) \cdot \Gamma(n-2)$$

$$\Gamma(n+1) = n \cdot (n-1) \cdot (n-2) \cdots 3 \cdot 2 \cdot 1 \cdot \Gamma(1)$$

$\Gamma(1) = 1$ ಇದನ್ನು ಫಂಕ್ಷನ್ ಗೆ ಬೆಲೆ ಹಾಕಿ ಪರೀಕ್ಷಿಸಬಹುದು.

$$\Gamma(n+1) = n \cdot (n-1) \cdot (n-2) \cdots 3 \cdot 2 \cdot 1 \cdot 1 = n!$$

ಹಾಗಾದರೆ ಕೆಲವು ಆಸಕ್ತಿದಾಯಕ ಮೌಲ್ಯಗಳನ್ನು ನೋಡೋಣ $\Gamma(n+1)=n!$ ಈಗ n ಗೆ ಒಂದೊಂದಾಗಿ ಬೆಲೆ ನೀಡೋಣ.

$$1! = \Gamma(2)=1$$

$$2! = \Gamma(3)=2$$

$$3! = \Gamma(4)=6$$

ಇಲ್ಲಿವರೆಗೆ ಎಲ್ಲವೂ ಪರಿಚಿತ. ಆದರೆ,

$$\left(\frac12\right)!=\Gamma\left(\frac32\right) = \frac{\sqrt{\pi}}{2} \approx 0.886$$

ಅಂದರೆ $\frac{1}{2}!$ ಕೂಡ ಚೆನ್ನಾಗಿ ವ್ಯಾಖ್ಯಾನಿಸಬಹುದು!

$\Gamma\left(\frac{1}{2}\right) = \sqrt{\pi}$ ಇದನ್ನು ಬೆಲೆ ಹಾಕಿ ನೀವು ನೋಡಿ ಸ್ವಲ್ಪ ಆಲೋಚನೆ ಮಾಡಬೇಕು!

ಇನ್ನೂ ಆಶ್ಚರ್ಯಕರವಾದದ್ದು

$$\left(-\frac{1}{2}\right)! = \Gamma\left(-\frac{1}{2} + 1\right) = \Gamma\left(\frac{1}{2}\right) = \sqrt{\pi}$$

ಅಂದರೆ ಋಣಾತ್ಮಕ ಭಿನ್ನರಾಶಿಗಳಿಗೂ (negative fractions) ಫ್ಯಾಕ್ಟೋರಿಯಲ್ ಅರ್ಥಪೂರ್ಣವಾಗಿರಬಹುದು. ಆದರೆ ಎಲ್ಲ ಋಣಾತ್ಮಕ ಸಂಖ್ಯೆಗಳಿಗೂ ಅಲ್ಲ (-1)! , (-2)! , (-3)! ಇವುಗಳಿಗೆ ಗಾಮಾ ಫಂಕ್ಷನ್ ಮೌಲ್ಯ ನೀಡುವುದಿಲ್ಲ. ಅಲ್ಲಿ ಅದು ಅನಂತದ ಕಡೆಗೆ ಹೋಗುತ್ತದೆ. ಹೇಗೆ ಕಾಮೆಂಟ್ ನಲ್ಲಿ ಹೇಳಿ.

ಹೀಗಾಗಿ, ಫ್ಯಾಕ್ಟೋರಿಯಲ್ ಎನ್ನುವುದು ಕೇವಲ $1 \times 2 \times 3 \times \cdots \times n$ ಎಂಬ ಸ್ವಾಭಾವಿಕ ಸಂಖ್ಯೆಗಳ ಗುಣಾಕಾರ ಮಾತ್ರವಲ್ಲ, ಅದರ ಹಿಂದೆ [ಎಲ್ಲಾ ವಾಸ್ತವ ಸಂಖ್ಯೆಗಳಿಗೂ](https://byjus.com/maths/real-numbers/) (Real Numbers) ವಿಸ್ತರಿಸಬಹುದಾದ ಒಂದು ಆಳವಾದ ಗಣಿತೀಯ ಕಲ್ಪನೆ ಇದೆ. ಅದನ್ನು ನಮಗೆ ತೋರಿಸಿದವರು ಮಹಾನ್ ಗಣಿತಜ್ಞ [ಲಿಯೋನಾರ್ಡ್ ಒಯ್ಲರ್](https://simple.wikipedia.org/wiki/Leonhard_Euler) (Leonhard Euler).

ಮುಂದಿನ ಪೋಸ್ಟ್‌ನಲ್ಲಿ ಒಯ್ಲರ್ ಗೆ ಈ ಕಲ್ಪನೆ ಹೇಗೆ ಬಂತು? ಗಾಮಾ ಫಂಕ್ಷನ್‌ನ ಇತಿಹಾಸವೇನು? ಎಂಬುದನ್ನು ನೋಡೋಣ.
![HTTP Diagram](../../images/euler.png)

