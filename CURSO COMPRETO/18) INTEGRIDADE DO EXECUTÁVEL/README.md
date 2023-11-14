# INTEGRIDADE DO EXECUTÁVEL
## Conceito:
A integridade do executável refere-se à garantia de que o arquivo executável não foi corrompido, alterado ou comprometido de maneira não autorizada. Manter a integridade do executável é fundamental para garantir que o software seja executado conforme projetado e não tenha sido modificado por terceiros mal-intencionados.

## Tutorial Passo a Passo:
### Verificação de Integridade com Hashes:
Uma maneira comum de verificar a integridade de um executável é usar funções de hash, como SHA-256. Vamos ver como você pode gerar e verificar hashes em um ambiente Linux usando o terminal:

1. **Gerar Hash SHA-256:**
   - Abra o terminal e navegue até o diretório onde está localizado o seu executável.

   ```bash
   cd caminho/do/seu/executavel
   sha256sum SeuApp.exe
   ```

   O comando acima irá gerar o hash SHA-256 do executável.

2. **Verificar Hash:**
   - Guarde o hash gerado em um local seguro. Sempre que precisar verificar a integridade, compare o hash atual com o hash armazenado.

   ```bash
   sha256sum -c <<< "hash_gerado SeuApp.exe"
   ```

   Isso verificará se o hash do executável ainda corresponde ao hash armazenado.

## Considerações Importantes:
- **Assinatura Digital:**
  - Além da verificação de hash, a assinatura digital é uma camada adicional de segurança que pode ser usada para confirmar a autenticidade do executável.

- **Atualizações:**
  - Ao atualizar o executável, regenere e armazene o novo hash para futuras verificações de integridade.

- **Ambiente Controlado:**
  - Em ambientes de produção, a verificação de integridade deve ser realizada regularmente para garantir que o software não tenha sido comprometido.

- **Documentação da Ferramenta:**
  - Consulte a documentação específica da ferramenta que está utilizando para obter informações sobre como verificar a integridade do executável.

A verificação regular da integridade do executável é uma prática essencial para garantir a segurança do software, especialmente em ambientes onde a confiabilidade e a integridade são críticas.