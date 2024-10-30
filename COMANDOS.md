## Acesso ao Servidor
- Usar o comando `ip address` para saber o IP do Linux Server
- Logar no Linux Server com: `ssh [ip]`

## Comandos Básicos
- Verificar atualizações: `sudo apt-get update`
- Mostrar diretório atual: `pwd`
- Mostrar arquivos do diretório: `ls`
- Mostrar arquivos ocultos: `ls -a`
- Criar um diretório: `mkdir diretorio-teste`
- Mudar para o diretório: `cd diretorio-teste`
- Voltar para a home: `cd`
- Ver histórico de comandos: `history`

## Manipulação de Arquivos
- Criar um arquivo: `cat > teste.txt` (sair com `Ctrl + D`)
- Mostrar conteúdo do arquivo: `cat teste.txt`
- Exibir arquivos no diretório: `ls`
- Exibir `hello world`: `echo hello world`
- Enviar `hello world` para `teste.txt`: `echo hello world > teste.txt`
- Instalar editor de texto: `sudo apt-get install nano`
- Criar e editar arquivo: `nano teste2.txt` (salvar com `Ctrl + O`, sair com `Ctrl + X`)
- Compactar arquivos: `tar -czf compactado.tar.gz teste.txt teste2.txt`
- Mover arquivo compactado: `mv compactado.tar.gz /home/wally/diretorio-teste/`
- Voltar para a pasta devops: `cd diretorio-teste`
- Mostrar arquivos: `ls`
- Voltar para a home: `cd`
- Remover arquivos: `rm teste.txt teste2.txt`

---

## Conclusão

Nesta lista de comandos básicos de Linux, apresentamos ferramentas essenciais para a manipulação de arquivos e navegação no sistema.

- [Script de Backup](BACKUP.md): Passo a passo para criar um script simples de backup de arquivos no Linux.
