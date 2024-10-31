# Criando um Script de Compactação de Arquivos

Neste guia, você aprenderá a criar um script simples para compactar arquivos no Linux.

## Passo a Passo

1. **Criar os diretórios `compactador` e `arquivos`:**
   - `mkdir -p compactador arquivos`

2. **Criar arquivos de exemplo (`arq1`, `arq2`, `arq3`) dentro do diretório `arquivos`:**
   - `touch arquivos/arq1 arquivos/arq2 arquivos/arq3`

3. **Ir para o diretório `compactador`:**
   - `cd compactador`

4. **Abrir o editor de texto (nano) dentro do diretório `compactador`:**
   - `nano compactador.sh`

5. **Adicionar o interpretador ao script:**
   - `#!/bin/bash`

6. **Criar uma condição para o número de parâmetros:**
   - ```bash
     if [ "$#" -lt 2 ]; then
         echo "O script $0 precisa de um nome, e dos arquivos para compactar!"
         exit 1
     fi
     ```

8. **Criar uma variável para o nome do arquivo de saída:**
   - `nome="$1"`

9. **Criar uma variável array para os arquivos a serem compactados:**
   - `arquivos=("${@:2}")`

10. **Compactar os arquivos usando as variáveis:**
    - `tar -czf "$nome" "${arquivos[@]}"`

11. **Informar que a compactação foi realizada com sucesso:**
    - `echo "Os arquivos foram compactados em $nome com sucesso!"`

12. **Salvar o arquivo como `compactador.sh`:**
    - Pressione `Ctrl + O`, depois `Enter`.

13. **Sair do editor:**
    - Pressione `Ctrl + X`.

14. **Tornar o script executável:**
    - `chmod +x compactador.sh`

15. **Executar o script passando o nome do arquivo de saída e os arquivos:**
    - `./compactador.sh arquivos.tar.gz arquivos/arq1 arquivos/arq2 arquivos/arq3`

16. **Verificar os arquivos dentro do arquivo compactado:**
    - `tar -tf arquivos.tar.gz`

---

## Conclusão

Agora você tem um script simples que compacta arquivos de forma automatizada! Se precisar de mais alguma ajuda, é só avisar!
