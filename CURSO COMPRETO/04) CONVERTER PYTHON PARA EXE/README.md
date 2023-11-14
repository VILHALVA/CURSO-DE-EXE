# CONVERTER PYTHON PARA EXECUTAVEL
Para converter um script Python em um executável, você pode usar várias ferramentas, e uma delas é o PyInstaller. Aqui estão as etapas básicas para usar o PyInstaller para criar um executável a partir de um script Python:

## 1. Instale o PyInstaller:
Abra um terminal ou prompt de comando e execute o seguinte comando para instalar o PyInstaller usando o pip:

```bash
pip install pyinstaller
```

## 2. Navegue até o Diretório do Seu Script Python:
Use o comando `cd` para navegar até o diretório que contém seu script Python.

```bash
cd caminho/do/seu/script
```

## 3. Execute o PyInstaller:
Use o seguinte comando para gerar o executável:

```bash
pyinstaller --onefile seu_script.py
```

- `--onefile`: Gera um único arquivo executável.

Depois de executar este comando, o PyInstaller criará uma pasta chamada `dist` no mesmo diretório do seu script, e dentro dessa pasta, você encontrará o seu executável.

## Exemplo com um Script Python Simples:
Vamos supor que você tenha um script chamado `hello.py` com o seguinte conteúdo:

```python
print("Hello, World!")
input("Pressione Enter para sair...")
```

Você seguiria os passos acima:

1. Instale o PyInstaller:

```bash
pip install pyinstaller
```

2. Navegue até o diretório do script:

```bash
cd caminho/do/seu/script
```

3. Execute o PyInstaller:

```bash
pyinstaller --onefile hello.py
```

Depois de concluído, você encontrará o executável na pasta `dist` dentro do diretório do seu script.

Lembre-se de que o tamanho do executável pode ser maior do que o script Python, pois ele inclui o interpretador Python e quaisquer bibliotecas necessárias. Se desejar otimizar ainda mais o tamanho do executável, você pode explorar opções adicionais do PyInstaller, como a opção `--exclude-module` para excluir módulos não utilizados. Consulte a [documentação do PyInstaller](https://pyinstaller.readthedocs.io/en/stable/) para obter informações mais detalhadas.