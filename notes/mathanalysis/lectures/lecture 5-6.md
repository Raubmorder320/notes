19.09

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
$\omega \subset R^{n}, \ n \geq 1, \ \omega$ - открыто
$f \in C^{1}(\omega), \ \ \ \partial^{1} f(x,H)=\partial f(x,H) = \sum\limits_{k=1}^{n}f'_{x_{k}}(\lambda)h_{k}$ - дифференциал
$H = \begin{bmatrix} h_{1} \\ . \\ . \\ . \\ h_{n} \end{bmatrix}$
$r \geq 1, \ \ f \in C^{r}(\omega) \ \ \ \partial^{r}f(x,H) = \sum\limits_{|\alpha|=r}A_{r ,\alpha}\partial^{\alpha}f(x)H^\alpha$ ==(9)==
$A_{1,\alpha}=1 \ \ \ \forall \alpha, \ \ \ |\alpha|=1$
$f \in C^{r+1}(\omega)$
$\partial^{r+1} f(x,H) = \sum\limits_{|\alpha|=r}A_{r ,\alpha}\partial(\partial^{\alpha}f(x))H^{\alpha} = \sum\limits_{|\alpha|=r+1}A_{r+1 ,\alpha}\partial^{\alpha}f(x))H^{\alpha}$ ==(10)==
$\partial^{1}f(x,H) = \sum\limits_{k=1}^{n}f'_{x_k}(x)h_k$
$\partial^{2}f(x,H) = \sum\limits_{k=1}^{n} \partial (f'_{x_k}(x))h_{k} = \sum\limits_{k=1}^{n} \left(\sum\limits_{l=1}^{n} f''_{x_{k}x_{l}}(x)h_{l}\right)h_{k} = \sum\limits_{k=1}^{n}\sum\limits_{l=1}^{n} f''_{x_{k}x_{l}}(x)h_{l}h_{k} = 1\sum\limits_{k=1}^{n} f''_{x_{k}x_{l}}(x)h_{k}^{2} + 2\sum\limits_{k<l} f''_{x_{k}x_{l}}(x)h_{k}h_{l} = \sum\limits_{|\alpha|=2}C_{2}^{\alpha} \partial f(x) H^{\alpha}$
$A_{2,\alpha} = C_{2}^{\alpha}$

#### Теорема
$A_{r,\alpha} = C_{r}^{\alpha}$ ==(11)==
Доказательство:
$\partial^{r+1} f(x,H) = \sum\limits_{|\alpha|=r} C_{r}^{\alpha} \partial(\partial^{\alpha}f(x))H^{\alpha} = \sum\limits_{|\alpha|=r} C_{r}^{\alpha}\left(\sum\limits_{\nu=1}^{n} (\partial^{\alpha}f)'_{x_{\nu}}(x) h_{\nu}\right) H^{\alpha}$ ==(12)==
(12) = $\sum\limits_{|\alpha|=r+1} C_{r+1}^{\alpha} \partial^{\alpha}f(x)H^{\alpha}$
$f(x_{0}+H) = f(x_{0}) + \sum\limits_{k=1}^{r} \frac{1}{k!} \partial^{k} f(x_{0},H) + \frac{1}{(r+1)!} \partial^{r+1} f(x_{0}+cH, H)$
$f(x_{0}+H) = f(x_{0}) + \sum\limits_{k=1}^{r} \partial^{k} f(x_{0},H) + \rho(H)$
$r=2 : \ \ f(x_{0}+H) = f(x_{0}) + \partial f(x_{0},H) + \frac{1}{2} \partial^{r} f(x_{0},H) + \rho(H)$ ==(13)==
$\frac{{\rho(H)}}{{\|H\|^{2}}} \longrightarrow 0, \ \ H \longrightarrow 0_{n}$ ==(14)==

13: $f(x_{0}+H) = f(x_{0}) + \sum\limits_{k=1}^{n} f'_{x_{k}}(x_{0})h_{k} + \frac{1}{2} \sum\limits_{k=1}^{n} \sum\limits_{l=1}^{n} f''_{x_{k}x_{l}}(x_{0}) h_{k}h_{l} + \rho(H)$ ==(15)==
$a_{kl} = \frac{1}{2} f''_{x_{k}x_{l}}(x_{0})$
$A(H) = \sum\limits_{k=1}^{n} \sum\limits_{k=1}^{n} a_{kl}h_{k}h_{l} \ \ \ \ (a_{kl}=a_{lk})$

#### Теорема
1) $A(H)$ - положительно определенная, тогда $\exists m_{1}>0: \ \ A(H) \geq m_{1}\|H\|^2$ ==(1)==
2) $A(H)$ - отрицательно определенная, тогда $\exists m_{2}>0: \ \ A(H) \leq -m_{2}\|H\|^2$ ==(2)==
Доказательство:
Рассмотрим единичную сферу $S = \{ H\in R^{n}: \ \ \|H\|=1\}$, $S$ - компакт в $R^n$
$A(H) \in C(R^{n})$
По второй теореме Вейерштрасса:  $\exists H_{0} \in S: \ \ \ \forall H \in S \ \ A(H_0)$ ==(3)==
Обозначим $m_{1} = A(H_{0})$, по условию $A(H_{0}>0)$
Рассмотрим $\forall H \ne 0_{n} \ \ \ t = \|H\|>0 \ \ \ \ H^{*}= \frac{1}{t}H$, тогда $\|H*\| = \| \frac{1}{t}H\| = \frac{1}{t}\| H\| = \frac{1}{t}t=1$
То есть $H* \in S$ => $A(H*) \geq m_{1}$
$A(H*) = A\left(\frac{1}{t}H\right) = \frac{1}{t^{2}} A(H) \geq m_{1}$ => $A(H) \geq m_{1}t^{2} = m_{1} \|H\|^{2}$


#### Теорема
$\omega \subset R^{n}$ - открытое  $x_{0}\in \omega \ \ \ f \in C^{2}(\omega)$
$f'_{x_{j}}(x_{0})=0, \ \ 1 \leq j \leq n$
1) Если $\partial^{2}f(x_{0}, H)$  положительно определенная => $x_{0}$ - строгий локальный минимум ==(4)==
2) Если $\partial^{2}f(x_{0}, H)$  отрицательно определенная => $x_{0}$ - строгий локальный максимум ==(5)==
3) Если $\partial^{2}f(x_{0}, H)$ неопределенная форма => нет локального экстремума ==(6)==
Доказательство:
$f(x_{0}+H) = f(x_{0}) + \partial f(x_{0},H) + \frac{1}{2} \partial^{2} f(x_{0}) + \rho(H)$ ==(7)==
(7): $f(x_{0}+H) = f(x_{0}) + \frac{1}{2} \partial^{2} f(x_{0}) + \rho(H)$ ==(7')==
$\frac{{\rho(H)}}{{\|H\|^{2}}} \longrightarrow 0, \ \ H \longrightarrow 0_{n}$
$\exists m_{1}>0: \ \ \ \partial^{2} f(x_{0}, H) >= m_{1}\|H\|^{2}$ ==(9)==
$\exists \delta > 0 : \ \ \ 0<\|H\|<\delta, \ \ \ \left| \frac{{\rho(H)}}{\|H\|^{2}} \right| < \frac{m_{1}}{4}$ ==(10)==
(10) => $|\rho(H)| < \frac{m_{1}}{4} \|H\|^{2}$ ==(11)==
(7'),(9),(11) =>$f(x_{0}+H) \geq f(x_{0}) + \frac{1}{2}\partial^{2} f(x_{0},H) - |\rho(H)| \geq f(x_{0}) + \frac{m_{1}}{2}\|H\|^{2}$
$\geq f(x_{0}) + \frac{m_{1}}{2}\|H\|^{2} - \frac{m_{1}}{4}\|H\|^{2} = f(x_{0}) + \frac{m_{1}}{4}\|H\|^{2} = f(x_{0}) + \frac{m_{1}}{4}\|H\|^{2} > f(x_{0})$ => (5)

$H_{1}^{*} = \frac{1}{\|H_{1}\|}H_{1} \ \ \ \ H_{1}^{*} \in S$

$H_{2}^{*} = \frac{1}{\|H_{2}\|}H_{2} \ \ \ \ H_{2}^{*} \in S$
$A(H_{1}^{*}) = \frac{1}{\|H_{1}\|^{2}} \ \ \ A(H_{1}) = p_{1}>0$
$A(H_{2}^{*}) = \frac{2}{\|H_{2}\|^{2}} \ \ \ A(H_{2}) = -p_{2}, \ \ p_{2}>0$
$t>0$
$A(tH_{2}^{*}) = t^{2}A(H_{2}^{*}) = -p_{2}t^{2}$ ==(12)==
$A(tH_{1}^{*}) = t^{2}A(H_{1}^{*}) = p_{1}t^{2}$ ==(13)==
$A(H) = \partial^{2} f(x_{0},H)$
$\delta_{1}>0 \ \ \ \ 0 < \|H\| < \delta_{1} \ \ \ \ |\rho(H)| < \frac{1}{4}\min(p_{1}, p_{2}) \|H\|^{2}$ ==(14)==
$0 < t < \delta_{1} \ \ \ \ \|tH_{1}^{*}\| = \|tH_{2}^{*}\| = t$
$f(x_{0}+tH_{1}) = f(x_{0}) + \frac{1}{2} \partial^{2} f(x_{0}, tH_{1}^{*}) + \rho(tH_{1}^{*}) \geq f(x_{0}) + \frac{1}{2}t^{2}\partial^{2}f(x_{0}, H_{1}^{*}) - |\rho(tH_{1}^{*})| > f(x_{0}) + \frac{1}{2} p_{1} t^{2} - \frac{1}{4} p_{1} t^{2} = f(x_{0}) + \frac{1}{4}p_{1}t^{2} > f(x_{0})$
$f(x_{0}+tH_{2}) \leq f(x_{0}) - \frac{p_{2}}{2} t^{2} + |\rho(H)| < f(x_{0})  - \frac{p_{2}}{2} t^{2} +  \frac{p_{2}}{4} t^{2} = f(x_{0}) - \frac{p_{2}}{4}t^{2} < f(x_{0})$
