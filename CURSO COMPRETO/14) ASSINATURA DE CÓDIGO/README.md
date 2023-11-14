# ASSINATURA DE CÓDIGO
## Conceito:
A assinatura de código é uma prática de segurança que envolve a aplicação de uma assinatura digital a arquivos executáveis ou scripts para verificar sua autenticidade e integridade. Essa assinatura digital é gerada por meio de chaves criptográficas, permitindo que os usuários finais confirmem que o código não foi alterado desde a assinatura e que o arquivo foi realmente assinado pelo desenvolvedor.

## Tutorial Passo a Passo:
Vamos explorar a assinatura de código usando um exemplo básico no ambiente Windows e a ferramenta `signtool`, que faz parte do kit de desenvolvimento do Windows (Windows SDK).

1. **Instale o Windows SDK:**
   - Certifique-se de ter o Windows SDK instalado. Você pode obtê-lo durante a instalação do Visual Studio ou baixando-o separadamente do [site oficial da Microsoft](https://developer.microsoft.com/en-us/windows/downloads/windows-10-sdk/).

2. **Crie um Certificado de Desenvolvedor:**
   - Use a ferramenta `makecert` incluída no Windows SDK para criar um certificado de desenvolvedor.

   ```bash
   makecert -r -pe -n "CN=Seu Nome" -ss MY -sr LocalMachine -a sha256 -len 2048 -cy end
   ```

   Este comando cria um certificado autoassinado no repositório de certificados pessoais (MY) da máquina local.

3. **Exporte o Certificado:**
   - Abra o "Gerenciador de Certificados" (`certmgr.msc`), navegue até "Certificados Pessoais" > "Certificados" e localize seu certificado. Exporte-o em um arquivo `.pfx`.

4. **Importe o Certificado no Repositório de Certificados do Windows:**
   - Execute o comando `certutil` para importar o certificado.

   ```bash
   certutil -p senha -importPFX SeuCertificado.pfx
   ```

5. **Assine o Executável:**
   - Utilize o `signtool` para assinar o executável.

   ```bash
   signtool sign /f SeuCertificado.pfx /p senha /tr http://timestamp.digicert.com /td sha256 /fd sha256 SeuApp.exe
   ```

   Isso adiciona a assinatura digital ao executável usando o certificado que você criou.

## Considerações Importantes:
- **Distribuição do Certificado:**
  - Mantenha o certificado seguro e não o compartilhe publicamente. Ele é usado para provar a autenticidade do código.

- **Renovação do Certificado:**
  - Certificados de desenvolvedor geralmente têm um prazo de validade. Lembre-se de renovar ou obter um novo certificado quando necessário.

- **Timestamping:**
  - O uso de um serviço de timestamping, como o fornecido no exemplo, ajuda a garantir que a assinatura permaneça válida mesmo após a expiração do certificado.

- **Documentação da Ferramenta:**
  - Consulte a documentação específica da ferramenta e os requisitos da plataforma que você está usando para obter informações detalhadas sobre a assinatura de código.

Lembre-se de que essas etapas podem variar dependendo do ambiente de desenvolvimento e das ferramentas específicas que você está utilizando. Certifique-se de consultar a documentação relevante para obter informações específicas do sistema operacional e das ferramentas.