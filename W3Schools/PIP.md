# PIP

### Sumário:

- [O que é PIP?](#o-que-é-pip)
- [O que é um Package?](#o-que-é-um-package)
- [Verificando se o PIP está instalado](#verificando-se-o-pip-está-instalado)
- [Baixando um Package](#baixando-um-package)
- [Usando um Package](#usando-um-package)
- [Encontrar Packages](#encontrar-packages)
- [Remover um Package](#remover-um-package)
- [Listar Packages](#listar-packages)

---

## O que é PIP?

``PIP`` é um **gerenciador de pacotes** para _packages_ ou **Modules** Python.

> **Nota**: Se tiver a versão Python ``3.4`` ou _posterior_, o ``PIP`` será incluído por padrão.

## O que é um Package?

Um _package_ contém **todos os arquivos** necessários para um **Module**.

**Modules** são _bibliotecas_ de código Python que podem ser _incluídas em um projeto_.

## Verificando se o PIP está instalado

- Para _verificar a versão_ do ``PIP``, basta digitar no **terminal**:
    ```
    pip --version

    # Exemplo de saída: pip 22.3.1
    ```

## Baixando um Package

Abra a _interface de linha de comando_ (**terminal**) e "diga" ao ``PIP`` para baixar o _package_ desejado.

```
# Baixando um 'package' chamado "camelcase"

pip install camelcase
```

## Usando um Package

Depois que o _package_ estiver **instalado**, ele estará pronto para uso.

- **Importando** o _package_ "**camelcase**" para o projeto:
    ```
    import camelcase

    c = camelcase.CamelCase()

    txt = "lorem ipsum dolor sit amet"

    # Este 'método' coloca a primeira letra de cada palavra em maiúscula
    print(c.hump(txt))

    # Retorna: Lorem Ipsum Dolor Sit Amet
    ```

## Encontrar Packages

- Encontre mais _packages_ em [PyPi](https://pypi.org/)

## Remover um Package

Utilizando o **comando** ``uninstall`` para _remover um package_.

```
# Desinstalando o package "camelcase"

pip uninstall camelcase
```

- O ``PIP Package Manager`` solicitará a _confirmação_ para **remover** o _package_ ``camelcase``:
    ```
    pip uinstall camelcase

    >>> Proceed (y/n)?
    ```

    - Pressione ``y`` e o _package_ será **removido**.

## Listar Packages

Utilizando o **comando** ``list`` para _listar todos os packages **instalados no sistema**_.

```
# Listando packages instalados

pip list

"""Exemplo de saída:
    Package         Version
    -----------------------
    camelcase       0.2
    mysql-connector 2.1.6
    pip             18.1
    pymongo         3.6.1
    setuptools      39.0.1
"""
```

---