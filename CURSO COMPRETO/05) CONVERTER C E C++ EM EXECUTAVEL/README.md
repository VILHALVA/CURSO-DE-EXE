# CONVERTER C E C++ EM EXECUTAVEL
Para converter código fonte em C ou C++ em um executável, você normalmente usaria um compilador adequado para a sua linguagem. Aqui estão algumas orientações básicas para compilar C e C++ em executáveis:

## **Compilação de C:**
Supondo que você tenha um arquivo de código fonte em C chamado `seu_programa.c`, você pode usar o compilador GCC (GNU Compiler Collection) para criar um executável. Abra um terminal ou prompt de comando e siga estes passos:

1. **Instale o GCC:**
   - Em sistemas Linux, geralmente o GCC já está instalado. Se não estiver, você pode instalá-lo usando o gerenciador de pacotes da sua distribuição (por exemplo, `sudo apt-get install build-essential` no Ubuntu).
   - Em sistemas Windows, você pode instalar o MinGW (Minimalist GNU for Windows) que inclui o GCC.

2. **Navegue até o Diretório do Seu Código:**
   ```bash
   cd caminho/do/seu/projeto
   ```

3. **Compile o Código:**
   ```bash
   gcc -o seu_programa seu_programa.c
   ```
   - Este comando compila o arquivo `seu_programa.c` e gera um executável chamado `seu_programa`.

4. **Execute o Executável:**
   ```bash
   ./seu_programa
   ```
   - Isso executará o seu programa compilado.

## **Compilação de C++:**
O processo é semelhante ao C, mas você usará `g++` para compilar código C++. Supondo que você tenha um arquivo de código fonte em C++ chamado `seu_programa.cpp`:

1. **Instale o G++:**
   - Se você já instalou o GCC, geralmente o G++ também é instalado. Caso contrário, você pode instalar o G++ da mesma maneira que o GCC.

2. **Navegue até o Diretório do Seu Código:**
   ```bash
   cd caminho/do/seu/projeto
   ```

3. **Compile o Código C++:**
   ```bash
   g++ -o seu_programa seu_programa.cpp
   ```
   - Este comando compila o arquivo `seu_programa.cpp` e gera um executável chamado `seu_programa`.

4. **Execute o Executável:**
   ```bash
   ./seu_programa
   ```
   - Isso executará o seu programa compilado.

Lembre-se de que esses são passos básicos e os comandos podem variar dependendo do seu ambiente e sistema operacional. Para compilação mais avançada, você pode precisar ajustar as opções do compilador e, se estiver usando bibliotecas externas, também pode precisar configurar a linkagem adequadamente. Consulte a documentação do GCC e G++ para obter mais informações.