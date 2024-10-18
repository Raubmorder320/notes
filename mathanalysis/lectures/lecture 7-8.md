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
$A$ - обратима <=> det$A \ne o$
$A$ - обратима <=>$Ax = \mathbb{O}_{n} \ \forall x \ne \mathbb{O}_{n}$ 
Теорема:
Пусть $A_{n \times n}$ - обратимая матрица,  $||A^{-1}|| = \frac{1}{\alpha}, \ \alpha > 0$
Пусть $B$ т.ч. $||B - A|| = \beta, \ \ 0<\beta<\alpha$ , тогда $B$ - обратима и $||A^{-1} - B^{-1}||_{R^{n}} \le \frac{\beta}{\alpha(\alpha - \beta)}$
Доказательство:
$x = \mathbf{I}x = AA^{-1}(x), \ x \in R^{n}$ => $||x||_{R^{n}} = ||A^{-1}(Ax)||_{R^{n}} \le ||A^{-1}||_{R^{n}}||Ax||_{R^{n}} = \frac{1}{\alpha}||Ax||_{R^{n}}$ 
=> $||Ax||_{R^{n}} \ge \alpha ||x||_{R^{n}}$   ==(9)==
$Bx = Ax+(Bx - Ax)$ => $||Bx||_{R^{n}} \ge ||Ax||_{R^{n}} - ||Bx - Ax||_{R^{n}}$  ==(10)==
$||Bx - Ax||_{R^{n}} = ||(B - A)x||_{R^{n}} \le ||(B - A)||_{R^{n}}||x||_{R^{n}}$  ==(11)==
(9)-(11) =>$|| Bx ||_{R^{n}} \ge \alpha||x||_{R^{n}} - ||(B-A)||_{R^{n}}||x||_{R^{n}} = \alpha ||x||_{R^{n}} - \beta ||x||_{R^{n}}$  ==(12)==
(12) => $B$ - обратимая (если $x \ne \mathbb{O}_{n}$, то $||Bx||_{R^{n}} \ne 0$)
$\forall y \ne \mathbb{O}, \ \ x = B^{-1}y$
(12) => $||B(B^{-1}y)||_{R^{n}} \ge (\alpha - \beta) ||B^{-1}y||_{R^{n}}$   ==(13)==
$||BB^{-1}y||_{R^{n}} = ||\mathbf{I}y||_{R^{n}} = ||y||_{R^{n}} \ge (\alpha-\beta)||B^{-1}y||_{R^{n}}$ <=> $||B^{-1}y||_{R^{n}} = \frac{1}{\alpha-\beta}||y||_{R^{n}}$  ==(14)==
(14) => $||B^{-1}||_{R^{n}} \le 1/\alpha-\beta$  ==(15)==
Вычислим $A(A^{-1} - B^{-1})B = (A(A^{-1} - B^{-1}))B = (AA^{-1} - AB^{-1})B=$ 
$= (\mathbf{I} - AB^{-1})B = (\mathbf{I}B - AB^{-1}B) = \mathbf{I}B - A \mathbf{I} = B-A$  ==(16)== 
(16) => $A^{-1}A(A^{-1}-B^{-1})BB^{-1} = A^{-1}(B-A)B^{-1}$ <=> $A^{-1}-B^{-1} = A^{-1}(B-A)B^{-1}$  ==(17)==
(15),(16) => $||A^{-1}-B^{-1}||_{R^{n}} \le ||A^{-1}||_{R^{n}}||A-B||_{R^{n}}||B^{-1}||_{R^{n}} \le \frac{1}{\alpha}\beta \frac{1}{\alpha-\beta} = \frac{\beta}{\alpha(\alpha-\beta)}$
Пусть $E \subset R^{n}, \ \ n \ge 2 \ \ \ x_{0} \in E$ - внутренняя точка
$F: E \longrightarrow R^{n}$ - биекция  $G = F(E)$
$\exists \Upphi: G \longrightarrow E \ \ \Upphi(F(x)) = x \ \ \forall x \in E$
