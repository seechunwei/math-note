

1. Suppose that the population $P(t)$ with $t$ in year of a town satisfies the differential equation $\begin{array} { r } { \frac { d P } { d t } = } \end{array}$ $P \left( 0 . 1 - { \frac { P } { 1 0 ^ { 7 } } } \right)$ . The population in 1975 was 500000. Predict this town’s population for the year 2025. 

$$
\begin{align}
\frac{dP}{dt}&=P\left( 0.1- \frac{P}{10^{7}} \right) \\
\frac{1}{P\left( 0.1- \frac{P}{10^{7}} \right)} \frac{dP}{dt}&=1  
\end{align}
$$
Partial Fraction:

$$
\begin{align}
\frac{1}{P\left( 0.1- \frac{P}{10^{7}} \right)}&= \frac{A}{P}+ \frac{B}{\left( 0.1- \frac{P}{10^{7}} \right)} \\
1&=\left( 0.1- \frac{P}{10^{7}} \right)A+ PB \\
\end{align}
$$

Let $P=0$.
$$
\begin{align}
1&=0.1A+0 \\
A&=10
\end{align}
$$
Let $P=10^{6}$. Hence,

$$
\begin{align}
1&= 0+10^{6}B \\
B&= \frac{1}{10^{6}}
\end{align}
$$
Hence,
$$
\begin{align}
\frac{1}{P\left( 0.1- \frac{P}{10^{7}} \right)}&=  \frac{10}{P}+ \frac{1}{10^{6}\left( 0.1- \frac{P}{10^{7}} \right)} \\
&= \frac{10}{P}+ \frac{1}{10^{5}-0.1P}
\end{align}
$$

Substitute back to the DE:

$$
\begin{align}
\left( \frac{10}{P}+ \frac{1}{10^{5}-0.1P} \right) \frac{dP}{dt}&=1   \\
\int  \left( \frac{10}{P}+ \frac{1}{10^{5}-0.1P} \right) \frac{dP}{dt} \, dt &= \int 1 \, dt  \\
10\ln \lvert P \rvert-10\ln \lvert 10^{5}-0.1P \rvert&=t+c  \\
\ln \left\lvert  \frac{P}{10^{5}-0.1P}  \right\rvert&= \frac{t}{10}+c_{1} \\
\left\lvert  \frac{P}{10^{5}-0.1P}  \right\rvert&=c_{2}e^{t/10} \\
\frac{P}{10^{5}-0.1P}&= c_{3} e^{t/10} \\
P&= 10^{5}c_{3}e^{t/10}-0.1c_{3}Pe^{t/10} \\
P+c_{3}0.1Pe^{t/10}&=10^{5}c_{3}e^{t/10} \\
P(1+c_{3}0.1e^{t/10})&= 10^{5}c_{3}e^{t/10} \\
P&= \frac{10^{5}c_{3}e^{t/10}}{1+c_{3}0.1e^{t/10}} \\
P&= \frac{10^{6}}{\frac{1}{c_{3}0.1e^{t/10}}+1}  \\
P(t)&= \frac{10^{6}}{Ae^{-t/10}+1}
\end{align}
$$

Substitute the condition $(t,P(t))=(0,500000)$:

$$
\begin{align}
P(t)&= \frac{10^{6}}{Ae^{-t/10}+1} \\
500000&= \frac{10^{6}}{A+1} \\
A+1&= \frac{10^{6}}{500000} \\
A+1&=2 \\
A&= 1
\end{align}
$$
Hence, prediction on 2025, $t=2025-1975=50$

$$
\begin{align}
P(t)&= \frac{10^{6}}{ e^{-t/10}+1} \\
P(50)&= \frac{10^{6}}{e^{-5}+1} \\
&= 993307.149 \\
&\approx 993307
\end{align}
$$


2. The population of a district in northern Penang is known to increase at a rate proportional to the number of people presently living in the place. If after two years the population has doubled, and after three year the population is 20000, estimate the number of people initially living in the state. 

Let $P$ denotes the population and $t$ denotes the year.
$$
\begin{align}
\frac{dP}{dt}=rP
\end{align}
$$
The rate of population growth can be formulated by DE above with $r$ as the growth rate. Hence,

$$
\begin{align}
\frac{1}{P} \frac{dP}{dt}&=r \\
\ln \lvert P \rvert&= rt+c \\
\lvert P \rvert&=c_{1}e^{rt} \\
P(t)&=c_{2}e^{rt}
\end{align}
$$
Hence, $P(t)=c_{2}e^{rt}$ is the solution of one parameter family in term of $r$.

Substitute $(0,P_{0})$ into the solution we get
$$
\begin{align}
P_{0}&=c_{2}
\end{align}
$$

After 2 year the population have double, hence substitute $(2,2P_{0})$ 

$$
\begin{align}
2P_{0}&= P_{0}e^{2r} \\
2&= e^{2r} \\
2r&= \ln 2 \\
r&= \frac{\ln 2}{2}

\end{align}
$$
Substitute $(3,2000)$ in the general solution

$$
\begin{align}
20000&= P_{0}e^{ \ln 2 ^{3/2}} \\
&=P_{0} 2^{3/2} \\
P_{0}&=7071.06 \\
&=7071
\end{align}
$$

3. The acceleration of a Maserati is proportional to the difference between 300km/h and the velocity of this sport car. If this machine can accelerate from rest to 120km/h in 10 seconds, how long will it take for the car to accelerate from rest to 250km/h? 

Let $V$ denotes velocity and $t$ denotes times, the problem can be formulated by the DE below: 
$$
\begin{align}
\frac{dV}{dt}= r(V-300)
\end{align}
$$
Solve the DE:
$$
\begin{align}
\frac{1}{V-300} \frac{dV}{dt}&= r\\
\ln \lvert V-300 \rvert&= rt+c \\
V-300&= c_{1}e^{rt} \\
V&= c_{1}e^{rt}+300
\end{align}
$$

Substitute $(0,0)$, we get
$$
\begin{align}
0&=c_{1}+300 \\
c_{1}&=-300
\end{align}
$$
Hence,
$$
V=-300e^{rt}+300
$$
Substitute $(10,120)$:

$$
\begin{align}
120&= -300 e^{10r}+300 \\
-180&=-300 e^{10r} \\
\frac{3}{5}&=e^{10r} \\
10r&=\ln\frac{3}{5} \\
r&=-0.0511
\end{align}
$$

Hence,
$$
V=-300e^{-0.0511t}+300
$$
Find $t$ when $V(t)=250$

$$
\begin{align}
250&=-300e^{-0.0511t}+300 \\
\frac{1}{6}&=e^{-0.0511t} \\
-0.0511t&= \ln \frac{1}{6} \\
t&= 35.06 \text{ second}
\end{align}
$$


4. A businessman places RM20000 in a savings account that pays 5% interest every year compounded continuously. Find 
a. The amount in the account after three years 

The formula compounded continuously at $5$% with $P=20000$ is
$$
A(t)=20000e^{0.05t}
$$
When $t=3$

$$
\begin{align}
A(3)&= 20000e^{0.05(3)} \\
&=\operatorname{RM}23236.68
\end{align}
$$

> [!remark]
> We get the formula by solving the DE 
> $$
> \frac{dA}{dt}=rA
> $$
> the rate of change is proportional to the money value itself

b. The time required for the account to twice the original value, assuming that there is no withdrawals and no additional deposits. 

$$
\begin{align}
40000&=20000e^{0.05t} \\
2&=e^{0.05t} \\
0.05t&=\ln 2 \\
t&=13.86
\end{align}
$$
It need 14 years to double the original value.


5. A cold meat at a temperature of $\mathsf { 1 0 ^ { \circ } C }$ is placed outdoors where the temperature is $3 8 ^ { \circ } \mathsf { C } .$ . If after 5 minutes the temperature of the meat is $1 5 . 5 ^ { \circ } \mathsf C ,$ , find: 
 
 a. how long does it take for the meat to reach a temperature of $2 4 ^ { \circ } \mathsf { C } ?$ 

By Newton's Law of Warming:

$$
\begin{align}
\frac{dT}{dt}&=r(T-38)
\end{align}
$$

Solve the DE:

$$
\begin{align}
\frac{1}{T-38} \frac{dT}{dt}&=r \\
\ln \lvert T-38 \rvert&= rt+c \\
T-38&=c_{1}e^{rt} \\
T&=c_{1}e^{rt}+38
\end{align}
$$

Substitute $(t,T)=(0,10)$:

$$
\begin{align}
10&= c_{1}+38 \\
c_{1}&=-28
\end{align}
$$
Hence, 
$$
T=-28e^{rt}+38
$$
Substitute $(t,T)=(5,15.5)$

$$
\begin{align}
15.5&=-28e^{5r}+38 \\
\frac{45}{56}&=e^{5r} \\
5r&= \ln \frac{45}{56} \\
r&= -0.0437
\end{align}
$$

Hence,
$$
T=-28e^{-0.0437t}+38
$$
Find $t$ when $T=24$:

$$
\begin{align}
24&=-28e^{-0.0437t}+38 \\
\frac{1}{2}&=e^{-0.0437t} \\
-0.0437t&= \ln \frac{1}{2} \\
t&=15.861 \operatorname{minutes}
\end{align}
$$

b. the temperature of the meat after 20 minutes? 

$$
\begin{align}
T&=-28e^{-0.0437(20)}+38 \\
T&=26.31 ^\circ C
\end{align}
$$

6. A metal chair at a temperature of 100°F is placed in a room at a constant temperature of 0°F. If after 20 minutes the temperature of the chair is 50°F, find: 

a. the time it will take the chair to reach a temperature of 25°F? 

By Newton's Law of Cooling, we will get the same DE in 5(a). Hence, we will get

$$
T(t)=c_{1}e^{rt}+0
$$
Substitute $(t,T)=(0,100)$:

$$
\begin{align}
100&=c_{1}
\end{align}
$$
Hence,
$$
T(t)=100e^{rt}
$$
Substitute $(t,T)=(20,50)$

$$
\begin{align}
50&= 100e^{20r} \\
\frac{1}{2}&= e^{20r} \\
20r&= \ln \frac{1}{2} \\
r&= -0.0347
\end{align}
$$
Hence, we have
$$
T(t)=100e^{-0.0347t}
$$
Find t when $T=25$:

$$
\begin{align}
25&=100e^{-0.0347t} \\
\frac{1}{4}&=e^{-0.0347t} \\
-0.0347t&= \ln \frac{1}{4} \\
t&= 39.95 \text{ minutes}
\end{align}
$$

b. the temperature of the chair after 10 minutes? 

$$
\begin{align}
T(10)&= 100e^{-0.0347(10)} \\
&=70.68 ^\circ F
\end{align}
$$

7. An electrical circuit with a nonlinear component is modeled by $\textstyle { \frac { d i } { d t } } + 2 i = 3 i ^ { 3 }$ . If the initial current is $i ( 0 ) =$ 0.5 A, solve for the current $i(t)$ over time.  ^90bcb6

$$
\begin{align}
\frac{di}{dt}+2i&=3i^{3}  \\
\frac{di}{dt}&= 3i^{3}-2i \\
\frac{1}{i(3i^{2}-2)} \frac{di}{dt}&= 1 \\
\end{align}
$$

By partial fraction:
$$
\begin{align}
\frac{1}{i(3i^{2}-2)}&= \frac{A}{i}+ \frac{Bi+C}{3i^{2}-2} \\
1&= A(3i^{2}-2)+ i(Bi+C) \\
\end{align}
$$

Let $i=0$, we get
$$
\begin{align}
1&=A(-2) \\
A&= -\frac{1}{2}
\end{align}
$$
Note that
$$
3i^{2}-2=0\implies 3i^{2}=2\implies i^{2}=  \frac{2}{3}\implies i=  \pm \sqrt{ \frac{2}{3} }
$$
Let $i= \sqrt{ \frac{2}{3} }$. Then

$$
\begin{align}
1&= \sqrt{ \frac{2}{3} }\left( \sqrt{ \frac{2}{3} }B+C \right) \\
1&= \frac{2B}{3}+ \sqrt{ \frac{2C^{2}}{3} } \tag*{(1)}
\end{align}
$$
Let $i=- \sqrt{ \frac{2}{3} }$, we have
$$
\begin{align}
1&= \frac{2B}{3}- \sqrt{ \frac{2C^{2}}{3} } \tag*{(2)}
\end{align}
$$

(1)+(2):
$$
\begin{align}
2&= \frac{4B}{3} \\
4B&=6 \\
B&= \frac{3}{2}
\end{align}
$$

Substitute $B= \frac{3}{2}$ into (1), we get

$$
\begin{align}
1&= \frac{2\left( \frac{3}{2} \right)}{3}+ \sqrt{ \frac{2C^{2}}{3} } \\
&=1+ \sqrt{ \frac{2C^{2}}{3} } \\
0&= \sqrt{ \frac{2}{3} }C \\
C&=0
\end{align}
$$

Hence. we have

$$
\begin{align}
\frac{1}{i(3i^{2}-2)}&=- \frac{1}{2i}+ \frac{3i}{2(3i^{2}-2)} \\
&= -\frac{1}{2i}+\frac{3i}{6i^{2}-4} \tag*{(3)}
\end{align}
$$
Substitute (3) into DE

$$
\begin{align}
\frac{1}{i(3i^{2}-2)} \frac{di}{dt}&= 1  \\
\left( -\frac{1}{2i}+ \frac{3i}{6i^{2}-4} \right) \frac{di}{dt} &=1 \\
-\frac{1}{2}\ln \lvert i \rvert+  \frac{1}{4} \ln \lvert 6i^{2}-4 \rvert&= t+c \\
-\ln \lvert i^{2} \rvert+\ln \lvert 6i^{2}-4 \rvert&= 4t+c_{1} \\
\ln \left\lvert  6- \frac{4}{i^{2}}  \right\rvert&=4t+c_{1} \\
6- \frac{4}{i^{2}}&= c_{2}e^{4t} \\
6i^{2}-4&= c_{2} e^{4t}i^{2} \\
(6-c_{2}e^{4t})i^{2}&=4 \\
i^{2}&= \frac{4}{6-c_{2}e^{4t}} \\
i&= \pm \frac{2}{\sqrt{ 6-c_{2}e^{4t} }}
\end{align}
$$
Since the initial condition given is $(i(t),t)=(0.5,0)$. Hence, the general solution of one parameter family is

$$
i=\frac{2}{\sqrt{ 6-c_{2}e^{4t} }}
$$

Substitute the initial condition:

$$
\begin{align}
0.5&= \frac{2}{\sqrt{ 6-c_{2} }} \\
\sqrt{ 6-c_{2} }&= 4 \\
6-c_{2}&= 16 \\
c_{2}&= -10
\end{align}
$$
Hence, the particular solution for this IVP is
$$
i= \frac{2}{\sqrt{ 6+10e^{4t} }}
$$

Since $6+10e^{4t}\geq 6> 0$ for all $t\in \mathbb{R}$. Hence the interval of definition is $(-\infty ,\infty)$.

> [!remark]
> We excluded $i=0,i= \pm \sqrt{ \frac{2}{3} }$ in the interval when obtaining the solution and they are all equilibrium solution for the DE. 
> Do we need to check if it cross the equilibrium solution?
> No, it never cross.

8. A tank has fresh water flowing into it at 10 gal/min. The contents of the tank are kept thoroughly mixed, and the contents flow out at 10 gal/min. Salt is added to the tank at the rate of 0.1 lbs./min. Initially, the tank contains 10 pound of salt in 100 gal of water. How much salt is in the tank after 30 minutes? 

$$
\begin{align}
\frac{dA}{dt}&= R_{in}-R_{out}
\end{align}
$$

where $A$ is the amount of salt in the tank and
$$
R_{in}=c_{in}\cdot r_{in}
$$
where $c_{in}$ is the concentration of salt per gal and ,$r_{in}$ is the flow rate of water.

From question, we know that
$$
R_{in}= 0.1 \operatorname{{lbs} / {min}}
$$
and
$$
\begin{align}
R_{out}&= \frac{A(t)}{V(t)}\cdot 10 \text{ gal/min} \\
&= \frac{A(t)}{100} \cdot 10 \\
&=\frac{A(t)}{10}
\end{align}
$$
Hence,
$$
\begin{align}
\frac{dA}{dt}&= 0.1- \frac{A}{10} \\
10 \frac{dA}{dt}&= 1-A \\
\frac{10}{1-A} \frac{dA}{dt}&=1 \\
-10\ln \lvert 1-A \rvert&= t+c \\
\ln \lvert 1-A \rvert&= \frac{t}{-10}+c_{1} \\
1-A&= c_{2}e^{-t/10} \\
A&= 1-c_{2}e^{-t/10}
\end{align}
$$

Hence, this is the general solution of one parameter family.

Substitute the initial condition $(t,A(t))= (0, 10)$.  Hence

$$
\begin{align}
10&= 1-c_{2} \\
c_{2}&=-9
\end{align}
$$
Therefore,
$$
A(t)= 1+9 e^{-t/10}
$$
is the particular solution for this IVP.

Find $A(t)$ when $t=30$:

$$
\begin{align}
A(30)&= 1+9e^{-3} \\
&=1.448 \operatorname{ lbs}
\end{align}
$$

> [!remark]
> $A=-1$ is the equilibrium solution.

