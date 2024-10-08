# Касательная прямая (3 параграф)

## Лемма
Пусть $\overline{r}(t), \ t \in I$ - регулярная параметризация элементарной кривой $C$. Вектор функция $\overline{r}_{1}(\tau), \tau \in I,$ является регулярной параметризацией той же кривой $С$ тогда и только тогда когда существует дифференциальная биекция $\phi: I_{1} \rightarrow I$ такая что $\dot{\phi}(\tau) \ne 0 \ \text{и} \ \overline{r}_{1}(\tau) = \overline{r}(\phi(\tau))$ для всех $\tau \in I$ 

### Доказательство
$\textcolor{GREEN}{\Leftarrow}$ : Прямо следует из правила дифференцирования сложной функции. В самом деле,$\overline{r}_{1}(\tau) = \overline{r}(\phi(\tau))$ регулярна, т.к. $\dot{\overline{r}}_{1}(\tau)=\dot{\phi}(\tau)\dot{\overline{r}} \neq 0$. притом $\dot{\phi} \neq 0, \dot{\overline{r}} \neq 0$
$\textcolor{green}{\Rightarrow}$ : Очевидно, существует гомеоморфизм $\phi = \overline{r}^{-1} \circ r_{1}:I_{1}\rightarrow I$ такой, что $\overline{r_{1}}(\tau)=\overline{r}(\phi(\tau))$. Покажем, что $\phi(\tau)$ дифференцируема. 
$$
(*) = \frac{\overline{r}_{1}(\tau +\Delta \tau)-\overline{r}_{1}(\tau)}{\Delta \tau} =\frac{\overline{r}_{1}(\tau +\Delta \tau)-\overline{r}_{1}(\tau)}{\Delta \tau} \dots
$$
#дописать  $$