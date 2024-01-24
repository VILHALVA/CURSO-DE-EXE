# CURSO DE EXE
👨‍⚖️UM ARQUIVO EXECUTÁVEL (.EXE) É UM ARQUIVO QUE CONTÉM INSTRUÇÕES EM LINGUAGEM DE MÁQUINA (CÓDIGO BINÁRIO) QUE PODEM SER EXECUTADAS DIRETAMENTE POR UM COMPUTADOR. É COMUMENTE USADO PARA INICIAR UM PROGRAMA OU APLICATIVO PARA DESKTOP.

[![GitHub Repo stars](https://img.shields.io/badge/VILHALVA-GITHUB-03A9F4?logo=github)](https://github.com/VILHALVA) 
[![GitHub Repo stars](https://img.shields.io/badge/VEJA%20DOCUMENTAÇÃO-PYINSTALLER-03A9F4?logo=google)](https://pyinstaller.readthedocs.io/en/stable/index.html)
[![GitHub Repo stars](https://img.shields.io/badge/VEJA%20DOCUMENTAÇÃO-GCC-03A9F4?logo=google)](https://gcc.gnu.org/onlinedocs/)  <br>

# CONCEITO:
## VISÃO GERAL:
Um executável, muitas vezes referido como um "arquivo executável" ou "binário executável", é um arquivo que contém um programa pronto para ser executado ou "executado" em um computador. Este arquivo é geralmente formado por instruções de código de máquina específicas para a arquitetura do processador alvo.

Vamos desdobrar o conceito:

1. **Código Fonte:**
   - O código fonte é o programa escrito em uma linguagem de programação específica, compreensível para os programadores. Este código precisa ser traduzido para um formato executável antes de poder ser executado.

2. **Compilação/Interpretação:**
   - Dependendo da linguagem de programação, o código fonte é traduzido para código de máquina de uma das duas maneiras:
     - **Compilação:** O código fonte é transformado em código de máquina (ou um código intermediário) por um compilador antes da execução.
     - **Interpretação:** O código fonte é lido e executado linha por linha por um interpretador durante o tempo de execução.

3. **Arquivo Executável:**
   - Se o código foi compilado, o arquivo executável resultante contém as instruções de código de máquina diretamente. Se foi interpretado, o arquivo executável pode conter o código fonte ou um bytecode interpretado.

4. **Execução:**
   - O sistema operacional ou a máquina virtual lê e executa as instruções contidas no arquivo executável.

5. **Resultados:**
   - O programa realiza suas tarefas conforme definido no código fonte, interagindo com o sistema operacional, hardware e outros recursos conforme necessário.

Exemplos de arquivos executáveis incluem:
- **Windows:** `.exe`
- **Linux/Unix:** Sem extensão específica, mas muitas vezes não tem extensão.
- **Java:** `.jar` (contendo bytecode executável para a Máquina Virtual Java).

Ter um executável facilita a distribuição de software, pois os usuários finais podem executar o programa sem precisar do código fonte ou do ambiente de desenvolvimento instalado.

## O PROCESSO:
Vamos abordar alguns aspectos gerais desse processo.

1. **Escolha da Linguagem:**
   - Primeiro, escolha a linguagem de programação que melhor atende às suas necessidades e preferências. Alguns exemplos populares para desenvolvimento de aplicativos desktop incluem C++, Java, Python, C# (para aplicações .NET), entre outras.

2. **Ambiente de Desenvolvimento Integrado (IDE):**
   - Utilize uma IDE adequada para a linguagem escolhida. Exemplos incluem Visual Studio para C#, Eclipse para Java, PyCharm para Python, e Visual Studio Code que é uma opção multi-linguagem.

3. **Desenvolvimento do Código:**
   - Escreva o código do seu aplicativo na linguagem escolhida. Este código será o núcleo funcional do seu aplicativo.

4. **Compilação:**
   - Dependendo da linguagem, o processo de compilação pode variar. Algumas linguagens, como Java e C#, são executadas em máquinas virtuais e não precisam ser compiladas para código de máquina nativo. Outras, como C++ e Rust, geralmente são compiladas diretamente em código de máquina.

5. **Empacotamento e Distribuição:**
   - Após a compilação, você precisará empacotar seu aplicativo de forma adequada para distribuição. Isso pode envolver a criação de um instalador, a inclusão de recursos necessários e a garantia de que todas as dependências estejam presentes.

Vamos dar um exemplo simples em Python usando o framework PyQt para criar uma aplicação desktop.

**Código em Python (app.py):**
```python
import sys
from PyQt5.QtWidgets import QApplication, QLabel, QWidget

class MyApp(QWidget):
    def __init__(self):
        super().__init__()
        self.initUI()

    def initUI(self):
        lbl = QLabel('Hello, World!', self)
        lbl.move(50, 50)

        self.setGeometry(300, 300, 300, 200)
        self.setWindowTitle('My First App')

if __name__ == '__main__':
    app = QApplication(sys.argv)
    ex = MyApp()
    ex.show()
    sys.exit(app.exec_())
```

**Compilação (não necessária em Python):**
   - Python é uma linguagem interpretada, então não há um processo explícito de compilação. Você pode executar este código diretamente usando o interpretador Python.

**Empacotamento (usando pyinstaller como exemplo):**
```bash
pip install pyinstaller
pyinstaller --onefile app.py
```

Este exemplo usa o PyQt para criar uma interface gráfica simples. O PyInstaller é usado para empacotar o aplicativo em um único arquivo executável.

Lembre-se de que os detalhes específicos podem variar com base na linguagem escolhida e nas ferramentas utilizadas. 
