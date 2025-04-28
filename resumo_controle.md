# Resumo de Sistemas de Controle

## 1. Transformada de Laplace
- **Definição**: \(F(s) = \int_0^\infty e^{-st} f(t)\,dt\). A base para análise no domínio da frequência. citeturn0file2
- **Propriedades principais**:
  - Linearidade: \(L\{a f_1 + b f_2\} = aF_1 + bF_2\).
  - Derivada: \(L\{f'\} = sF(s) - f(0)\).
  - Integral: \(L\{\int_0^t f\} = F(s)/s\).
- **Exemplo**: Degrau unitário \(u(t)\) → \(U(s) = 1/s\). citeturn0file2

## 2. Teoremas do Valor Inicial e Final
- **Valor Final**: \(\lim_{t	o\infty} f(t) = \lim_{s	o0} sF(s)\). citeturn0file1
- **Valor Inicial**: \(\lim_{t	o0^+} f(t) = \lim_{s	o\infty} sF(s)\). citeturn0file1
- **Exemplo rápido**: Para \(G(s)=rac{s-2}{(s+1)(s+4)}\) e entrada degrau unitário:
  - \(y(0^+) = 0\)
  - \(y(\infty) = -	frac12\) citeturn0file1

## 3. Função de Transferência (FT)
- **Definição**: \(G(s)=Y(s)/U(s)\), relaciona entrada e saída no domínio de Laplace. citeturn0file2
- **Polos e Zeros**:
  - Polos: raízes do denominador; definem estabilidade.
  - Zeros: raízes do numerador; influenciam formato da resposta.
- **Exemplos práticos**:
  - **Circuito RC**: \(G(s)=1/(RC\,s+1)\). Filtro de graves num auto‑rádio. citeturn0file2
  - **Massa‑mola‑amortecedor**: \(G(s)=1/(m s^2 + b s + k)\). Suspensão de carro absorvendo impacto. citeturn0file2

## 4. Sistemas de Primeira Ordem
- **Forma**: \(G(s)=	frac{k}{s+p}\) → \(y(t)=	frac{k}{p}igl(1 - e^{-p t}igr)\). citeturn0file1
- **Constante de tempo**: \(	au = 1/p\). Em \(t=	au\), \(y=63\%\) de \(y(\infty)\).  
  - *Exemplo*: Chuveiro elétrico demora ~5 s para atingir 63% da temperatura; logo \(	aupprox5\,s\). citeturn0file1
- **Indicadores de desempenho**:
  - Tempo de subida: \(T_r = 2{,}2/p\).
  - Tempo de acomodação: \(T_s = 4/p\). citeturn0file1

## 5. Sistemas de Segunda Ordem
- **Forma**: \(G(s)=k/(s^2 + a s + b)\). Usamos:
  - Fator de amortecimento \(\zeta\).
  - Frequência natural \(\omega_n\).
  - Frequência amortecida \(\omega_d = \omega_n\sqrt{1-\zeta^2}\). citeturn0file3
- **Tipos de resposta**: 
  - Subamortecida (\(\zeta<1\)): senoide amortecida.
  - Criticamente amortecida (\(\zeta=1\)): resposta mais rápida sem overshoot.
  - Superamortecida (\(\zeta>1\)): sem oscilação, porém mais lenta.
  - Não amortecida (\(\zeta=0\)): oscilações permanentes. citeturn0file3
- **Métricas chave**:
  - Pico máximo: \(M_p = e^{-\zeta\pi/\sqrt{1-\zeta^2}}\).
  - Tempo de pico: \(t_p = \pi/\omega_d\).
  - Tempos de subida e acomodação: \(\displaystyle T_r pprox 1.8/\omega_n,\; T_s(2\%)=4/(\zeta\omega_n)\). citeturn0file3
- **Exemplo**: Suspensão de carro – controla o retorno do banco após um buraco na rua. citeturn0file3

## 6. Estabilidade de Sistemas
- **Definições**:
  - Estável: resposta natural → 0 quando \(t	o\infty\).
  - Instável: resposta natural → ∞.
  - Marginal: oscila sem crescer nem decair. citeturn0file0
- **Estabilidade BIBO**: saída limitada para toda entrada limitada. citeturn0file0
- **Estabilidade assintótica interna**: todos os polos no semiplano esquerdo. citeturn0file0
- **Critério de Routh‑Hurwitz**: número de mudanças de sinal na primeira coluna da tabela de Routh = número de polos instáveis.  
  - *Exemplo*: sistema com ganho \(K\) estável para \(0<K<1386\). citeturn0file0
