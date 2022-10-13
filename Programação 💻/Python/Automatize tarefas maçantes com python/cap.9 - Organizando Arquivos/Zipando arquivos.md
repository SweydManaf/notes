# Compactando arquivos com módulo `zipfile`

Compactar um arquivo reduz seu tamanho, o que é útil quando transferimos esse arquivo pela Internet. Como um arquivo ZIP também pode conter vários arquivos e subpastas, essa é uma maneira conveniente de empacotar diversos arquivos em um só. Esse arquivo único (archive file) pode então ser, por exemplo, anexado a um email.

## Extraindo itens de arquivos ZIP

```python
import zipfile

os.chdir('diretorio') # vai para a pasta que conrém o ficheiro zipado

exampleZip = zipfile.ZipFile('example.zip')
exampleZip.extractall()
exampleZip.close()
```

## Criando arquivos ZIP  e adicionando itens

```python
import zipfile

newZip = zipfile.ZipFile('new.zip', 'w')
newZip.write('arquivo', compress_type=zipfile.ZIP_DEFLATED)
newZip.close()
```

## Compactando uma pasta

`shutil.make_archive('pastaCompactada', 'zip', 'pasta')`