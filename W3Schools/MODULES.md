# Modules

### Sumário:

- [O que é um Módulo?](#o-que-é-um-módulo)
- [Crie um Módulo](#crie-um-módulo)
- [Use um Módulo](#use-um-módulo)
- [Variáveis no Módulo](#variáveis-no-módulo)
- [Nomeando um Módulo](#nomeando-um-módulo)
- [Renomeando um Módulo](#renomeando-um-módulo)
- [Módulos Integrados](#módulos-integrados)
- [Usando a Função dir()](#usando-a-função-dir)
- [Importar do Módulo](#importar-do-módulo)

---

## O que é um Módulo?

Considere um **Módulo** igual a uma _biblioteca de códigos_.

Um "**arquivo**" contendo um _conjunto de **funções**_ que se deseja incluir em seu _aplicativo_.

## Crie um Módulo

- Para _criar um **Módulo**_ basta _salvar o código_ desejado em um **arquivo** com a _extensão_ ``.py``:
    ```
    # Salvando o seguinte código em um arquivo chamado 'mymodule.py'

    def greeting(name):
        print("Hello, {}.".format(name))
    ```

## Use um Módulo

- Agora é possível _usar o **Módulo**_ que foi _criado_, usando a **instrução** ``import``:
    ```
    # Importando o 'módulo' chamado 'mymodule' e chamando a função 'greeting'

    import mymodule

    mymodule.greeting("Vinícius")
    ```

    > **Nota**: Ao usar uma **função de um Módulo**, use a _sintaxe_: ``module_name.function_name``.

## Variáveis no Módulo

O **Módulo** pode conter **funções**, conforme já descrito, mas também **variáveis** de _todos os tipos_ (**arrays**, **dictionaries**, **objects**, etc.).

```
# Salvando o código no arquivo 'mymodule.py'

person1 = {
    "name": "Vinícius",
    "age": 22,
    "country": "Brazil"
}
```

- _Importando o **Módulo**_ chamado ``mymodule`` e acessando o **Dictionary** ``person1``:
    ```
    import mymodule

    a = mymodule.person1["age"]
    print(a)  # Retorna: 22
    ```

## Nomeando um Módulo

É possível _nomear o arquivo do **Módulo**_ como quiser, mas ele deve ter a _extensão de arquivo_ ``.py``.

## Renomeando um Módulo

- É possível _criar um ``alias`` ao importar um **Módulo**_, usando a **palavra-chave** ``as``:
    ```
    # Criando um 'alias' para 'mymodule' chamado 'mx'

    import mymodule as mx

    a = mx.person1["age"]
    print(a)  # Retorna: 22
    ```

## Módulos Integrados

Existem _vários **Módulos** integrados_ em Python, que podem ser _importados_ sempre que quiser.

```
# Importando e usando o módulo 'platform'

import platform

x = platform.system()
print(x)  # Retorna: Windows
```

## Usando a Função ``dir()``

- Existe uma **função integrada** para _listar todos os nomes de **funções**_ (ou _nomes de variáveis_) em um **Módulo**. A **função** ``dir()``:
    ```
    # Listando todos os 'nomes definidos' pertencentes ao 'módulo platform'

    import platform

    x = dir(platform)
    print(x)
    
    # Retorna: ['DEV_NULL', '_UNIXCONFDIR', 'WIN32_CLIENT_RELEASES', 'WIN32_SERVER_RELEASES', '__builtins__', '__cached__', '__copyright__', '__doc__', '__file__', '__loader__', '__name__', '__package __', '__spec__', '__version__', '_default_architecture', '_dist_try_harder', '_follow_symlinks', '_ironpython26_sys_version_parser', '_ironpython_sys_version_parser', '_java_getprop', '_libc_search', '_linux_distribution', '_lsb_release_version', '_mac_ver_xml', '_node', '_norm_version', '_perse_release_file', '_platform', '_platform_cache', '_pypy_sys_version_parser', '_release_filename', '_release_version', '_supported_dists', '_sys_version', '_sys_version_cache', '_sys_version_parser', '_syscmd_file', '_syscmd_uname', '_syscmd_ver', '_uname_cache', '_ver_output', 'architecture', 'collections', 'dist', 'java_ver', 'libc_ver', 'linux_distribution', 'mac_ver', 'machine', 'node', 'os', 'platform', 'popen', 'processor', 'python_branch', 'python_build', 'python_compiler', 'python_implementation', 'python_revision', 'python_version', 'python_version_tuple', 're', 'release', 'subprocess', 'sys', 'system', 'system_aliases', 'uname', 'uname_result', 'version', 'warnings', 'win32_ver']
    ```

    > **Nota**: A **função** ``dir()`` pode ser usada em _todos os **Módulos**_, inclusive naqueles que você mesmo cria.

## Importar do Módulo

- É possível _importar "apenas" peças de um **Módulo**_, usando a **palavra-chave** ``from``:
    ```
    # O 'módulo' nomeado 'mymodule' possui uma função e um dictionary

    def greeting(name):
        print("Hello, {}.".format(name))

    person1 = {
        "name": "Vinícius",
        "age": 22,
        "country": "Brazil"
    }
    ```

    _Importando_ apenas o **Dictionary** ``person1`` do **Módulo**:
    
    ```
    from mymodule import person1

    print(person1["age"])  # Retorna: 22
    ```

> **Nota**: Ao _importar_ usando a **palavra-chave** ``from``, _não use o nome do **Módulo**_ ao se referir aos _elementos_ do **Módulo**. Exemplo: ``person1["age"]``, não ~~``mymodule.person1["age"]``~~.

---