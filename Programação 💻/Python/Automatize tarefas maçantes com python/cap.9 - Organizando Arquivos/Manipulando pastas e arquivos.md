# Módulos `shutil`, `os`

O módulo **shutil** (shell utilities, ou utilitários de shell) contém funções que permitem copiar, mover, renomear e apagar arquivos em seus programas Python. Para usar as funções de shutil, inicialmente você deverá usar `import shutil`.

- `os.chdir(diretorio)` \- vai para o diretório.

## Copiando arquivos e pastas

- `shutil.copy(origem, destino)` \- se você não incluir nome do ficheiro no destino, o arquivo será simplesmente copiado. Se você incluir o arquivo será copiado e renomeado.
- `shutil.copytree(origem, destino)` \- copia todas as pastas, subpastas, arquivos para o destino.

## Movendo e renomeando arquivos e pastas

- `shutil.move(origem, destino)` \- move pastas ou ficheiros para o destino, se já existir subscreve.
- `os.rename(nomeAtual, novoNome)` \- renomea o arquivo ou pasta.

## Apagando arquivos e pastas permanentemente

- `os.unlink(diretorio)` \- apagá o arquivo no diretório.
- `os.rmdir(diretorio)` \- apagará a pasta no diretório se estiver vázia.
- `shutil.rmtree(diretório)` \- removerá a pasta no diretorio e todos os arquivos e as pastas nele contidos.

## Apagando arquivos com segurança

```python
import send2trash

send2trash.send2trash('nome do arquivo | pasta')
```

## Percorrendo árvore de diretório

```python
import os

for folderName, subfolders, filenames in os.walk('..'):
    print('The current folder is ' + folderName)

    for subfolder in subfolders:
        print('SUBFOLDER OF ' + folderName + ': ' + subfolder)

    for filename in filenames:
        print('FILE INSIDE ' + folderName + ': '+ filename)
    
    print('')
```