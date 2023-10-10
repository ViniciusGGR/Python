# Create Table

### Sumário:

- [Criando uma Tabela](#criando-uma-tabela)
- [Verifique se a Tabela existe](#verifique-se-a-tabela-existe)
- [Primary Key](#primary-key)

---

## Criando uma Tabela

Para "criar" uma **tabela** no ``MySQL``, basta utilizar a _instrução_ "``CREATE TABLE``".

- Certifique-se de _definir o **nome do banco de dados** ao criar a conexão_:
    ```
    import mysql.connector

    mydb = mysql.connector.connect(
        host="localhost",
        user="test",
        password="123456789",
        database="mydatabase"
    )

    mycursor = mydb.cursor()

    mycursor.execute("CREATE TABLE customers (name VARCHAR(255), address VARCHAR(255))")
    ```

## Verifique se a Tabela existe

É possível _verificar_ se existe uma **tabela** listando _todas as **tabelas** no banco de dados_ com a _instrução_ "``SHOW TABLES``".

```
import mysql.connector

mydb = mysql.connector.connect(
    host="localhost",
    user="test",
    password="123456789",
    database="mydatabase"
)

mycursor = mydb.cursor()

# Verificando as Tabelas do banco de dados
mycursor.execute("SHOW TABLES")

for x in mycursor:
    print(x)
```

## Primary Key

- Ao "criar" uma **Tabela**, também deve-se _criar uma **coluna com uma ``PRIMARY KEY`` exclusiva** para cada registro_.

Isso pode ser feito _definindo_ uma ``PRIMARY KEY``.

Utiliza-se a **instrução** "``INT AUTO INCREMENT PRIMARY KEY``" que irá _inserir um **número único para cada registro**. Começando em ``1`` e aumentando em ``1`` para cada registro_.

```
import mysql.connector

mydb = mysql.connector.connect(
    host="localhost",
    user="test",
    password="123456789",
    database="mydatabase"
)

mycursor = mydb.cursor()

mycursor.execute("CREATE TABLE customers (id INT AUTO_INCREMENT PRIMARY KEY, name VARCHAR(255), address VARCHAR(255))")
```

- Se a **Tabela** já _existir_, use a **palavra-chave** ``ALTER TABLE``:
    ```
    import mysql.connector

    mydb = mysql.connector.connect(
        host="localhost",
        user="test",
        password="123456789",
        database="mydatabase"
    )

    mycursor = mydb.cursor()

    # Alterando a Tabela
    mycursor.execute("ALTER TABLE customers ADD COLUMN id INT AUTO_INCREMENT PRIMARY KEY")

    ```

---