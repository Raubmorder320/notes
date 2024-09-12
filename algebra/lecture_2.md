11.09.
еще одно замечание к прошлому параграфу:
##### **Предложение:** "Модельный пример" циклического пространства\
$K[t]|_{p(t)}$ -    под $K$с базисом $1, t,....,t^{n-1}$
линейный оператор умножения на $E$
$\mu_t: K[t]|_{p(t)}\rightarrow K[t]|_{p(t)}$
$\tilde{f(t)}\rightarrow t*\tilde{f(t)}$
Матрица $[\mu_t]_{1,t,..,t^{n-1}}$ = (матрица)$\begin{pmatrix}\end{pmatrix}$

Если $V_k,A$ - циклическое пространство $V=<v> \ \ \ \mu_{A,v}(k)=p(t)$, то оно изоморфно
$(K[t]|_{p(t)},\mu_t)$, т.е. коммутативна
(комм диаграмма)

Доказывать тут нечего:)

##### Задача:
Инвариантные подпространства в $(K[t]|_{p(t)},\mu_t)$; $(K[t]|,\mu_t)$?
$(t^2+2t-1)*f(t)$ - это идеал в кольце $K[t]$
Задача в том, чтобы доказать, что пространство находится в биективном соответствии с его делителями $g(t)|p(t)$
### Аннуляторы
$\mu_{A,v}(t)$ - min ann вектора
$L \subset V \ \ \mu_{A,L}(t)$ - min ann $L=НОД(f(t):f(A)(x)=0 \forall x \in L)$
произведение аннулятораа делится на минимальный аннулятор
**Замечание**: $\mu_{A,L}(t)=\mu_{A,<L>}(t)$
$U=<x_1,...x_l>$
$\mu_{A,U}(t)=НОК(\mu_{A,x_{i}}(t))$
$L_{1}\subset L_2$   $\mu_{A,L_1}(t)|\mu_{A,L_2}(t)$
$\mu_{A,U_1+U_2}(t)=НОК(\mu_{A,U_1}(t),\mu_{A,U_2}(t))$
Аналогичное утверждение для $U_{1}(пересечение) U_2$
##### Предложение:
$\frac{НОК(...)}{НОД(...)} \ | \ \mu_{A,x+y}(t) \ | \ НОК(\mu_{A,x}(t),\mu_{A,y}(t))$

Доказательство:
Если $(\mu_{A,x}(t), \mu_{A,y}(t))=1$, то $\mu_{A,x+y}(t)=\mu_{A,x}(t)*\mu_{A,y}(t)$
                                =f(t)           =g(t)
Докажем, что левая часть делится на правую.
$\mu_{A,x+y}(t):\mu_{A,x}(t)$
$\uparrow$
$\mu_{A,x+y}(t)*g(t):f(t)$
$\uparrow$
$\mu_{A,x+y}(t)*g(A)(x)=0$   т.к. произведение анн делится на минимальный
$\uparrow$
$g(A)(x)=g(A)(x+y)$
$\uparrow$
$g(A)\mu_{A,x+y}(A)(x+y)=0$

**Опр**  $\mu_{A,V}(t)=\mu_{A}(t)$  минимальный многочлен оператора
##### Следствие теоремы Гамильтона-Кэли
Характеристический многочлен оператора делится на минимальный
##### Предложение:
$\chi_{A}(t)$ и $\mu_{A}(t)$ имеют одинаковый набор простых делителей
**Док-во над $С$:**
$\forall$ собственного числа $\lambda$ оператора $А$  $t-\lambda|\mu_{A}(t)$
возьмем собственный вектор 
$A(v)=\lambda v$
$\downarrow$                $A^{k}(v)-\lambda^{k}*v$
$p(A)(v)=p(\lambda)v$

$K[t]\rightarrow End(V)$
$t \rightarrow A$
$a \rightarrow aE$
$p(A)=0$ => $p(\lambda)=0$

неприводимый
$\downarrow$
$p(t)|\chi_{A}(t)$ => $p(t)|\mu_{A}(t)$
$\downarrow$
$1 \ne (p(t),\mu_{A}(t))$
$p(t)$ делится на $t-\lambda$
ч.т.д.
Предложение как следствие нашего последнего доказательства теоремы Гамильтона-Кэли:
Если $V$ - циклическое, то $\chi_{A,V}(t)=\mu_{A}(t)=\chi_{A}(t)$,  где $V=<v>_{A}$
(чето с матрицами)

### Примарное разложение пространства с оператором
Пространство с оператором можно разложить в прямую сумму инвариантных подпространств в соответствии с каноническим разложением $\chi_{A}(t)(\mu_{A}(t))$ на множители в $K[t]$. 
Прямые слагаемые биективно отвечаются неприводимым делителям $\chi_{A}(t)(\mu_{A}(t))$

##### Лемма о коммутирующих операторах
$A,B: V \rightarrow V$ такие, что $A*B=B*A$
тогда $Ker(B), \ Int(B)$ инвариантны относительно $А$
В частности $Ker(g(A)), \ Int(g(A))$ инвариантны относительно $А$
Док-во:
Возьмем $x\in Ker(B)$
$A(x)\in Ker(B) \leftarrow (BA)(x)=(AB)(x)=A(0)=0$
Возьмем $x\in Int(B)$, т.е. $x=B(y)\rightarrow A(x)=A(B(y))=B(A(y)) \in Int(B)$

$A,g(A)$ коммутируют 
$K[t] \rightarrow End(V)$
$f(t)\rightarrow f(A)$
$(f*g)(A)=f(A)g(A)$
ч.т.д.
##### Лемма 
$(f(t),g(t))=1$      $A: V \rightarrow V$
Тогда $Ker(fg)(A)=Ker(f(A))\oplus Ker(g(A))$
 
 Док-во:
 Из теоремы о представлении НОД
 надо проверить:
 1) $Ker(f(A))(пересечь)Ker(g(A))=0$
2) $Ker(f(A))+Ker(g(A))=Ker(fg(A))$
$\subset$ очевидно

$1 = a(t)f(t)+b(t)g(t)$
подставим $A$:    $Id=a(A)f(A)+b(A)g(A)$
$v=Id(v)=a(A)f(A)(v)+b(A)g(A)(v)$
$f(A)\in Ker(g(A))$,  $g(A)\in Ker(f(A))$
Возьмем $v \in Ker(fg)(A)$
$u=g(A)(v)\in Ker(f(A))$
$b(t)g(t)=1 \ mod f(t)$
$b(A)(u)=b(A)g(A)(v)=v-a(A)f(A)(v)$
ч.т.д

**Следствие.** Если $\mu_{A}(t)= f_{1}(t)*f_{2}(t)*...*f_{r}(t)$ 
$V=Ker(f_{1}(A))\oplus Ker(f_{2}(A))\oplus....\oplus Ker(f_{r}(A))$
Индукция по r:
$f_{r}(t)()$