# Resumo Teórico de Sistemas de Controle

## 1. Transformada de Laplace
- **Definição**: 
  \[
    F(s) = \mathcal{L}\{f(t)\} = \int_{0}^{\infty} e^{-st}\,f(t)\,dt
  \] citeturn0file2
- **Propriedades**:
  - Linearidade: \(\mathcal{L}\{a f_1 + b f_2\} = aF_1(s) + bF_2(s)\).
  - Derivada: \(\mathcal{L}\{f'(t)\} = sF(s) - f(0)\).
  - Integral: \(\mathcal{L}\{\int_0^t f(	au)\,d	au\} = rac{F(s)}{s}\).

## 2. Teoremas do Valor Inicial e Final
- **Valor Inicial**:
  \[
    \lim_{t 	o 0^+} f(t) = \lim_{s 	o \infty} sF(s)
  \] citeturn0file1
- **Valor Final**:
  \[
    \lim_{t 	o \infty} f(t) = \lim_{s 	o 0} sF(s)
  \] citeturn0file1

## 3. Função de Transferência
- **Definição**: 
  \[
    G(s) = rac{Y(s)}{U(s)}
  \]
  com condições iniciais nulas. citeturn0file2
- **Polos e Zeros**:
  - **Polos**: raízes de denominação de \(G(s)\); determinam estabilidade.
  - **Zeros**: raízes do numerador; influenciam resposta em frequência.

## 4. Sistemas de Primeira Ordem
- **Função de Transferência**:
  \[
    G(s) = rac{k}{s + p}
  \]
- **Resposta ao Degrau Unitário**:
  \[
    y(t) = rac{k}{p}\Bigl(1 - e^{-p t}\Bigr)
  \] citeturn0file1
- **Constante de tempo**:
  \(	au = rac{1}{p}\).
- **Tempos Característicos**:
  - Tempo de subida: \(T_r = rac{2{,}2}{p}\).
  - Tempo de acomodação: \(T_s = rac{4}{p}\). citeturn0file1

## 5. Sistemas de Segunda Ordem
- **Forma Geral**:
  \[
    G(s) = rac{k}{s^2 + a s + b}
      = rac{lpha \,\omega_n^2}{s^2 + 2\zeta\omega_n s + \omega_n^2}
  \] citeturn0file3
- **Parâmetros**:
  - Fator de amortecimento: \(\zeta = rac{a}{2\sqrt{b}}\).
  - Frequência natural: \(\omega_n = \sqrt{b}\).
  - Frequência amortecida: \(\omega_d = \omega_n \sqrt{1 - \zeta^2}\).
- **Classificação**:
  - Subamortecido: \(0 < \zeta < 1\).
  - Criticamente amortecido: \(\zeta = 1\).
  - Superamortecido: \(\zeta > 1\).
  - Não amortecido: \(\zeta = 0\). citeturn0file3
- **Indicadores de Transiente**:
  - Pico máximo: \(M_p = e^{-rac{\zeta\pi}{\sqrt{1-\zeta^2}}}\).
  - Tempo de pico: \(t_p = rac{\pi}{\omega_d}\).
  - Tempo de subida aproximado: \(T_r pprox rac{1.8}{\omega_n}\).
  - Tempo de acomodação (2%): \(T_s = rac{4}{\zeta\omega_n}\). citeturn0file3

## 6. Estabilidade de Sistemas
- **Estabilidade Interna**:
  - Estável: todos os polos em Re(s) < 0.
  - Marginalmente estável: polos em Re(s) ≤ 0, com polos imaginários simples.
  - Instável: ao menos um polo em Re(s) > 0. citeturn0file0
- **Estabilidade BIBO**:
  - Saída limitada para toda entrada limitada. citeturn0file0
- **Critério de Routh–Hurwitz**:
  - Número de mudanças de sinal na primeira coluna da tabela = número de polos com Re(s) > 0. citeturn0file0
