#  Modelo M/M/1/K (∞ población)

## Parámetros
- **λ** = tasa de llegada  
- **μ** = tasa de servicio  
- **K** = capacidad máxima del sistema (cola + servicio)  
- **ρ = λ/μ** (factor de utilización)  

---

## 📐 Fórmulas principales

1. **Probabilidad de 0 clientes**
\[
P_0 = \frac{1-\rho}{1-\rho^{K+1}}, \quad (\rho \neq 1)
\]

2. **Probabilidad estado n**
\[
P_n = P_0 \, \rho^n, \quad n=0,1,\dots,K
\]

3. **Probabilidad de bloqueo**
\[
P_K = P_0 \, \rho^K
\]

4. **Tasa de llegada efectiva**
\[
\lambda_{\text{eff}} = \lambda (1 - P_K)
\]

5. **Número medio en el sistema**
\[
N_s = \frac{\rho \left(1-(K+1)\rho^K + K\rho^{K+1}\right)}{(1-\rho)(1-\rho^{K+1})}, \quad (\rho\neq1)
\]

6. **Número medio en cola**
\[
N_w = N_s - (1-P_0)
\]

7. **Tiempos promedio (Little)**
\[
T_s = \frac{N_s}{\lambda_{\text{eff}}}, 
\qquad 
T_w = \frac{N_w}{\lambda_{\text{eff}}}
\]

---

## 📊 Simulación de Escenarios

Se toma **K = 10** y **μ = 5** (5 clientes/tiempo).  
Se varía **λ** entre 0.1 y 2 para analizar tres escenarios:

---

###  1. Baja carga (λ = 0.1, ρ = 0.02)
- P₀ ≈ 0.981  
- Pₖ ≈ ~0.000  
- λ_eff ≈ 0.100  
- Ns ≈ 0.020  
- Nw ≈ 0.001  
- Ts ≈ 0.200  
- Tw ≈ 0.010  

✅ Sistema casi vacío, esperas mínimas.

---

###  2. Carga media (λ = 1, ρ = 0.2)
- P₀ ≈ 0.834  
- Pₖ ≈ 1.07×10⁻⁷  
- λ_eff ≈ 1.0  
- Ns ≈ 0.25  
- Nw ≈ 0.084  
- Ts ≈ 0.25  
- Tw ≈ 0.084  

 Flujo estable, con algo de cola.

---

###  3. Alta carga (λ = 2, ρ = 0.4)
- P₀ ≈ 0.600  
- Pₖ ≈ 1.58×10⁻⁴  
- λ_eff ≈ 2.0  
- Ns ≈ 0.67  
- Nw ≈ 0.27  
- Ts ≈ 0.33  
- Tw ≈ 0.13  

 El sistema empieza a congestionarse, aunque aún dentro de capacidad.

---
