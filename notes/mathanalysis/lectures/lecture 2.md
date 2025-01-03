<font color="#00b050">продолжение</font>

#### Теорема о смешанной производной
$B_r(x_1,x_2)$
$x_{0} = \begin{bmatrix}x_{1}\\ x_{2}\end{bmatrix}$ 
$f:G \rightarrow R$ $f \in C(G)$
$\forall x \in G$ $\exists f'_{x_1}(x),f'_{x_{2}}\in C(G)$
$\forall x \in G$ $\exists f''_{x_1x_{2}}(x),f''_{x_2x_{1}}(x)$
$f''_{x_1x_{2}}(x),f''_{x_1x_{2}}(x)$ непрерывны в $x_0$, тогда $f''_{x_1x_{2}}(x_0)=f''_{x_2x_{1}}(x_0)$==(1)==
#### Док-во:
$0<h<\frac{r}{\sqrt{2}}$     $(x_1+h,x_2+h)\in G$

$g(h)=\frac{f(x_1+h,x_2+h)-f(x_1+h,x_2)-f(x_1,x_2+h)+f(x_1,x_2)}{h^2}$==(2)==

$\phi(x_2)=\frac{f(x_1+h,x_2)-f(x_1,x_2)}{h}$==(3)==

$x_{2} \in [x_2,x_2+h]$

$\frac{\phi(x_2+h)-\phi(x_2)}{h}$

$\frac{\phi(x_2+h)-\phi(x_2)}{h}=\frac{f(x_1+h,x_2+h)-f(x_1,x_2+h)-f(x_1+h,x_2)+f(x_1,x_2)}{h^2}=g(h)$==(4)==

(3)=>$\forall x_{2} \in [x_2,x_2+h]$ $\exists \phi'(x_2)=\frac{f'_{x_2}(x_1+h,x_2)-f'_{x_2}(x_1+h,x_2)}{h}$==(5)==

Применим теорему Лагранжа:
$\exists h_2,0<h_2<h$
$\phi(x_2+h)-\phi(x_2)=\phi'(x_2+h_2)*h$ => $\frac{\phi(x_2+h)-\phi(x_2)}{h}=\phi'(x_2+h_2)$==(6)==

(5)(6)=>$\frac{\phi(x_2+h)-\phi(x_2)}{h}=\frac{f'_{x_2}(x_1+h,x_2+h_2)-f'_{x_2}(x_1,x_2+h_2)}{h}$==(7')==

$f'_{x_2}(x_1+h,x_2+h_2)-f'_{x_2}(x_1,x_2+h_2)$
$\phi(x_1)=f'_{x_2}(x_1,x_2+h_2)$
$\forall x_{1} \in [x_1,x_1+h]$ $\exists \phi(x_1)=f''{x_2x_1}(x_1,x_2+h_2)$==(7)==

Снова Лагранж:
$\exists h_1,0<h_1<h$ т.ч. $\phi(x_1+h)-\phi(x_1)=\phi'(x_1+h_1)*h$==(8)==
(7)(8)=>$\frac{\phi(x_1+h)-\phi(x_1)}{h}=\frac{f'_{x_2}(x_1+h,x_2+h_2)-f'_{x_2}(x_1,x_2+h_2)}{h}=$
$=\phi'(x_1+h_1)=f''_{x_2x_1}(x_1+h_1,x_2+h_2)$==(9)==
(7')(9)(4)=>$g(h)=f''_{x_2x_1}(x_1+h_1,x_2+h_2)$  $0<h_1<h$   $0<h_2<h$ ==(10)  ==

Рассмотрим функцию $\psi$:

$\psi(x_1)=\frac{f(x_1,x_2+h)-f(x_1,x_2)}{h}$==(11)==

$\frac{\psi(x_1^0+h)-\psi(x_1^0)}{h}=\frac{f(x_1^0+h,x_2^0+h)-f(x_1^0+h,x_2^0)-f(x_1^0,x_2^0+h)+f(x_1^0,x_2^0)}{h^2}=g(h)$==(12)==

$\forall x \in [x_1^0,x_1^0+h]$  $\exists \psi'(x)$

$\psi(x_1)=\frac{f'_{x_1}(x_1,x_2^0+h)-f'_{x_1}(x_1,x_2^0)}{h^2}$==(13)==

(13)=> $\frac{\psi(x_1^0+h-\psi(x_1^0)}{h}$    (опять Лагранж $\exists 0<h^-_1<h$   $\exists 0<h_2^-<h$)$=\psi'(x_1^0+h_1^-)=$

$=\frac{f'_{x_1}(x_1^0+h_1^0,x_2^0+h)-f'_{x_1}(x_1^0+h,x_2^0)}{h}=f'_{x_1}(x_1^0+h_1^0,x_1)=f''_{x_1x_2}(x_1^0+h_1^0,x_2^0+h_2^-)$ ==(14)==

(12)(13)(14)=>$g(h)=f''_{x_1x_2}((x_1^0+h_1^0,x_2^0+h_2^-))$(==15)==
(10)(15)=> $f''_{x_1x_2}(x_1^0+h_1^0,x_2^0+h_2^-)=''_{x_2x_1}(x_1^0+h_1^0,x_2^0+h_2^-)$==(16)==
$f''_{x_2x_1}(x_1^0+h_1^0,x_2^0+h_2^-)\rightarrow f''_{x_1x_2}(x_1^0+h_1^0,x_2^0+h_2^-)$ ==(17)==
$f''_{x_1x_2}(x_1^0+h_1^0,x_2^0+h_2^-)\rightarrow f''_{x_2x_1}(x_1^0+h_1^0,x_2^0+h_2^-)$==(18)== 
В силу единственности предела (16)-(18)=>(1)

<font color="#ffff00">ЧТД</font>

#### Следствие для n>2
$x_{0} \in R^{n}, n>=3$
$x_0=(x_1^0,x_2^0,...,x_n^0)$
$f: B_r(x^0) \rightarrow R$  $f \in C(B_r(x^0))$
$\forall x \in B_r(x^0)$  $\exists f'_{x_2}(x),\exists f'_{x_{3}}(x) \in C(B_r(x^0))$
$\forall x \in B_r(x^0)$  $\exists f''_{x_ix_j}(x),\exists f''_{x_jx_i}(x)$
$f''_{x_ix_j}(x)=f''_{x_jx_i}(x)$
$F(x_i,x_j)=f(x_1^0,...,x_n^0)$
$F''(x_i,x_j)=f''_{x_ix_j}(x_1^0,...,x_n^0)$

$\Upomega \in R^n;n>=2$
$f \in C(\Upomega),\forall x \in \Upomega f'_{x_i}(x),f'_{x_{j}}(x)\in C(\Upomega)$
$f \in C(\Upomega),\forall x \in \Upomega f''_{x_jx_i}(x),f''_{x_{i}x_j}(x)\in C(\Upomega)$
$\forall x \in \Upomega f''_{x_jx_i}(x)=f''_{x_{i}x_j}(x)$

Рассмотрим случай частной производной третьего порядка
$\Upomega \in R^{n} n>=2$
$i\ne j,k$
$f'''_{x_ix_jx_k}(x)$     $f'''_{x_jx_ix_k}(x)$ $\in C(\Upomega)$
$f'''_{x_ix_kx_j}(x)$                       
также существуют производные первого и второго порядка и они непрерывны
$f''_{x_ix_j}(x)=f''_{x_jx_i}(x)$=>$(f''_{x_ix_j})'_{x_k}(x)=f''_{x_jx_i})'_{x_k}(x)$
$(f'_{x_i})''_{x_kx_j}(x)=(f'_{x_i})''_{x_kx_j}(x)$
