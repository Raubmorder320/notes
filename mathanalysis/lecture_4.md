*продолжение*

(17)=>$Dg(t)=Df(v)|_{v=y+tH}*D\Uppsi(t)$(18)
$Dg(t)=g'(t)$(19')
$Df(v)|{v=y+tH}= (f'_{x_1}(y+tH),...,f'_{x_n}(y+tH))$(19)
$D\Uppsi(t)= \begin{bmatrix}h_{1} \\ . \\ . \\ . \\ h_{n}\end{bmatrix}$(20)
(18),(19),(19'),(20)=> $g'(t)= \sum\limits_{v=1}^{n}f'_{x_v}(y+tH)h_v$(21)
$f\in C^{r+1}(E)$
$t\in (-a,a)$
$|\beta|=r+1, \ \ \beta=(\beta_1,...,\beta_n)=(0,..,\beta_i,0,..,]\beta_j,...,0)$
$\beta_{i_{k}}\ne 0, \ 1<=k<=l$
$\alpha^{(1)}=(0,..,\beta_{i_{1}}^{-1},0...,\beta_{i_2},..,\beta_{i_l},..0)$
$\alpha^{(2)}=(0,..,\beta_{i_{1}},0...,\beta_{i_2}^{-1},..,\beta_{i_l},..0)$
.
$\alpha^{(l)}=(0,..,\beta_{i_{1}},0...,\beta_{i_2},..,\beta_{i_l}^{-1},..0)$

$|\alpha|=r, \ \ \alpha+e_{\nu}=\beta$  =>  $\nu=i_{1} \ или \ i_{2} \ или \ i_l$(22) 
$g^{(r)}(y+tH)= \sum\limits_{|\alpha|=r} C^{\alpha}_{r}\partial^{\alpha}f(y+tH)H^{\alpha}$(23)
(22),(23)=>$g^{(r+1)}(y+tH)=\sum\limits_{|\alpha|=r} C^{\alpha}_{r}H^{\alpha}(\partial^{\alpha}f(y+tH))'$=
$\partial^{\alpha}f(y+tH)=f_{\alpha}$ (временное обозначение)
=$\sum\limits_{|\alpha|=r} C^{\alpha}_{r}H^{\alpha}(\sum\limits_{v=1}^{n}f'_{\alpha x_v}(y+tH)h_v)$
$\sum\limits_{|\alpha|=r} \sum\limits_{v=1}^{n}C^{\alpha}_{r}H^{\alpha}h_v(\partial^{\alpha} f(y+tH)))'_{x_{\nu}}$
$\alpha=(e_1,e_\nu,e_n)$
$(\partial^{\alpha}f(X))'_{x_\nu}=f^{(r+1)}_{x_1,..,x_1,x_{\nu},...,x_{\nu},...,x_n,..x_n}(x)=\partial^{\alpha+e_\nu}f(X)$(24)
$H^{\alpha}h_\nu=h_{1}^{e_{1}}*h_{\nu}^{e_{\nu}}*...*h_{n}^{e_{n}}*...*h_{\nu}^{e_{\nu}}=H^{\alpha+e^{\nu}}$
$\sum\limits_{|\alpha|=r} \sum\limits_{v=1}^{n}C^{\alpha}_{r}H^{\alpha+e^{\nu}}\partial^{\alpha+e^\nu} f(y+tH))$(25)
$\alpha+e^{\nu}=\beta$
$|\beta|=r+1$
$\beta=(0,..,\beta_{i_1},..,\beta_{i_l},..,0)$
$\beta_{i_{k}}\ne 0$
(25)=$\sum\limits_{|\beta|=r+1}\partial^{\beta}f(y+tH)H^{\beta}\sum\limits_{по \ всем \ \alpha \ и \ \nu \ т.ч. \ \alpha+e_{\nu}=\beta}C^{\alpha}_{r}$
$1<=\mu<=l$
$\nu=i_1,...,i_l$
$\alpha^{(\mu)}=(0,..,\beta_{i_1},..,\beta^{-1}_{i_{\mu}},..,0,..,\beta_{i_l},..,0)$
$\alpha^{(\mu)}+e_{i_\mu}=\beta$(26)
(26)=>  $\sum\limits_{\alpha+e_{\nu}=\beta}C^{\alpha}_{r}=\sum\limits_{\mu=1}^{l}C^{\alpha^{(\mu)}}_{r}=\sum\limits_{\mu=1}^{l} \frac{r!}{\beta_{i_1}!*..*(\beta_{i_{\mu}})^{-1}!*..*\beta_{i_{l}}!}$ = $\frac{r!}{\beta_{i_1}!*..*(*..*\beta_{i_{l}}!}\sum\limits_{\mu=1}^{l}\beta_{i_{mu}}$ = $\frac{r!}{\beta!}|\beta| = \frac{r!}{\beta!}(r+1)= \frac{(r+1)!}{\beta!} = C^{\beta}_{r+1}$(27)
(25),(26),(27)=> $g^{(r+1)}(t)= \sum\limits_{|\beta|=r+1}\partial^{\beta}f(y+tH)H^{\beta}C^{\beta}_{r+1}$
ч.т.д.

#### Формула Тейлора с остатком формулы Лагранжа для функции от n переменных
$E\subset R^{n},n >=2, E$-открыто
$x_{0}\in E, \ \ B_{\delta}(x_{0})\subset E$
$f\in C^{(r+1)}(E), \ \ \ H\in R^{n}, \ \ ||H||_{R^{n}}<\delta$
$\exists c, \ 0<c<1$
$f(x_{0}+H)=f(x_{0})+ \sum\limits_{k=1}^{r} \sum\limits_{|\alpha|=k} \frac{1}{\alpha!}\partial^{\alpha}f(x_{0})H^{\alpha}+\sum\limits_{|\alpha|=r+1}\frac{1}{\alpha!}\partial^{\alpha}f(x_{0}+cH)H^{\alpha}$
Доказательство:
$g(t)=f(x_{0}+tH)$
$g(1)=f(x_{0}+H)$
$g(0)=f(x_{0})$
$g\in C^{r+1}(-a,a)$
$g(1)=g(0)+ \sum\limits_{k=1}^{r} \frac{g^{(k)}(0)}{k!}1^{k}+ \frac{1}{(r+1)!}g^{(r+1)}(c)1^{r+1}$ = $g(0) + \sum\limits_{k=1}^{r} \frac{1}{k!}g^{(k)}(0)+ \frac{1}{(r+1)!}g^{(r+1)}(c)$ = $f(x_{0}) + \sum\limits_{k=1}^{r} \frac{1}{k!} \sum\limits_{|\alpha|=k}C^{\alpha}_{k}\partial^{\alpha} f(x_{0}) g^{(k)}(0)+ \frac{1}{(r+1)!}g^{(r+1)}(c)$
