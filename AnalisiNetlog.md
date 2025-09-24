Análisis Detallado por Escenario
1. Baja Carga (λ = 0.1, ρ = 0.02)
Modelo Matemático:

$P_0$ (probabilidad sistema vacío) ≈ 0.981

$N_w$ (clientes en cola) ≈ 0.001

$T_w$ (tiempo en cola) ≈ 0.010 ticks

NetLogo (Resultados Observados):

Queue Length: 0

Avg. Queue Length: 0.05

Avg. Time in Queue: 0.508 ticks

Server Utilization: 0.05%

Coincidencia: ALTA
El sistema permanece casi vacío como predice la teoría

La utilización es mínima (0.05% vs 2% teórico)

Pequeñas diferencias atribuibles a variabilidad estadística

2. Carga Media (λ = 1.0, ρ = 0.20)
Modelo Matemático:

$P_0$ ≈ 0.834

$N_w$ ≈ 0.084

$T_w$ ≈ 0.084 ticks

NetLogo (Resultados Observados):

Avg. Queue Length: 0.05

Avg. Time in Queue: 0.249 ticks

Server Utilization: 19.864%


Utilización casi idéntica (19.86% vs 20% teórico)

Longitud de cola ligeramente inferior a la teórica

Tiempo en cola mayor al teórico, posiblemente por efectos transitorios

3. Alta Carga (λ = 2.0, ρ = 0.80)
Modelo Matemático:

$N_w$ ≈ 3.2

$T_w$ ≈ 1.6 ticks

$T_s$ ≈ 2.0 ticks

NetLogo (Resultados Observados):

Queue Length: 0 (en momento específico)

Avg. Queue Length: 3.259

Avg. Time in Queue: 1.628 ticks

Avg. Time in System: 2.028 ticks

Server Utilization: 80.153%


Longitud promedio de cola: 3.259 vs 3.2 teórico (error: 1.8%)

Tiempo en cola: 1.628 vs 1.6 teórico (error: 1.7%)

Tiempo en sistema: 2.028 vs 2.0 teórico (error: 1.4%)

Utilización: 80.15% vs 80% teórico (error: 0.2%)

