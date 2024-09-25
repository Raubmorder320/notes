### Формула Тейлора с остатком в форме Пеано для функций от n переменных
#### Теорема: 
$f: E \rightarrow R$    $E \in R^{n}, \ n\geq2 \ \ x_{0}\in E, \ \omega \subset E$
$f \in C^{r}(\omega),  \ r \geq 1 \ \ \ f(x_{0}+H) \ = \ f(x_{0}) + \sum\limits_{k=1}^{n}\sum\limits_{|\alpha|=k} \frac{1}{\alpha!} \partial^{\alpha} f(x_{0})H^{\alpha} + \rho(H)$ ==(1)==
где $\frac{\rho(H)}{\|H\|^{2}}\rightarrow0, \ H\rightarrow0_{n}$ ==(2)==

Доказательство:
1. $r=1$  
Применим достаточное условие дифференцируемости $f$ в $x_0$ => 
=> $f(x_{0}) + \sum\limits_{\nu=1}^{n} f'_{x_0}(x_{0})h_{\nu} + \rho(H)$ ==(3)==, где $\frac{\rho(H)}{\|H\|}\rightarrow0, \ \ H\rightarrow0_{n}$ ==(4)== 
 $H = \begin{bmatrix} h_{1} \\ . \\ . \\ . \\ h_{n} \end{bmatrix}$
 Перепишем определение:
 $|\alpha|=1 \ \ \ \alpha=(0,..,1,0,..,0)$
 $C^{\alpha}_{1} \ = \ \frac{0!..1!..0!}{1!}$
$\sum\limits_{\nu=1}^{n}f'_{x_{0}}h_{\nu} \ = \ \sum\limits_{|\alpha|=1}C^{\alpha}_{1}\partial^{\alpha}f(x_{0})H^{\alpha}$ ==(5)==
2. $r\geq2$
$\exists c \in (0,1): \ f(x_{0}+H) \ = \ f(x_{0}) + \sum\limits_{k=1}^{r-1}\sum\limits_{|\alpha|=r} \frac{1}{\alpha!} \partial^{\alpha} f(x_{0})H^{\alpha} + \sum\limits_{|\alpha|=r} \frac{1}{\alpha!} \big(\partial^{\alpha} f(x_{0}+cH)-\partial^{\alpha} f(x_{0})\big)H^{\alpha}$==(6)==
$f \in C^{r}(\omega)$=>$\partial^{\alpha}f(x_{0}+cH)-\partial^{\alpha}f(x_{0}) \ \rightarrow 0, H \rightarrow 0_{n} \ \ \forall \alpha, \ |\alpha|=r$ ==(7)==
$H^{\alpha}=h_{1}^{\alpha_{1}}...h_{n}^{\alpha_{n}}$=>$|H| \leq \|H\|^{\alpha_1}...\|H\|^{\alpha_n}=\|H\|^{|\alpha|}=\|H\|^{r}$
$\frac{\partial^{\alpha}f(x_{0}+cH)-\partial^{\alpha}f(x_{0})}{\|H\|^{r}} \leq |\partial^{\alpha}f(x_{0}+cH)-\partial^{\alpha}f(x_{0})| \longrightarrow 0, H \longrightarrow 0_{n}$ ==(8)==
(8)(6)=>(2)
ч.т.д

### Дифференциалы второго и последующих порядков
