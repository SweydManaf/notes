# Manipulação de arquivos e diretórios

## Bibliotecas

- **os** \- manipula o sistema
- **os.path** \- manipula diretórios
- **shutil** \- utilidades do shell

## `import os`

Fornece uma interface multiplataforma para interagir com o sistema operacional, ou suja, permite facilitar a interação com o "shell".Se quisermos listar, criar, deletar, modificar, aquivos e diretórios, tempos várias funções internas que nos permitem fazer esse tipo de operação.

Exemplos:

- `listdir` -\> lista os arquivos em um diretório
- `rmdir` -\> Remove um diretório
- `walk` -\> Cria uma relação de todos os arquivos e diretórios presentes no diretório passado como parâmetro.

### import os.path

Este módulo implementa algumas funções úteis em nomes de caminho e utilização de paths.

Exemplos:

- `exists` -\> Retorna se o arquivo ou diretório existe.
- `abspath` -\> Retorna o caminho absoluto do arquivo.
- `join` -\> Concatena **paths** para descrever caminhos.

## `import shutil`

O módulo **shutil** oferece uma série de operações de alto nível em arquivos e coleções de arquivos. Em particular, são fornecidas funções que suportam a cópia e remoção de arquivos.

Exemplos:

- `copy` -\> Copia um arquivo
- `rmtree` -\> Remove uma árvore de diretórios
- `disk_usage` -\> Retorna a capacidade total/livre/usada em bytes do disco a qual o **path** pertence.