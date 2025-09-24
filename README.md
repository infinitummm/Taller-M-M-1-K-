#  Modelo M/M/1/K (∞ población)

## Parámetros
- **λ** = tasa de llegada  
- **μ** = tasa de servicio  
- **K** = capacidad máxima del sistema (cola + servicio)  
- **ρ = λ/μ** (factor de utilización)  

---

##  Fórmulas principales

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

##  Simulación de Escenarios

Se toma **K = 10** y **μ = 5** (5 clientes/tiempo).  
Se varía **λ** para analizar tres escenarios:

---

### 🔹 1. Baja carga (λ = 1, ρ = 0.2)
- P₀ ≈ 0.834  
- Pₖ ≈ 1.07×10⁻⁷  
- λ_eff ≈ 1.0  
- Ns ≈ 0.25  
- Nw ≈ 0.084  
- Ts ≈ 0.25  
- Tw ≈ 0.084  

 Sistema casi vacío, esperas mínimas.

---

### 🔹 2. Carga media (λ = 3, ρ = 0.6)
- P₀ ≈ 0.252  
- Pₖ ≈ 0.006  
- λ_eff ≈ 2.982  
- Ns ≈ 1.49  
- Nw ≈ 0.74  
- Ts ≈ 0.50  
- Tw ≈ 0.25  

 Flujo estable, con algo de cola.

---

### 🔹 3. Alta carga (λ = 4.9, ρ = 0.98)
- P₀ ≈ 0.020  
- Pₖ ≈ 0.163  
- λ_eff ≈ 4.1  
- Ns ≈ 8.22  
- Nw ≈ 7.20  
- Ts ≈ 2.0  
- Tw ≈ 1.76  

 Sistema congestionado, largas esperas y pérdidas notables.

---

	​

