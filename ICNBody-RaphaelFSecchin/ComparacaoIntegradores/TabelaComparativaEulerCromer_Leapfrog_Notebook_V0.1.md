# Tabela comparativa dos métodos integradores 

## Comparação entre Euler-Cromer e Leapfrog

### Autor: Raphael Figueiredo Secchin
### Data: 31/07/2026

A simulação foi executada no ambiente jupyter-lab do notebook LOQ-E (informações de hardware presentes no documento "NBodyLeapfrog_Euler_v0_2") utilizando as seguintes configurações iniciais:

Condições iniciais:
Massas = 1
Velocidades iniciais = 1
Espaçamento = 10
Passos = 15
G = 1
Dt = 0.1
ThreadsPerBlock = 32
Número de Corpos = $2^{12}$ (4.096)
Epsilon = 5


## Euler-Cromer
||	 1D  	  |		2D    |    3D   |
|:-------------:|:-----------:|:---------:|:-------:|
|**Python Puro** | 18.20 s | 25.20 s | 35.00 s |
|**NumPy** | 3.29 s | 5.01 s | 7.04 s |
|**Numba CPU** | 1.59 s | 1.74 s | 2.00 s |
|**Numba CPU //** | 6.68 s | 8.24 s | 8.93 s |
|**Numba GPU** | 124 ms | 141 ms | 180 ms |

## Leapfrog
||	 1D  	  |		2D    |    3D   |
|:-------------:|:-----------:|:---------:|:-------:|
|**Python Puro** | 36.60 s | 52.30 s | 1min 15 s |
|**NumPy** | 7.43 s | 10.80 s | 14.30 s |
|**Numba CPU** | 3.29 s | 3.69 s | 4.48 s |
|**Numba CPU //** | 15.80 s | 17.30 s | 17.90 s |
|**Numba GPU** | 399 ms | 289 ms | 441 ms |