# Dates

### Sumário:

- [Dates](#dates-1)
- [Date Output](#date-output)
- [Criando Objects Date](#criando-objects-date)
- [O Método strftime()](#o-método-strftime)

---

## Dates

Uma **Date** em Python não é um _tipo de dados_ próprio, mas é possível **importar** um _Module_ nomeado ``datetime`` para trabalhar com **Dates** como _objects de **Date**_.

```
# Importando o 'Module' 'datetime' e exibindo a data atual

import datetime

x = datetime.datetime.now()
print(x)

# Exemplo de saída: 2023-09-21 16:10:12.983717
```

## Date Output

A **Date** contém _ano_, _mês_, _dia_, _hora_, _minuto_, _segundo_ e _microsegundo_.

O _Module_ ``datetime`` possui vários **métodos** para _retornar informações_ sobre o _Object **Date**_.

```
# Retornando o ano e o nome do dia da semana atual

import datetime

x = datetime.datetime.now()

print(x.year)            # Retorna: 2023
print(x.strftime("%A"))  # Retorna: Thursday
```

## Criando Objects Date

Para criar uma **Date**, pode-se utilizar a _class_ ``datetime()`` (**construtor**) do _Module_ ``datetime``.

- A _class_ ``datetime()`` requer **três parâmetros** para criar uma **Date**: _ano_, _mês_, _dia_:
    ```
    # Criando um object de 'Date'

    import datetime

    x = datetime.datetime(2020, 5, 17)

    print(x)  # Retorna: 2020-05-17 00:00:00
    ```

A _class_ ``datetime()`` também usa **parâmetros** de _hora_ e _fuso horário_ (_hora_, _minuto_, _segundo_, _microssegundo_, _tzone_), mas eles são opcionais e têm um **valor padrão** de ``0``, (``None`` para _fuso horário_).

## O Método ``strftime()``

O _object_ ``datetime`` possui um **método** para _formatar objects_ de **Date** em **strings** legíveis.

- O **método** é chamado ``strftime()`` e usa um **parâmetro** ``format``, para _especificar o formato da **string** retornada_:
    ```
    # Exibindo o nome do mês

    import datetime

    x = datetime.datetime(2018, 6, 1)
    print(x.strftime("%B"))  # Retorna: June
    ```

Uma "referência" de todos os códigos de formato legal:

- ``%a``: Dia da semana, versão curta. - ``Wed``.
- ``&A``: Dia da semana, versão completa. - ``Wednesday``.
- ``%w``: Dia da semana como um número de 0 a 6, 0 é Domingo. - ``3``.
- ``%d``: Dia do mês 01 a 31. - ``31``.
- ``%b``: Nome do mês, versão curta. - ``Dec``.
- ``%B``: Nome do mês, versão completa. - ``December``.
- ``%m``: Mês como um número 01-12. - ``12``.
- ``%y``: Ano, versão curta, sem século. - ``18``.
- ``%Y``: Ano, versão completa. - ``2018``.
- ``%H``: Hora 00-23. - ``17``.
- ``%I``: Hora 00-12. - ``05``.
- ``%p``: AM (Manhã)/PM (Tarde). - ``PM``.
- ``%M``: Minuto 00-59. - ``41``.
- ``%S``: Segundo 00-59. - ``08``.
- ``%f``: Microssegundo 000000-999999. - ``548513``.
- ``%z``: Deslocamento UTC. - ``+0100``.
- ``%Z``: Fuso horário. - ``CST``.
- ``%j``: Número do dia do ano 001-366. - ``365``.
- ``%U``: Número da semana do ano, Domingo como o primeiro dia da semana, 00-53. - ``52``.
- ``%W``: Número da semana do ano, Segunda-Feira como primeiro dia da semana, 00-53. - ``52``.
- ``%c``: Versão local de data e hora. - ``Mon Dec 31 17:41:00 2018``.
- ``%C``: Século. - ``20``.
- ``%x``: Versão local da data. - ``12/31/18``.
- ``%X``: Versão local da hora. - ``17:41:00``.
- ``%%``: Um caractere %. - ``%``.
- ``%G``: Ano ISO 8601. - ``2018``.
- ``%u``: Dia da semana ISO 8601 (1-7). - ``1``.
- ``%V``: Número da semana ISO 8601 (01-53). - ``01``.

---