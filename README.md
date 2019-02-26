# <center> Comparação de Benchmark</center>
# <center> N-Body gravitacional em Python x Python NumPy x </center>
# <center> Python Numba CPU x Python Numba CPU // x Python Numba GPU 64 bits </center>
## <center> 22/11/2018 a 22/02/2019 </center>
## <center> $M = 1$ passo, $dt = 0.01$, $N = 32^3 = 32K$ corpos em cubo homogêneo</center>

| Tool \ Computer time    | Dell G3 | Google Colab | Lenovo Ideapad 320  | Gemini | RPi Zero | RPi 3B+ |
| --------------------------- | ---------------- | --------- | -------------------- | ------------ | ------------------- | ---------- 
| C                              |                 |    |            |                        |                |                       |                                   
| C OpenMP //               | |   |   |       |   |      | |        |
| Python                 |        |    1124.351219 s |   901.008028 s | |       |      |              
| Python NumPy                |  |     52.851517 s | 47.639086 s |    |           |       |
| Python Numba              |  |  10.242123 s |6.554241 s |  |       |            |
| Python NumPy Numba         |  |  39.379604 s | 24.690848 s|  |                 |     |
| Python Numba //        |    |   9.477498 s | 3.121972 s |       |                    ||
| Python NumPy Numba //     |   |  25.358395 s | 22.016941 s |     |   |        |
| CUDA SP                |    |  |     -   |   -    |     -   | -   |     
| CUDA kernel SP         |   |  |     -   |   -    |     -   |    -   |
| CUDA DP                |    |  |     -   |   -    |     -   |     -   |  
| CUDA kernel DP         |    |  |     -   |   -    |     -   |        -   |
| PyCUDA SP              |    |    |     -   |   -    |     -   |      -   |
| PyCUDA kernel SP       |    |  |     -   |   -    |     -   |      -   |
| PyCUDA DP              |    ||     -   |   -    |     -   |     -   |    
| PyCUDA kernel DP         |  | |     -   |   -    |     -   |     -   |
| Numba GPU vectorize SP |    | |     -   |   -    |          -   | -   |
| Numba GPU SP           |     |  |     -   |   -    |          -   | -   |
| Numba GPU kernel SP    |    |  |     -   |   -    |          -   | -   |
| Numba GPU vectorize DP |     |   |     -   |   -    |         -   | -   |
| Numba GPU DP           |   |  |       -   |   -    |     -   |     -   |     
| Numba GPU kernel DP  |      | 0.635123 s |     -   |   -    |     -   |   -   |
