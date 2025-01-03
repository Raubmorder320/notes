26.09

### Теорема Лагранжа для вектор функций
**Опр**: отображение $F: (a,b) \longrightarrow R^{n}, \ \ n \ge 2$  часто называют **вектор-функцией, заданной на  $(a,b)$**
$F(t) = \begin{bmatrix} f_{1}(t) \\ . \\ . \\ f_{n}(t) \end{bmatrix}$      
**Напоминание**: $t_{0} \in (a,b), \ \ \ F$ дифференцируема в $t_{0}$ <=> $f_{j}(t)$ дифференцируема в $t_{0} \ \forall \ j = 1,2,...,n$ <=> $\exists \ f'_{j}(t_{0}) \ \forall j = 1,..,n$

Тогда $\mathbf{D}F(t_{0}) = \begin{bmatrix}  f'_{1}(t_{0}) \\ . \\ . \\ f'_{n}(t_{0}) \end{bmatrix}$
$|| \mathbf{D}F(t_{0}|| = sup || \mathbf{D}F(t_{0}h ||_{R^{n}} = sup|| h\mathbf{D}F(t_{0} ||_{R^{n}} = sup|h|*|| = \mathbf{D}F(t_{0} ||_{R^{n}} = || \begin{bmatrix} f'_{1}(t_{0}) \\ . \\ f'_{n}(t_{0}) \end{bmatrix} ||_{R^{n}}$


### Теорема Лагранжа для вектор функций
пусть $F : [a,b] \longrightarrow R^{n}, \ \ n \ge 2 \ \ \ \ F \in C([a,b]) \ \forall t \in (a,b)$
предположим, что $F$ - дифференцируема в $t$, тогда 
$\exists c \in (a,b): || F(b) - F(b) ||_{R^{n}} \ \le \ ||\mathbf{D}F(c)||_{R^{n}}(b-a)$  ==(1)==

Доказательство:
$\phi (t) = F(t)^{T} * (F(b) - F(a)) = f_{1}(t) * (f_{1}(b) - f_{1}(a)) + ... + f_{n}(t)(f_{n}(b) - f_{n}(a))$ ==(2)==
Будем считать, что $F(b) \ne F(a)$
$\phi \in C([a,b]), \ \ \forall t \in (a,b) \ \ \exists \phi'(t)$  ==(3)==
(2) => $\phi'(t) = f'_{1}(t)(f_{1}(b) - f_{1}(a)) + ... + f'_{n}(t)(f_{n}(b) - f_{n}(a))$  ==(4)==
Применим Лагранжа:
(4) => $\exists c \in (a,b)$ т.ч. $\phi (a) - \phi (b) = \phi'(c)(b-a)$ ==(5)==
(2) = $\phi (b) - \phi (a) = (f_{1}(b) - f_{1}(a))^{2} +...+ (f_{n}(b) - f_{n}(a))^{2}$ ==(6)==
(6) => $\phi (b) - \phi (a) = || F(b) - F(a) ||^{2}_{R^{n}}$  ==(7)==
(4) => $|\phi'(c)| \le ((f'_{1}(c))^{2} + ... + (f'_{n}(c)^{2}))^{\frac{1}{2}} * ((f'_{1}(b) - f'_{1}(a))^{2})^{\frac{1}{2}} + ... + ((f'_{n}(b) - f'_{1}(n))^{2})^{\frac{1}{2}} =$
$=||\mathbf{D}F(c)||_{R^{n}} * ||F(b) - F(a)||_{R^{n}}$  ==(8)==
(7)(8) => $|| F(b) - F(a) ||^{2}_{R^{n}} \le ||\mathbf{D}F(c)||_{R^{n}} \ ||F(b) - F(a)||_{R^{n}} (b-a)$ 
=> $|| F(b) - F(a) ||_{R^{n}} \le ||\mathbf{D}F(c)||_{R^{n}} (b-a)$
### Теорема об обратимости линейного отображения близкого к обратимым
$A: R^{n} \longrightarrow R^{n}, \ \ n \ge 2 \ \ \ \ A(x) = Ax, \ x \in R^{n}$
$\exists B \ \ AB = \mathbf{I} \ \ B = A^{-1}$
$A$ - обратима <=> det$A \ne 0$
$A$ - обратима <=>$Ax = \mathbb{O}_{n} \ \forall x \ne \mathbb{O}_{n}$ 
Теорема:
Пусть $A_{n \times n}$ - обратимая матрица,  $||A^{-1}|| = \frac{1}{\alpha}, \ \alpha > 0$
Пусть $B$ т.ч. $||B - A|| = \beta, \ \ 0<\beta<\alpha$ , тогда $B$ - обратима и $||A^{-1} - B^{-1}||_{R^{n}} \le \frac{\beta}{\alpha(\alpha - \beta)}$
Доказательство:
$x = Ix = AA^{-1}(x), \ x \in R^{n}$ => $||x||_{R^{n}} = ||A^{-1}(Ax)||_{R^{n}} \le ||A^{-1}||_{R^{n}}||Ax||_{R^{n}} = \frac{1}{\alpha}||Ax||_{R^{n}}$ 
=> $||Ax||_{R^{n}} \ge \alpha ||x||_{R^{n}}$   ==(9)==
$Bx = Ax+(Bx - Ax)$ => $||Bx||_{R^{n}} \ge ||Ax||_{R^{n}} - ||Bx - Ax||_{R^{n}}$  ==(10)==
$||Bx - Ax||_{R^{n}} = ||(B - A)x||_{R^{n}} \le ||(B - A)||_{R^{n}}||x||_{R^{n}}$  ==(11)==
(9)-(11) =>$|| Bx ||_{R^{n}} \ge \alpha||x||_{R^{n}} - ||(B-A)||_{R^{n}}||x||_{R^{n}} = \alpha ||x||_{R^{n}} - \beta ||x||_{R^{n}}$  ==(12)==
(12) => $B$ - обратимая (если $x \ne \mathbb{O}_{n}$, то $||Bx||_{R^{n}} \ne 0$)
$\forall y \ne \mathbb{O}_{n}, \ \ x = B^{-1}y$
(12) => $||B(B^{-1}y)||_{R^{n}} \ge (\alpha - \beta) ||B^{-1}y||_{R^{n}}$   ==(13)==
$||BB^{-1}y||_{R^{n}} = ||Iy||_{R^{n}} = ||y||_{R^{n}} \ge (\alpha-\beta)||B^{-1}y||_{R^{n}}$ <=> $||B^{-1}y||_{R^{n}} = \frac{1}{\alpha-\beta}||y||_{R^{n}}$  ==(14)==
(14) => $||B^{-1}||_{R^{n}} \le 1/\alpha-\beta$  ==(15)==
Вычислим $A(A^{-1} - B^{-1})B = (A(A^{-1} - B^{-1}))B = (AA^{-1} - AB^{-1})B=$ 
$= (I - AB^{-1})B = (IB - AB^{-1}B) = IB - AI = B-A$  ==(16)== 
(16) => $A^{-1}A(A^{-1}-B^{-1})BB^{-1} = A^{-1}(B-A)B^{-1}$ <=> $A^{-1}-B^{-1} = A^{-1}(B-A)B^{-1}$  ==(17)==
(15),(16) => $||A^{-1}-B^{-1}||_{R^{n}} \le ||A^{-1}||_{R^{n}}||A-B||_{R^{n}}||B^{-1}||_{R^{n}} \le \frac{1}{\alpha}\beta \frac{1}{\alpha-\beta} = \frac{\beta}{\alpha(\alpha-\beta)}$
ч.т.д.
### Теорема об обратном отображении
Пусть $E \subset R^{n}, \ \ n \ge 2 \ \ \ x_{0} \in E$ - внутренняя точка
$F: E \longrightarrow R^{n}$ - биекция  $G = F(E)$
$\exists \Upphi: G \longrightarrow E : \ \ \Upphi(F(x)) = x \ \ \forall x \in E, \ \ F(\Upphi(y)) = y \ \ \ \forall \ y \in G, \ \ y = F(x)$ <=> $x = \Upphi(y)$
Пусть $F$ - дифференцируема в $x_{0}, \ y_{0}=F(x_{0})$,  $\Upphi$ - дифференцируема в $y_{0}$
Обозначим через $I(x)=x \ \forall \ x \in E$ - тождественное отображение
Тогда $\Upphi(F(x))=I(x)$
$\mathbf{D} I(x) = I_{n}(x)$ (единичная матрица в $R^{n}$) => $\mathbf{D}\Upphi(y_{0})\mathbf{D}F(x_{0}) = \mathbf{D}I(x_{0}) = I_{n}$
(это значит матрицы $\mathbf{D}\Upphi(y_{0}) \ \ \mathbf{D}F(x_{0})$ - обратимы)
Справедливо соотношение $\mathbf{D}\Upphi(y_{0})=(\mathbf{D}F(x_{0}))^{-1}$

Теорема:
$E \in R^{n}, \ \ n \ge 2$    $E$ - открыто,  $x_{0} \in E, \ \ y_{0} = F(x_{0})$
$F: \longrightarrow R^{n}, \ \ \ F \in C^{1}(E)$
Пусть $\mathbf{D}F(x_{0})$ - обратима, тогда $\exists U \subset E$ и $V$ - открытое:  $x_{0} \in U, y_{0} \in V$ и $F|_{V}$ - обратимо  $F(U)=V$
и если $\Upphi = (F|_{V})^{-1}$, то $\Upphi \in C^{1}(V)$

Доказательство:
==Шаг 1.== (определение множества $U$)
Пусть $A = \mathbf{D}F(x_{0})$
$|| \mathbf{D}F(x) - A ||_{R^{n}} = || \mathbf{D}F(x) - \mathbf{D}F(x_0) ||_{R^{n}}$
$\mathbf{D}F(x) - \mathbf{D}F(x_{0)}= \begin{bmatrix} f'_{1x_{1}}(x) - f'_{1x_{1}}(x_{0}) & \dots & f'_{x_{n}}(x) - f'_{x_{n}}(x_{0}) \\ \vdots & \ddots & \vdots \\ f'_{nx_{1}}(x) - f'_{nx_{1}}(x_{0}) & \dots & f'_{nx_{n}}(x) - f'_{nx_{n}}(x_{0})\end{bmatrix} * \mathbf{D}F(x)$ =$\begin{bmatrix} f'_{1x_{1}}(x) & \dots & f'_{x_{n}}(x) \\ \vdots & \ddots & \vdots \\ f'_{nx_{1}}(x) & \dots & f'_{nx_{n}}(x) \end{bmatrix}$
$\lambda = \frac{1}{4||A^{-1}||}$
(по 6 свойству лекции от 05.09)  $|| \mathbf{D}F(x) - \mathbf{D}F(x_{0}) || = (\sum\limits_{i=1}^{n}\sum\limits_{j=1}^{n}(f'_{ix_{i}}(x) - f'_{jx_{j}}(x_{0}))^{2})^\frac{1}{2}$ ==(1)==
$f \in C(E), (1)$ => $|| \mathbf{D}F(x) - \mathbf{D}F(x_{0}) || \underset{x\to x_{0}}{\longrightarrow}  0$  ==(2)==
(2) => $\exists r>0 : \ \ \forall \ x \in B_{r}(x_{0}) : \ \ || \mathbf{D}F(x) - A||_{R^{n}} < 2\lambda$  ==(3)==
$V = B_{r}(x_{0})$  ==(4)==
==Шаг 2== $F|_{V}$ - инъективно
Замечание о выпуклости шара: $x_{1} \in B_{r}(x_{0}), \ x_{2} \in B_{r}(x_{0}), \ 0<t<1$ => $tx_{1} + (1-t)x_{2} \in B_{r}(x_{0})$
Доказательство: $||tx_{1} + (1-t)x_{2} -x_{0}||_{R^{n}} = ||t(x_{1}-x_{0}) + ((1-t)x_{2} -x_{0})||_{R^{n}} \le$
$\le||t(x_{1}-x_{0})||_{R^{n}} + ||((1-t)x_{2} -x_{0})||_{R^{n}} < t*r + (1-t)r = r$
ч.т.д.
Следствие: $x \in B_{r}(x_{0}), \ \ \ x+H \in B_{r}(x_{0}), \ \ 0<t<1$ => $x+tH \in B_{r}(x_{0})$
Доказательство: $x_{1}=x+H, \ \ x_{2}=x$, тогда $tx_{1}+(1-t)x_{2} = tx + t+1 + (1-t)x = x+tH$ ч.т.д.
$x \in B_{r}(x_{0}), \ H \ne \mathbb{O}_{n}, \ \ x+H \in B_{r}(x_{0}), \ \ F|_{V}(x+H) - F|_{V}(x) \overset{?}{\ne} \mathbb{O}_{n}$
$t\in [0,1] \ \ p(t) = F|_{V}(x+tH) - tAH$  ==(5)==      $p: [0,1] \longrightarrow R^{n}$
$\mathbf{D}p(t) = \mathbf{D}(F|_{V}(x+tH)) - \mathbf{D}(tAH)$  ==(6)==
$q(t) = x + tH$    
(6): $\mathbf{D}p(t) = \mathbf{D}(F|_{V}(q(t))) - \mathbf{D}(tAH)$  ==(7)==
$y \in R^{n}, \ \ t \longrightarrow ty$ => $\mathbf{D}(ty) = y$ => $\mathbf{D}(tAH) = AH, \ \ \mathbf{D}q(t) = H$ => $\mathbf{D}F|_{V}(q(t)) = \mathbf{D}F|_{V}(q(t))\mathbf{D}q(t) = \mathbf{D}F|_{V}(x+tH)*H$
Следовательно (7) => $\mathbf{D}p(t) = \mathbf{D}F|_{V}(x+tH)H-AH$  ==(8)==
Рассмотрим  $\lambda = \frac{1}{4||A^{-1}||}, \ \ \ ||A^{-1}|| = \frac{1}{4\lambda}, \ \ \ \forall H \ne \mathbb{O}_{n}$
$H = (A^{-1}A)H = A^{-1}(AH)$ => $||H||_{R^{n}} = ||A^{-1}(AH)||_{R^{n}} \le ||A^{-1}||_{R^{n}} ||AH||_{R^{n}} = \frac{1}{4\lambda}||AH||_{R^{n}}$ => $||AH||_{R^{n}} \ge ||A^{-1}||_{R^{n}} 4\lambda$  ==(9)==
$p(1) - p(0) = F|_{V}(x+H) - AH - F|_{V}(\lambda) = F|_{V}(x+H) - F|_{V}(\lambda) - AH$  ==(10)==
Применим теорему Лагранжа для вектор-функций:
$\exists \ c \in (0,1): \ ||p(1) - p(0)||_{R^{n}} \le ||\mathbf{D}p(c)||_{R^{n}}$  ==(11)==
(8) => $||\mathbf{D}p(c)||_{R^{n}} = ||(\mathbf{D}F|_{V}(x+cH) - A)H||_{R^{n}} \le ||\mathbf{D}F|_{V}(x+cH)A||_{R^{n}} - ||H||_{R^{n}} < 2\lambda*||H||_{R^{n}} \le \frac{1}{2}||AH||_{R^{n}}$  ==(12)==
(10)(11)(12) => $||F|_{V}(x+H) - F|_{V}(x) + AH||_{R^{n}} \le \frac{1}{2}||AH||_{R^{n}}$  ==(13)==
(13) => $||F|_{V}(x+H) - F|_{V}(x)||_{R^{n}} = ||AH + F|_{V}(x+H) - F|_{V}(x) - AH||_{R^{n}} \ge$ 
$\ge ||AH||_{R^{n}} - ||F|_{V}(x+H) - F|_{V}(x) - AH||_{R^{n}} \ge ||AH||_{R^{n}} - \frac{1}{2}||AH||_{R^{n}} = \frac{1}{2}||AH||_{R^{n}} \ge 2\lambda||H||_{R^{n}} > 0$

**продолжение доказательства в 9-10**