# Math

### Sumário:

- [Funções Math integradas](#funções-math-integradas)
- [O Módulo Math](#o-módulo-math)

---

Python possui um _conjunto de **funções** math integradas_, incluindo um _extenso **Module** math_, que permite realizar _tarefas math com números_.

## Funções Math integradas

As **funções** ``min()`` e ``max()`` podem ser usadas para _encontrar o valor mais **baixo** ou mais **alto**_ em um iterável.

```
x = min(5, 10, 25)
y = max(5, 10, 25)

print(x)  # Retorna: 5
print(y)  # Retorna: 25
```

A **função** ``abs()`` retorna o _valor absoluto (**positivo**) do número especificado_.

```
x = abs(-7.25)

print(x)  # Retorna: 7.25
```

A **função** ``pow(x, y)`` retorna o _valor de ``x`` **elevado à potência** de ``y``_.

```
# Retornando o valor de '4' à potência de '3' (o mesmo que 4 * 4 * 4)

x = pow(4, 3)

print(x)  # Retorna: 64
```

## O Módulo Math

Python também possui um **Module** integrado chamado ``math``, que estende a _lista de **funções** math_.

- Para utilizá-lo, deve-se _importar_ o **Module** ``math``:
    ```
    import math
    ```

Depois de _importar o **Module**_ ``math``, é possível usar os **métodos** e **constantes** do **Module**.

O **método** ``math.sqrt()``, por exemplo, retorna a _raiz quadrada_ de um número.

```
import math

x = math.sqrt(64)

print(x)  # Retorna: 8.0
```

O **método** ``math.ceil()`` _arredonda um número para cima_, para o _número inteiro mais próximo_, e o **método** ``math.floor()`` _arredonda um número para baixo_, para o _número inteiro mais próximo_, e retorna o resultado.

```
import math

x = math.ceil(1.4)
y = math.floor(1.4)

print(x)  # Retorna: 2
print(y)  # Retorna: 1
```

A **constante** ``math.pi`` retorna o _valor de PI_ (**3.14...**).

```
import math

x = math.pi

print(x)  # Retorna: 3.141592653589793
```

---