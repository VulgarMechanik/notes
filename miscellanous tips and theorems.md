# **MISCELLANOUS TIPS AND THEOREMS**

$$
\newcommand{\bf}[1]{\boldsymbol{#1}} \\
\newcommand{\red}[1]{\color{red}{#1}}\\
\newcommand{\W}{\mathbb{W}}\\
$$

[toc]

***

## Binomial Expansion 

$$
\begin{aligned} &\text{Since for } |x|<1, \quad &&(1+x)^n=1+nx+\frac{n(n-1)}{2!}x^2+\cdots_\infty\\ &\text{for } |x|>1, &&(1+x)^n=x^n\left(1+\frac1x\right)^n=x^n\left(1+\frac{n}{x}+\frac{n(n-1)}{2!\ x^2}+\cdots_\infty \right) \end{aligned}
$$

---

## Square Roots

For any positive number $a$, there are exactly 2 numbers, $x$ and $-x$, whose square is $a$. The square root of a number $a$, denoted by $\sqrt a$, is defind as the *positive* number whose square is equal to $a$. Thus, by definition, 
$$
\bf{ \sqrt{x^2}=|x| }
$$
**Note**: 

1. $+\sqrt5$ is the *positive of the square root of 5*, NOT *positive square root of 5*

2. $-\sqrt5$ is the *negative of the square root of 5*, NOT *negative square root of 5*

   

**Using the square root operator for solving equations:** 
$$
\begin{alignat}{5}
& (1+x)^2 &&=5 \\
\text{Incorrect method:}\qquad& 1+x     &&=\pm \sqrt5  \\
& x       &&=-1\pm \sqrt5 \\
\\
& (1+x)^2 &&=5 \\
\text{Correct method:}\qquad& |1+x|     &&= \sqrt5  \\
& (1+x)    &&=+\sqrt5 \ &&&or \qquad &&&&(1+x)&&&&&=-\sqrt5 \\
&x&&=-1+\sqrt5 \qquad &&&or \qquad &&&&x&&&&&=-1-\sqrt5

\end{alignat}
$$

***

## Solving Equations: 

When solving any equaiton of the form  $LHS(X)=RHS(X)$, applying the same operation $\text{O}()$ to both sides of the equation preserves the original solutions as $LHS=RHS$ is a solution to O($LHS$)=O($RHS$)

However, if the operation O( ) is not injective, it is possible for O($LHS$)=O($RHS$) even when $LHS\ne RHS$, so 'extraneous' solutions that do not satisfy the original equaation may be introduced. 

|                 Injective operations                  |      Non-injective operations      |
| :---------------------------------------------------: | :--------------------------------: |
|      Adding/subtracting a number from both sides      |        Squaring both sides         |
|       Multiplying/dividng by a non-zero number        | Taking the $|\quad|$ of both sides |
|         Taking the square root of both sides          |     Multipling both sides by 0     |
|          Taking the reciprocal of both sides          | Applying $\sin(\ )$ to both sides  |
| Applying $\exp(\ ) \text{ or } \ln(\ )$ to both sides |                                    |

**Extraneous solutions (multiplication):**

Multiplying LHS and RHS by an expression containing unknown(s) can introduce extraneous solutions where that expression equals 0.

**Missing solutions (division):**

Dviding LHS and RHS by an expression containg unknown(s) can remove solutions where that expression equals 0.

**Extraneous solutions (combining logarithms)**
$$
\begin{aligned}
\ln x+\ln(x+2)&=\ln15 \\
\ln(x^2+2x)&=\ln15 \\
x^2+2x&=15 \\
\red{x=-5}\quad  &\text{or} \quad x=3
\end{aligned}
$$
**Missing solutions ($\log x^2 =2\log |x| \neq 2\log x$):**
$$
\begin{aligned}
\log x^2 &=2\log 5 \\
2\log x &=2\log 5 \\
x &= 5 \qquad \red{(x=-5\text{ missed})}
\end{aligned}
$$
<u>**Strategy:**</u>

1. ALWAYS check for extraneous solutions at the end (due to so many different cases)

2. Factor instead of diving by esxpressions containing unknown(s)
   $$
   \begin{aligned}
   f(X)\cdot g(X)&=f(X)\cdot h(X) \\
   f(X)\cdot g(X)-f(X)\cdot h(X) &=0 \\
   f(X) \cdot \left[g(X)-h(X)\right] &=0 \\
   f(X)=0 \quad  \text{or} \quad g(X)&=h(X)
   
   \end{aligned}
   $$
   
   ------


## Denesting Radicals 

**Motivation:**
$$
\begin{aligned}
\sqrt{2+\sqrt 3} &=\sqrt{2+2\sqrt{3/4}} \\
&=\sqrt{3/2+1/2+2\sqrt{3/2\cdot1/2}} \\
&= \sqrt{\left(\sqrt{3/2}+\sqrt{1/2}\right)^2}  \quad =\sqrt{3/2}+\sqrt{1/2} =\frac{\sqrt6+\sqrt2}{2}
\end{aligned}
$$



> **Theorem:**A *real* nested radical of the form $\sqrt{a\pm\sqrt{b}}\ \ ;\ a,b\in \mathbb{Q}\ \&\ \sqrt{b}\notin\mathbb{Q}$ can be expressed as $\sqrt{x}\pm\sqrt{y}\ ;\ x,y\in \mathbb{Q}^+$  if and only if $a^2-b$ is the square of a rational number.
>
> > *Proof*: 
> >
> > Let $z=\sqrt{a\pm\sqrt{b}}.\text{ Suppose }z=\sqrt{x}\pm\sqrt{y}\ ;\ x,y\in \mathbb{Q^+}\ \&\ x>y$
> > $$
> > a\pm \sqrt{b}=x+y\pm 2\sqrt{xy}
> > $$
> > Since $\sqrt{b}\notin\mathbb{Q}$ and $x+y\ \in \mathbb{Q}$
> > $$
> > \begin{align}
> > \sqrt{b}&=\pm2\sqrt{xy} \\
> > a&=x+y \\ 
> > 
> > \end{align}
> > $$
> >
> > $$
> > \begin{align}
> > &x+\frac{b}{4x}=a\\
> > &4x^2-4ax+b=0\\
> > &x=\frac{a\pm\sqrt{a^2-b}}{2}=\frac{a+\sqrt{a^2-b}}{2}\  (x>y)\\
> > &y=\frac{a\pm\sqrt{a^2-b}}{2}=\frac{a-\sqrt{a^2-b}}{2}
> > \end{align}
> > $$
> >
> > 1. $\sqrt{a^2-b}$ and thus $x \ \& \ y$ are rational if and only if $a^2-b=D^2;\ D\in \Q \ \{C_1\}$,  ($x,y\in \Q\iff C_1$)
> >
> > 2. For $x,y>0$, $a\pm\sqrt{a^2-b}>0 \ \Rightarrow a>0$. But $C_1 \Rightarrow a^2-b>0 \Rightarrow (a<-\sqrt b)\or (a>\sqrt b)$ and $z\in \R \Rightarrow a>-\sqrt b$ , so $C_1\Rightarrow a>0 \qquad (x,y>0 \impliedby C_1)$ 
> >    $$
> >    \therefore \quad x,y\in \Q^+\ \iff C_1 \tag{Q.E.D}
> >    $$



## Theorems concerning ratios

> **Theorem:** if $\displaystyle \frac{a_1}{b_1}=\frac{a_2}{b_2}=\cdots=\frac{a_k}{b_k}=\phi$, then $\displaystyle \left( \frac{\lambda_1a_1^n+\lambda_2a_2^n+\cdots\lambda_k a_k^n}{\lambda_1b_1^n+\lambda_2b_2^n+\cdots\lambda_k b_k^n}\right)^{1/n}=\phi \quad \forall\ \lambda_i,n\in \R/\{0\}$ 

> **Theorem:** $$\displaystyle \min \left\{ \frac{a_1}{b_1},\frac{a_2}{b_2},\cdots,\frac{a_n}{b_n} \right\} \le \frac{a_1+a_2+\cdots a_n}{b_1+b_2+\cdots b_n} \le \max \left\{ \frac{a_1}{b_1},\frac{a_2}{b_2},\cdots,\frac{a_n}{b_n} \right\}$$

> **Componendo and dividendo:** If $\displaystyle \frac{a}{b}=\frac{c}{d},\ \text{then } \frac{a+b}{a-b}=\frac{c+d}{c-d}$





## Binomial Coefficients 

Instead of defining $n\choose k $ as $\frac{n!}{k!(n-k)!}$, a better definition is 
$$
{n\choose k} := \frac{(n)_k}{k!} \qquad \text{where }\qquad (n)_k:=\underbrace{(n)(n-1)(n-2)\cdots (n-k+1)}_{k \text{ times}}
$$

1. This definition is equivilant to the first one for $n,k\in \W; n>k$ 
2. Unlike the former definition, it is defined for all $n\in \R, k\in \W$
3. By this definition, $n\choose k=0$ for $k>n$, which makes sense according to the combinatorial interpretation too as there are $0$ ways of choosing more than $n$ objects from $n$ objects
4. The coefficients of $x^k$ in the expansion of $(1+x)^n$ when $n\notin \W$ are given by $\frac{(n)_k}{k!}$ which justifies still calling this sequence *binomial coefficients*

Using this definition, it can be shown that the identity 
$$
{n\choose k}+{n\choose k+1}={n+1\choose k+1}
$$
is valid $\forall n\in \R$



 





























