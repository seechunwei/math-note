Division into case and the quotient-remainder theorem

==Theorem==  The Quotient-Remainder Theorem
For all integer n and positive integer d, there exists an unique integer q and r such that
$$
n =dq+r \text{ and }0\leq r<d
$$
Why we need to fix $d$ as positive integer. For simplify the proof of uniqueness of q and simplify the constraint for r. If not, $0\leq r<|d|$

%%The proof that there exist integers q and r with the given properties is in Section 5.4; the proof that q and r are unique is outlined in exercise 21 in Section 4.8.%%

Because of r is positive, when n is negative , d must be multiplied by a negative integer q to bring $dq$ either exactly to n (in which case r=0) or to a point below n (in which case the positive integer r is added to bring dq+r back up to n

Proof:
The proof of existence of such q and r requires strong mathematical induction from Section 5.4. In the following, we prove the uniqueness of such q and r.

Suppose not. That is there exists **two** different pairs of integers that satisfy the theorem. Suppose $a$ and $b$ is an arbitrary integer and $b>0$. Suppose that there exists $(q,r)$ and $(q',r')$ are two distinct pairs of integers such that
$$
\begin{array}
\ a=bq+r ,0\leq r<b \\
a=bq'+r',0\leq r'<b
\end{array}
$$
Thus,
$$
\begin{align}
bq+r&=bq'+r' \\
b(q-q')&=r'-r
\end{align}
$$
(To compare them effectively, we need to group similar terms as above. The equation reveals a crucial relationship: the difference between two remainder $r'-r$ must be multiple of b)

Now, since $0\leq r<b$ and $0\leq r'<b$. 
%%What is the possibility of $r'-r$
- **Largest possible:** If $r'$ is nearly $b$ and $r$ is $0$, the result is just under $b$.
    
- **Smallest possible:** If $r'$ is $0$ and $r$ is nearly $b$, the result is just above $-b$.
Thus, the range of possibility of $r'-r$ is $(-b,b)$. Or algebraically,%%
$$
\begin{array}
\ 0\leq r<b \\
0\geq-r>-b \\
-b<-r\leq 0
\end{array}
$$
Thus,
$$
-b<r'-r<b
$$

%%(Think about it this way: for the sum to be **equal** to the limit, _both_ parts would have to be equal to their limits.

- If $A < 10$ (A is strictly smaller than 10)
    
- And $B \le 5$ (B could be 5)
    
- Then $A + B$ can never reach 15, because $A$ will always be a tiny bit missing. So, $A + B < 15$.)%%


Let $t=q-q'$ and t is an integer because the difference of integers is an integer. Thus, we need to find t where
$$
-b< bt<b
$$
Thus, $t=0$ , by substitution 
$$
\begin{align}
q-q'=0 \\
q=q'
\end{align}
$$
Now, we already prove the quotient part now we need to prove the remainder part. Since $q-q'=0$, by zero product property 
$$
\begin{align}
r'-r=0 \\
r'=r
\end{align}
$$
Thus, it contradict the supposition that $q\neq q'$ and $r\neq r'$. Q.E.D





$b(q-q')=r'-r$
$(q-q')=0$ and $q=q'$
$r'-r=0$ and $r'=r$

==Definition== div and mod
Given an integer n and a positive integer d,
n div d= the integer quotient obtained when n is divided by d, 

n mod d= the nonnegative integer remainder obtained when n is divided by d.


Symbolically, if n and d are integer and $d>0$, then
n div d=q  and  n mod d=r $\Leftrightarrow$ $n =dq+r$,
where q and r are integers and $0\leq r<d$.


==Question== Why an integer is either odd or even but not both?
we defined an even integer to have the form twice some integer and an odd integer has the form twice some integer plus 1. We need to proof that there is only 2 possible remainder when an integer is divided by 2.

Suppose an arbitrary integer n. By the quotient-remainder theorem (with $d=2$), there exists unique integer q and r such that $n =2q+r$  and $0\leq r<2$

Noticed that the only integers that satisfy $0\leq r<2$ are $r=0$ and $r=1$. It follows that given any integer n, there exists an integer q with
$n =2q+0$ or $n =2q+1$
In the case that $n =2q+0$, n is even. In the case that $n =2q+1$, n is odd. Hence n is either even or odd, and, because of the uniqueness of q and r, n cannot be both even and odd.


==Theorem 4.5.2 The Parity Property==
Any two consecutive integers have opposite parity.
Proof:
Suppose x and y are arbitrary consecutive integers. WLOG, we assume that $x<y$. Let $x=m$ and $y=m+1$. We must show that one of m and $m+1$ is even and that the other is odd.

Case 1(m is even): By definition $m=2k$ for some integer k, and so $m+1=2k+1$ which is odd. In this case, one of $m$ and $m+1$ is even and other one is odd.

Case 2(m is odd): By definition $m=2k+1$ for some integer k, and $m+1=2k+1+1=2(k+1)$ 
Let $t=k+1$ where t is an integer because it is a sum of integers
By substitution, $m+1=2t$ for some integer t which is even.
Therefore, one of m and $m+1$ is even and the other is odd.

It follow that one of m and m+1 is even and the other is odd for all cases. Q.E.D


==Theorem The Square of an Odd Integer==
The square of any odd integer has the form $8m+1$ for some integer m.

The main idea is using the idea of remainder theorem to express any integer in one of the 4 forms $4q+0,4q+1,4q+2,4q+3$. 

==Absolute value and the Triangle Inequality==
Absolute value is the distance between one real number $\alpha$ and origin on number line. Note that distance is a magnitude which does not have direction. Thus, in this case the absolute value of a $\alpha$ and $-\alpha$ are same which denoted by:
$$|x| = \begin{cases} x, & \text{if } x \geq 0 \\ -x, & \text{if } x < 0 \end{cases}$$
The ==triangle inequality== says that the absolute value of the sum of two numbers is less than or equal to the sum of their absolute values. To prove this by using 2 lemma .
==Lemma 1==
$\forall r \in \mathbb{R},-|r|\leq r\leq|r|$

No matter what is r, $|r|$ is always $\geq 0$ thus, $-|r|\leq 0$ . Thus, if $r\geq 0$, then $r=|r|$ and $r\geq-|r|$ . if $r<0$, then $r<|r|$ and $r=-|r|$ . This lemma express the relationship (inequality) between absolute value and its real number.


To prove the triangle inequality we need to know the relation between plus minus sign which is $|-r|$ and $|r|$
==Lemma 2==
For every real number $r$, $|-r|=|r|$

==Theorem 4.5.6 The Triangle Inequality==
$$
\forall x,y,\text{ if }x,y\in \mathbb{R},\text{ then }|x+y|\leq|x|+|y|
$$
Case 1 $x+y\geq{0}$ .
In this case , $|x+y|=x+y$
What is the relation between $x+y$ and $|x|+|y|$.
By lemma 1, $x\leq|x|$ and $y\leq|y|$. Thus, $x+y\leq|x|+|y|$ 
Thus, $|x+y|=x+y\leq|x|+|y|$

Case 2 $x+y<0$
In this case, $|x+y|=-(x+y)=-x+(-y)$
By lemma 1, $-x\leq|-x|$ and $-y\leq|-y|$

By lemma 2,
$|-x|=|x|$ and $|-y|=|y|$
Thus, combine together $-x\leq|x|$ and $-y\leq|y|$

It follow that
$|x+y|\leq|x|+|y|$.

