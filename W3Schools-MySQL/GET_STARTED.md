# Get Started

### Sumário:

- [Banco de dados MySQL](#banco-de-dados-mysql)
- [Instale o driver MySQL](#instale-o-driver-mysql)
- [Testar o conector MySQL](#testar-o-conector-mysql)
- [Criar conexão](#criar-conexão)

---

Python pode ser usado em "aplicativos" de **banco de dados**.

- Um dos **bancos de dados** mais populares é o ``MySQL``.

## Banco de dados MySQL

É necessário ter o ``MySQL`` _instalado no computador_.

[É possível baixar um **banco de dados** ``MySQL`` em:](https://www.mysql.com/downloads/)

## Instale o driver MySQL

- Python precisa de um **driver ``MySQL``** para "acessar" o _banco de dados ``MySQL``_.
- É possível usar o **driver** "``MySQL Connector``".
    - É recomendado usar o **``PIP``** para _instalar_ o "``MySQL Connector``".

- Baixando e instalando o **driver** ``MySQL``:
    ```
    python -m pip install mysql-connector-python
    ```

## Testar o conector MySQL

Para "testar" se a _instalação_ foi bem-sucedida e se o "``MySQL Connector`` está instalado corretamente, basta criar uma página Python com o seguinte conteúdo.

```
import mysql.connector
```

- Se o código for **executado sem erros**, o "``MySQL Connector`` está _instalado_ e pronto para ser usado.

## Criar conexão

- Criando uma "**conexão**" com o _banco de dados_.
- Utilize o _nome de usuário_ e _senha_ do seu **banco de dados** ``MySQL``:
    ```
    import mysql.connector

    mydb = mysql.connector.connect(
        host="localhost",
        user="yourusername",
        password="yourpassword"
    )

    print(mydb)
    ```

- Agora é possível _começar a consultar o banco de dados_ usando **instruções** ``MySQL``.

---