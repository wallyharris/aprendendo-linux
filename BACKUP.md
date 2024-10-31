# Criando um Script de Backup de Arquivos

Neste guia, você aprenderá a criar um script simples para fazer backups de arquivos no Linux.

## Passo a Passo

1. **Criar os diretórios `backups` e `arquivos`:**
   - `mkdir -p backups arquivos`

2. **Criar arquivos de exemplo (`arq1`, `arq2`, `arq3`) dentro do diretório `arquivos`:**
   - `touch /home/usuario/arquivos/arq1 /home/usuario/arquivos/arq2 /home/usuario/arquivos/arq3`

3. **Ir para o diretório `backups`:**
   - `cd backups`

4. **Abrir o editor de texto (nano) dentro do diretório `backups`:**
   - `nano backup.sh`

5. **Adicionar o interpretador ao script:**
   - `#! /bin/bash`

6. **Criar uma variável para armazenar o caminho do diretório do backup:**
   - `caminho="/home/usuario/backups/"`

7. **Criar uma variável para o nome do arquivo de backup, incluindo a data e hora:**
   - `nome="backup_$(date +%Y%m%d_%H%M%S).tar.gz"`

8. **Criar um arquivo compactado com os parâmetros usando as variáveis:**
   - `tar -czf "$nome" "$caminho"`

9. **Informar que o backup foi realizado com sucesso:**
   - `echo "O backup foi feito em $nome com sucesso!"`

10. **Salvar o arquivo como `backup.sh`:**
    - Pressione `Ctrl + O`, depois `Enter`.

11. **Sair do editor:**
    - Pressione `Ctrl + X`.

12. **Tornar o script executável:**
    - `chmod +x backup.sh`

13. **Executar o script:**
    - `bash backup.sh`

---

## Conclusão

Agora você tem um script simples que faz backup dos arquivos de forma automatizada!
- [Script de Compactador](COMPACTADOR.md): Passo a passo para criar um script simples de compactador de arquivos no Linux.
