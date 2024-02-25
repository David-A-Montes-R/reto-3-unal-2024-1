# Diagrama de flujo para hallar los números primos

```mermaid
flowchart TD;
    A(inicio)
    A-->|crear| C[lista N para números n]
    A-->|crear| D[lista P para números p]
    A-->|crear| E[lista NP para números np]
    A-->|crear| F[lista RN para rn]
    G[n=1]-->E
    C-->H[i=n >1]
    C-->I[calcular todas las raices cuadradas de los números n]-->|clasificar las raíces en:| F
    H-->O{¿es i < rn?}-->|sí| K
    H-->O{¿es i < rn?}-->|No|P[n=n+1] -->O
    K[dividir todos los números n tal que n/i]
    K-->M{¿El residuo de n/i es cero?}
    M-->|sí| N[Clasificar n]-->|en| E
    M-->|no| T[Clasificar n]-->|en| D
    E-->Q[i+1]
    D-->Q
    Q-->R{¿es i < n ?}-->|sí| K
     Q-->R{¿es i < n ?}-->|No| S[acabar las divisiones]
     S-->Z(finalizar el proceso)