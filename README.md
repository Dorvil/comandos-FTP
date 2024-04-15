# Manual de Aprendizado - Comandos FTP

FTP (File Transfer Protocol) é um protocolo usado para transferir arquivos entre um cliente e um servidor na internet ou em qualquer outra rede TCP/IP.

## Conectar ao Servidor FTP

- **Comando**: `ftp <hostname ou ip>`
- **Descrição**: Inicia uma sessão FTP com o servidor especificado.
- **Exemplo**: `ftp example.com`

## Login

- **Comando**: Após conectar, insira o usuário (`username`) e senha (`password`).
- **Descrição**: Autentica o usuário no servidor FTP.
- **Exemplo**: username: exemplo_usuario password: exemplo_senha


## Listar Arquivos e Diretórios

- **Comando**: `ls` ou `dir`
- **Descrição**: Lista os arquivos e diretórios no diretório atual no servidor.
- **Exemplo**: `ls`

## Mudar Diretório

- **Comando**: `cd <diretório>`
- **Descrição**: Muda para o diretório especificado.
- **Exemplo**: `cd documentos`

## Baixar Arquivos

- **Comando**: `get <nome do arquivo>`
- **Descrição**: Baixa o arquivo especificado do servidor FTP para o computador local.
- **Exemplo**: `get exemplo.pdf`

## Enviar Arquivos

- **Comando**: `put <nome do arquivo>`
- **Descrição**: Envia o arquivo especificado do computador local para o servidor FTP.
- **Exemplo**: `put relatorio.pdf`

## Deletar Arquivos

- **Comando**: `delete <nome do arquivo>`
- **Descrição**: Deleta o arquivo especificado no servidor FTP.
- **Exemplo**: `delete obsoleto.pdf`

## Criar Diretório

- **Comando**: `mkdir <nome do diretório>`
- **Descrição**: Cria um novo diretório no servidor FTP.
- **Exemplo**: `mkdir novos_arquivos`

## Remover Diretório

- **Comando**: `rmdir <nome do diretório>`
- **Descrição**: Remove o diretório especificado, que deve estar vazio.
- **Exemplo**: `rmdir antigos_arquivos`

## Sair do FTP

- **Comando**: `bye` ou `quit`
- **Descrição**: Termina a sessão FTP e fecha o aplicativo.
- **Exemplo**: `bye`

## Modo Passivo

- **Comando**: `passive`
- **Descrição**: Ativa ou desativa o modo passivo, útil para resolver problemas de conexão devido a firewalls.
- **Exemplo**: `passive`

## Ajuda

- **Comando**: `help` ou `?`
- **Descrição**: Mostra uma lista de comandos disponíveis ou ajuda sobre um comando específico.
- **Exemplo**: `help` ou `? get`

## Notas Adicionais:

### Verificar o Caminho Atual

- **Comando**: `pwd`
- **Descrição**: Mostra o diretório atual (path) no servidor FTP.
- **Exemplo**: `pwd`

### Modo de Transferência de Arquivos

- **Comando**: `ascii` ou `binary`
- **Descrição**: Define o modo de transferência de arquivos. `ascii` é usado para textos e `binary` para arquivos binários (imagens, etc.).
- **Exemplo**:
  - Para transferir arquivos de texto: `ascii`
  - Para transferir arquivos binários: `binary`

### Renomear Arquivos

- **Comando**: `rename <nome atual> <novo nome>`
- **Descrição**: Renomeia um arquivo no servidor FTP.
- **Exemplo**: `rename relatorio_antigo.pdf relatorio_novo.pdf`

### Copiar Arquivos no Servidor

- **Comando**: Infelizmente, o comando FTP padrão não oferece uma funcionalidade direta para copiar arquivos. Isso geralmente requer baixar o arquivo e reenviá-lo com um novo nome.
- **Descrição Alternativa**: Use `get` para baixar e depois `put` para enviar o arquivo copiado com um novo nome.
- **Exemplo**: get original.pdf put original.pdf copia.pdf
### Visualizar Conteúdo de Arquivo

- **Comando**: `more <nome do arquivo>` ou `page <nome do arquivo>`
- **Descrição**: Mostra o conteúdo de um arquivo de texto no terminal.
- **Exemplo**: `more configuracao.txt`

### Modo Verbose

- **Comando**: `verbose`
- **Descrição**: Alterna entre mostrar ou ocultar detalhes das operações de comando (modo detalhado).
- **Exemplo**: `verbose`

### Status da Conexão

- **Comando**: `status`
- **Descrição**: Exibe o status atual da conexão FTP, incluindo o modo de transferência.
- **Exemplo**: `status`

### Lista Detalhada

- **Comando**: `ls -l` ou `dir -l`
- **Descrição**: Lista os arquivos e diretórios com detalhes completos, incluindo permissões, número de links, proprietário, grupo, tamanho e data de modificação.
- **Exemplo**: `ls -l`

### Continuar Download Interrompido

- **Comando**: `reget <nome do arquivo>`
- **Descrição**: Continua o download de um arquivo que foi interrompido anteriormente.
- **Exemplo**: `reget relatorio_parcial.pdf`

### Continuar Upload Interrompido

- **Comando**: `reput <nome do arquivo>`
- **Descrição**: Continua o upload de um arquivo que foi interrompido anteriormente.
- **Exemplo**: `reput upload_parcial.zip`
