#  Modelo M/M/1/K (∞ población)

## Parámetros
- **λ** = tasa de llegada  
- **μ** = tasa de servicio  
- **K** = capacidad máxima del sistema (cola + servicio)  
- **ρ = λ / μ** (factor de utilización)  

---

##  Fórmulas principales

1. **Probabilidad de 0 clientes**  
$P_0 = \frac{1 - \rho}{1 - \rho^{K+1}}, \quad (\rho \neq 1)$

2. **Probabilidad estado n**  
$P_n = P_0 \cdot \rho^n, \quad n = 0,1,\dots,K$

3. **Probabilidad de bloqueo**  
$P_K = P_0 \cdot \rho^K$

4. **Tasa de llegada efectiva**  
$\lambda_{eff} = \lambda \cdot (1 - P_K)$

5. **Número medio en el sistema**  
$N_s = \frac{\rho \, \left( 1 - (K+1)\rho^K + K\rho^{K+1} \right)}{(1-\rho)(1-\rho^{K+1})}, \quad (\rho \neq 1)$

6. **Número medio en cola**  
$N_w = N_s - (1 - P_0)$

7. **Tiempos promedio (Little)**  
$T_s = \frac{N_s}{\lambda_{eff}}, \qquad T_w = \frac{N_w}{\lambda_{eff}}$

---

##  Simulación de Escenarios

Se toma **K = 10** y **μ = 5** (5 clientes/tiempo).  
Se varía **λ** entre 0.1 y 2 para analizar tres escenarios:

---

###  1. Baja carga (λ = 0.1, ρ = 0.02)
- $P_0 \approx 0.981$  
- $P_K \approx 0.000$  
- $\lambda_{eff} \approx 0.100$  
- $N_s \approx 0.020$  
- $N_w \approx 0.001$  
- $T_s \approx 0.200$  
- $T_w \approx 0.010$  

 Sistema casi vacío, esperas mínimas.

---

###  2. Carga media (λ = 1, ρ = 0.2)
- $P_0 \approx 0.834$  
- $P_K \approx 1.07 \times 10^{-7}$  
- $\lambda_{eff} \approx 1.0$  
- $N_s \approx 0.25$  
- $N_w \approx 0.084$  
- $T_s \approx 0.25$  
- $T_w \approx 0.084$  

 Flujo estable, con algo de cola.

---

###  3. Alta carga (λ = 2, ρ = 0.4)
- $P_0 \approx 0.600$  
- $P_K \approx 1.58 \times 10^{-4}$  
- $\lambda_{eff} \approx 2.0$  
- $N_s \approx 0.67$  
- $N_w \approx 0.27$  
- $T_s \approx 0.33$  
- $T_w \approx 0.13$  

 El sistema empieza a congestionarse, aunque aún dentro de capacidad.

---






