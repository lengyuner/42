
# Problem Set 2
## 161110014   
## 董冀峥  
## Jizheng Dong  
## Problem 1



### (a)


let $\lambda \geq 0$, then

$$
\begin{aligned} \operatorname{Pr}[X \geq t] &=\operatorname{Pr}\left[e^{\lambda X} \geq e^{\lambda t}\right] \\ & \leq \frac{E\left[e^{\lambda X}\right]}{e^{\lambda t}} \\ &=\frac{e^{\Psi_{X}(\lambda)}}{e^{\lambda t}} \\ &=e^{-\left(\lambda t-\Psi_{X}(\lambda)\right)} \end{aligned}
$$

Since the above formula holds for any $\lambda \geq 0$, there is


$$
\operatorname{Pr}[X \geq t] \leq \inf _{\lambda \geq 0} e^{-\left(\lambda t-\Psi_{X}(\lambda)\right)}=e^{-\Psi_{X}^{*}(t)}
$$

In particular, if $\Psi_{X}(\lambda)$ is successively differentiable, $\Psi_{X}'(\lambda)$ strictly increases monotonically, so if there exists $\lambda \geq 0$, satisfying $\Psi_{X}'(\lambda) = t$, then when $\lambda '< \lambda$, there is $t− \Psi_{X}'(\lambda ') > 0$. 
When $\lambda '> \lambda$ there is $t− \Psi_{X}'(\lambda ') < 0$. Therefore, the upper bound of $\Psi_{X}^{*}(t)$ is reached if and only if $λ$ is taken.

### (b)
First, let us calculate the moment function of the normal function

$$
\begin{aligned} \mathbf{E}\left[e^{\lambda X}\right] &=\int_{-\infty}^{+\infty} e^{\lambda x} \frac{1}{\sqrt{2 \pi} \sigma} e^{-\frac{(x-\mu)^{2}}{2 \sigma^{2}}} \\ &=\frac{1}{\sqrt{2 \pi} \sigma} \int_{-\infty}^{+\infty} e^{\frac{x^{2}-2\left(\mu+\lambda \sigma^{2}\right) x+\mu^{2}}{2 \sigma^{2}}} \\ &=\frac{1}{\sqrt{2 \pi} \sigma} \int_{-\infty}^{+\infty} e^{\frac{\left(x-\left(\mu+\lambda \sigma^{2}\right)\right)^{2}+\mu^{2}-\left(\mu+\lambda \sigma^{2}\right)^{2}}{2 \sigma^{2}}} \\ &=\frac{1}{\sqrt{2 \pi} \sigma} \int_{-\infty}^{+\infty} e^{\frac{\left(x-\left(\mu+\lambda \sigma^{2}\right)\right)^{2}+\mu^{2}-\left(\mu+\lambda \sigma^{2}\right)^{2}}{2 \sigma^{2}}} \\ &=e^{\mu \lambda+\frac{1}{2} \sigma^{2} \lambda^{2}} \frac{1}{\sqrt{2 \pi} \sigma} \int_{-\infty}^{+\infty} e^{\frac{\left(x-\left(\mu+\lambda \sigma^{2}\right)\right)^{2}}{2 \sigma^{2}}} \\ &=e^{\mu \lambda+\frac{1}{2} \sigma^{2} \lambda^{2}} \end{aligned}
$$

thus $\Psi_{X}, \Psi_{X}^{*}(t)$ are

$$
\begin{array}{c}{\Psi_{X}(\lambda)=\ln \mathbf{E}\left[e^{\lambda X}\right]=\mu \lambda+\frac{1}{2} \sigma^{2} \lambda^{2}} 
\\ 
{\Psi_{X}^{*}(t)=\sup _{\lambda \geq 0}\left(\lambda t-\left(\mu \lambda+\frac{1}{2} \sigma^{2} \lambda^{2}\right)\right)=\left\{\begin{array}{ll}{0} & {t<\mu} \\ {\frac{(t-\mu)^{2}}{2 \sigma^{2}}} & {t \geq \mu}\end{array}\right.}\end{array}
$$

So we can get a tail inequality by the Chernoff boundary

$$
\operatorname{Pr}[X \geq t] \leq\left\{\begin{array}{ll}{1} & {t<\mu} \\ {e^{-\frac{(t-\mu)^{2}}{2 \sigma^{2}}}} & {t \geq \mu}\end{array}\right.
$$

### (c)

Let us calculate the moment function of the Poisson distribution

$$
\begin{aligned} \mathbf{E}\left[e^{\lambda X}\right] &=\sum_{k=0}^{+\infty} e^{\lambda k} e^{-\nu} \frac{\nu^{k}}{k !} \\ &=e^{-\nu} \sum_{k=0}^{+\infty} \frac{\left(e^{\lambda} \nu\right)^{k}}{k !} \\ &=e^{\left(e^{\lambda}-1\right) \nu} \end{aligned}
$$

thus $\Psi_{X}, \Psi_{X}^{*}(t)$ are

$$
\begin{array}{c}{\Psi_{X}(\lambda)=\left(e^{\lambda}-1\right) \nu} \\ {\Psi_{X}^{*}(t)=\sup _{\lambda \geq 0}\left(t \lambda-\left(e^{\lambda}-1\right) \nu\right)=\left\{\begin{array}{ll}{0} & {t \leq 0} \\ {t(\ln t-\ln v)-(t-v)} & {t>0}\end{array}\right.}\end{array}
$$

So we can get a tail inequality by the Chernoff boundary

$$
\operatorname{Pr}[X \geq t] \leq\left\{\begin{array}{ll}{1} & {t \leq 0} \\ {e^{-t(\ln t-\ln v)+(t-v)}} & {t>0}\end{array}\right.
$$

### (d)

Let us calculate the moment function of Bernoulli distribution

$$
\mathbf{E}\left[e^{\lambda X}\right]=p e^{\lambda}+(1-p)
$$


thus $\Psi_{X}, \Psi_{X}^{*}(t)$ are

$$
\begin{aligned} \Psi_{X}(\lambda) &=\ln \left(p e^{\lambda}+(1-p)\right) \\ \Psi_{X}^{*}(t)=& \sup _{\lambda \geq 0}\left(t \lambda-\ln \left(p e^{\lambda}+(1-p)\right)\right) \end{aligned}
$$


When $t \in(p, 1)$, it abtains the maximum as $\lambda=\ln \frac{t(1-p)}{p(1-t)} \geq 0$. Therefore

$$
\Psi_{X}^{*}(t)=t \ln \frac{t(1-p)}{p(1-t)}-\ln \frac{1-p}{1-t}
$$

### (e)

Because $X_{i}$ is i.i.d. so we have 

$$
\begin{aligned} \Psi_{X}(\lambda) &=\ln \mathbf{E}\left[e^{\lambda X}\right]=\ln \mathbf{E}\left[e^{\lambda \sum_{i=1}^{n} X_{i}}\right]=\ln \mathbf{E}\left[\prod_{i=1}^{n} e^{\lambda X_{i}}\right] \\ &=\sum_{i=1}^{n} \ln \mathbf{E}\left[e^{\lambda X_{i}}\right]=\sum_{i=1}^{n} \Psi_{X_{i}}(\lambda) 
\end{aligned}
$$

$$
\begin{aligned} \Psi_{X}^{*}(t) &=\sup _{\lambda \geq 0}\left(t \lambda-\Psi_{X}(\lambda)\right)=\sup _{\lambda \geq 0}\left(t \lambda-n \Psi_{X_{i}}(\lambda)\right) \\ &=n \sup _{\lambda \geq 0}\left(\frac{t}{n} \lambda-\Psi_{X_{i}}(\lambda)\right)=n \Psi_{X_{i}}^{*}\left(\frac{t}{n}\right) \end{aligned}
$$

Let $X_{i}$ be a series of unrelated random variables obeying the Bernoulli distribution with parameter $p$, $X$ obeys the binomial distribution with the parameter $n$ and $p$, then $X=\sum_{i=1}^{n} X_{i}$ and

$$
\Psi_{X}^{*}(t)=n \Psi_{X_{i}}^{*}\left(\frac{t}{n}\right)=(n-t) \ln \frac{n-t}{n(1-p)}+t \ln \frac{t}{n p}
$$

So if $t > np$ the tail is estimated to be

$$
\operatorname{Pr}[X \geq t] \leq e^{-\left((n-t) \ln \frac{n-t}{n(1-p)}+t \ln \frac{t}{n p}\right)}
$$





If $Y_{i}$ obeys an independent geometric distribution with a parameter $p$, $Y=\sum_{i=1}^{n} Y_{i}$. Therefore

$$
\begin{aligned} \Psi_{Y_{i}}(\lambda) &=\ln \mathbf{E}\left[e^{\lambda Y_{i}}\right]=\ln \sum_{k=1}^{+\infty} e^{\lambda k}(1-p)^{k-1} p=\ln \frac{p}{1-p} \sum_{k=1}^{+\infty}\left(e^{\lambda}(1-p)\right)^{k} \\ &=\ln \frac{p e^{\lambda}}{1-e^{\lambda}(1-p)} \quad\left(\text { for } \lambda<\ln \frac{1}{1-p}\right) \end{aligned}
$$

When $t > 1$, $\Psi_{Y_{i}}^{*}(t)$ is

$$
\Psi_{Y_{i}}^{*}(t)=\sup _{0 \leq \lambda \leq \ln \frac{1}{1-p}}\left(t \lambda-\ln \frac{p e^{\lambda}}{1-e^{\lambda}(1-p)}\right)=t \ln \frac{t-1}{t(1-p)}-\ln \frac{p(t-1)}{1-p}
$$

So from the above discussion, we can get that when $t > n$

$$
P[Y \geq n] \leq \exp \left(-n \Psi_{Y_{i}}^{*}\left(\frac{t}{n}\right)\right)=\exp \left(\ln \frac{p(t-n)}{n(1-p)}-\frac{t}{n} \ln \frac{t-n}{t(1-p)}\right)
$$




















## Problem 2



First, we have 

$$
u=<u_{1},\dots,u_{n}>
\\
v^{(1)}=<v_{1}^{(1)},\dots,v_{n}^{(1)}>
\\
\vdots
\\
v^{(m)}=<v_{1}^{(m)},\dots,v_{n}^{(m)}>
$$

We define $X_{t}$ as
the t-th bit of $u, v^{(1)}, \dots, v^{(m)}$


$f(X_{1},\dots,X_{k})$ is the minimum distance between $u$ and $v^{(1)}, \dots, v^{(m)}$

$Y_{k}=E(f(X_{1},\dots,X_{k})|X_{1},\dots,X_{k-1})$

so that, $Y_{0},Y_{1},\ldots$ is a martingale with respect to the sequence $X_{0},X_{1},\ldots$, and for all $k\geq 1$

$|Y_{k+1}-Y_{k}|\leq 1$

According to Azuma's Inequality,

$$
Pr[|Y_{n}-Y_{0}|\geq t]\leq 
2\exp \left( -\frac{t^{2}}{2\sum_{k=1}^{n}1^{2}}\right)
$$
## Problem 3



## Problem 4






