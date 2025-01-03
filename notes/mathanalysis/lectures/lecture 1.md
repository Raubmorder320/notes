### Норма линейного оператора

$A:R^{m}\rightarrow R^n$
$m,n\geq1$ 
$||A||=sup_{x \in R^m}||Ax||_{R^n}$
#### Свойства нормы линейного оператора
1. $||A||\geq 0; \quad||A||=0 \rightarrow A=O$,   т.е. $Ox=O_n\forall$ $x \in R_m$
   
$A_{n*m}=\begin{bmatrix}a_{11}.....a_{1m} \\.\\.\\.\\a_{n1}.....a_{nm}\end{bmatrix}\begin{bmatrix}0 \\.\\1\\.\\0\end{bmatrix}=\begin{bmatrix}a_{11} \\.\\1\\.\\a_{ni}\end{bmatrix}$

$1\leq j \leq m \qquad 1\leq i \leq n$
$e_i=[0....1...0]$

$f_j=\begin{bmatrix}0 \\.\\1\\.\\0\end{bmatrix}$

$e_i(A_{n*m}f_j)=e_i\begin{bmatrix}0 \\.\\.\\.\\0\end{bmatrix}=0$ ==(2)== т.к. $||A|| = 0 \implies ||Ax||_{n} = 0\implies Ax = O_{n}$

$e_i(A_{n*m}f_j)=e_i\begin{bmatrix}a_{1j} \\.\\ .\\.\\a_{ij}\end{bmatrix}=a_{ij}$ ==(3)==

(2),(3)$\implies a_{ij}=0$

2. $cR$  $||cA||=|c|*||A||$
$||cA||= sup_{x\in R^m}||(cA)x||_{R^n}=sup||c(Ax)||_{R^n}=sup(|c|*||Ax||)_{R^n}=|c|*sup||Ax||_{R^{n}}=|c|*||A||$

3. $A,B:R^m\to R^n$
$||A+B||\leq||A||+||B||$ $||A+B||=sup_{x \in R^m}||(A+B)x||_{R^n}=sup||Ax+Bx||_{R^n}\leq sup(||Ax||_{R^n}+||Bx||_{R^n})\leq sup||Ax||_{R^n}+sup||Bx||_{R^n}=||A||+||B||$

4. $||Ax||_{R^{n}} \leq||A||*||x||_{R^{m}}$   $\forall x \in R^m$
$x\ne0$  $t=||x||_{R^m}>0$
$y=\frac{1}{t}x$   $||y||_{R^m}=\frac{1}{t}||x||=1$
$||Ay||_{R^n}\leq sup||AU||_{R^n}=||A||$, где $U \in R^{m}; \ \ ||U||_{\mathbb{R}^{m}} \leq 1$
$x=ty \implies ||Ax||_{R^n}=||A(ty)||_{R^n}=t||Ay||_{R^n} \leq t||A||$

5. $c_0>0$
$\forall x \in R^m \quad ||Ax||_{R^n} \leq c_0||x||_{R^m} \implies ||A|| \leq c_0$
$\forall x \in R^m, ||x||_{R^n} \leq 1$ 
(4)$\implies||Ax||_{R^n}=c_0||x||{R^m}\leq c_0$
(5)$\implies sup||Ax||_{R^n}\leq c_0$

6. $A = \begin{bmatrix}a_{11}.....a_{1m} \\.\\.\\.\\a_{1n}.....a_{nm}\end{bmatrix}$

$||A||\leq (\sum\sum a_{ij}^2)^{1/2}$==(6)==

$x=e_i\begin{bmatrix}x_{1} \\.\\ .\\.\\x_{m}\end{bmatrix}$        $||x||_{R^m}<=1$

$Ax=A = \begin{bmatrix}a_nx_1+.....+x+ma_{1m} \\.\\.\\.\\a_mx_1+.....+a_{nm}x_m\end{bmatrix}$==(7)==

7=>$||Ax||_n^2=\sum\limits_{i=1}^{n}(\sum\limits_{j=1}^{m}a_{ij}x_j)^{2}<=\sum\limits_{i=1}^{n}(\sum\limits_{j=1}^{m} a_{ij}^2)(\sum\limits_{i=1}^{n}x_{j}^{2})\leq \sum\limits_{i=1}^{n}\sum\limits_{j=1}^{m} a_{ij}^2$==(8)==
(8),(5)$\implies$(6) <font color="#ffff00">ЧТД</font> 

7. $R^{m}, R^{n},R^{k}$
$1<=m,n,k$
$A:R^m->R^{n},B:R^n->R^k$
$BA:R^m->R^k$
$||BA||<=||B||*||A||$ при $x \in R^{m} ||x||_{R^m}<=1$
$y=Ax$
$BA(x)=B(Ax)=By$
$||BA(x)||_{R^k}=||By||_{R^k}<=||B||*||y||_{R^n}$==(9)==
$||y||_{R^n}=||Ax||_{R^n}<=||A||*||x||_{R^m}<=||A||$
(9)(10)$\implies||BA(x)||_{R^k}<=||B||*||A||$(11)
5.;(11) $\implies$ 7
### Частные производные второго и последующих порядков
$\Upomega \in R^{n}$   ${n>=2}$
$\Upomega$-открытое, $\Upomega\ne0$  $\exists f'_{x_{i}}(x)$ $\forall x \in \Upomega$
$f:\Upomega->R$             $x_{0} \in \Upomega$
$1<=i<=n$
$1<=j<=m$
пусть $\exists(f'_{x_{i}})_{x_{i}}'(x_0)$
$f''_{x_ix_j}(x_0)=(f'_{x_{i}})_{x_{i}}'(x_0)$
пусть $\forall x \in \Upomega$ $\exists f''_{x_ix_j}(x)$
$\exists(f''_{x_ix_j})'_{x_k}$
$f'''_{x_ix_jx_k}(x_0)=(f''_{x_ix_j})'_{x_k}$

$l>=3$
$x_{0} \in \Upomega$    $f^{(l)}_{x_ix_j...x_g}(x_0)$
пусть $\forall x \in \Upomega$ $\exists f^{(l)}_{x_ix_j...x_g}(x)$
$\exists (f^{(l)}_{x_ix_j...x_s})_{x_{t}}'(x_0)$

$f^{(l+1)}_{x_ix_j...x_sx_t}(x_0)=(f^{(l)}_{x_ix_j...x_s})_{x_{t}}'(x_0)$

$\frac{\partial^lf(x)}{\partial x_s...dx_jd_xi}$

*<font color="#8064a2">конец первой лекции</font>*