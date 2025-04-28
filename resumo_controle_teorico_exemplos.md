# Resumo Teórico com Exemplos e Cálculos

## 1. Transformada de Laplace
**Definição**  
\[
F(s) = \int_{0}^{\infty} e^{-s t}\,f(t)\,dt
\]  
(Sua base na análise frequência) citeturn0file2  

**Exemplo**  
Para \(f(t) = 5\,u(t)\):  
1. \(u(t) = 1\) para \(t \ge 0\).  
2. \(F(s) = 5 \int_0^\infty e^{-s t} \,dt = 5 \bigl[ -e^{-s t}/s \bigr]_0^\infty = 5/s\).  

---

## 2. Teoremas do Valor Inicial e Final
- **Valor Inicial**:  
  \[
    f(0^+) = \lim_{s\to\infty} s\,F(s)
  \] citeturn0file1  
- **Valor Final**:  
  \[
    f(\infty) = \lim_{s\to0} s\,F(s)
  \] citeturn0file1  

**Exemplo**  
Para \(F(s) = \tfrac{10}{s+2}\):  
- \(f(0^+) = \lim_{s\to\infty} s \cdot \tfrac{10}{s+2} = 10.\)  
- \(f(\infty) = \lim_{s\to0} s \cdot \tfrac{10}{s+2} = 0.\)  

---

## 3. Função de Transferência
**Definição**  
\[
G(s) = \frac{Y(s)}{U(s)}
\]  
(com condições iniciais nulas) citeturn0file2  

**Exemplo de Uso**  
Circuito RC: \(R=1\,\text{k}\Omega\), \(C=1\,\mu\text{F}\).  
- \(G(s) = 1/(RC\,s + 1) = 1/(0{,}001\,s + 1).\)  
- Constante de tempo \(\tau = RC = 0{,}001\) s.  

---

## 4. Sistemas de Primeira Ordem
**Forma**  
\[
G(s) = \frac{k}{s + p}
\]  
Resposta ao degrau unitário:  
\[
y(t) = \frac{k}{p}\Bigl(1 - e^{-p t}\Bigr)
\] citeturn0file1  

**Exemplo e Cálculo**  
Para \(k=2\) e \(p=4\,\text{s}^{-1}\):  
- \(y(t) = 0{,}5\bigl(1 - e^{-4t}\bigr).\)  
- \(\tau = 1/p = 0{,}25\) s; em \(t=0{,}25\) s:  
  \[
    y(0{,}25) = 0{,}5\bigl(1 - e^{-1}\bigr) \approx 0{,}5 \times 0{,}63 = 0{,}315.
  \]  

---

## 5. Sistemas de Segunda Ordem
**Forma**  
\[
G(s) = \frac{\alpha\,\omega_n^2}{s^2 + 2\zeta\omega_n s + \omega_n^2}
\] citeturn0file3  

**Parâmetros**  
- Fator de amortecimento \(\zeta\).  
- Frequência natural \(\omega_n\).  
- Frequência amortecida \(\omega_d = \omega_n\sqrt{1-\zeta^2}\).  

**Exemplo e Cálculos**  
Para \(\zeta=0{,}5\), \(\omega_n=10\,	ext{rad/s}\):  
- \(\omega_d = 10\sqrt{1-0{,}25} = 8{,}66\) rad/s.  
- Pico máximo:  
  \[
    M_p = e^{-\frac{\zeta\pi}{\sqrt{1-\zeta^2}}}
        = e^{-\frac{0{,}5\pi}{\sqrt{0{,}75}}}
        \approx 0{,}455.
  \]
- Tempo de pico:  
  \[
    t_p = \frac{\pi}{\omega_d} \approx \frac{3{,}14}{8{,}66} = 0{,}36\text{ s}.
  \]
- Tempo de acomodação (2%):  
  \[
    T_s = \frac{4}{\zeta\omega_n} = \frac{4}{0{,}5\times10} = 0{,}8\text{ s}.
  \]  

---

## 6. Estabilidade de Sistemas
**Critério de Routh–Hurwitz**  
- Constrói-se tabela de Routh; mudanças de sinal na primeira coluna = polos instáveis citeturn0file0  

**Exemplo de Cálculo**  
Para polinômio \(s^3 + 2s^2 + 3s + 4\):  
| Linha | Coeficientes |
|:-----:|:-------------|
| \(s^3\) | 1 , 3 |
| \(s^2\) | 2 , 4 |
| \(s^1\) | \(rac{2\cdot3 - 1\cdot4}{2} = 1\), 0 |
| \(s^0\) | 4 |

Primeira coluna: [1, 2, 1, 4] – sem mudanças de sinal → sistema estável.  

---

*Fim do resumo.*  
