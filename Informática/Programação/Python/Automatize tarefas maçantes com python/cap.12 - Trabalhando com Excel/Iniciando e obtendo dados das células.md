Resumo

- Carregando o documento e escolhendo a folha de trabalho

```python
import openpyxl

wb = openpyxl.load_workbook('example.xlsx')
sheet = wb.get_sheet_by_name('Sheet3')
```

- Determinado o tamanho da panilha

```python
sheet = wb.get_sheet_by_name('Sheet1')
print(sheet.max_row)
print(sheet.max_column)
```

- Fazer a conversão entre letras e números das colunas

Existem alguns casos que iremos preferir trabalhar com números invés de letras ou vice-versa.

```python
import openpyxl
from openpyxl.utils import get_column_letter, column_index_from_string

print(get_column_letter(27)) # Converte para letra
print(get_column_letter(900)) # Converte para letra

print(get_column_letter(sheet.max_column)) # Converte o valor d coluna máxima para letra

print(column_index_from_string('A')) # Converte a letra para número
```

- Obtendo linhas e colunas das panilhas

```python
import openpyxl

wb = openpyxl.load_workbook('example.xlsx')
sheet = wb.get_sheet_by_name('Sheet1')

print(tuple(sheet['A1':'C3']))

for rowOfCellObject in sheet['A1':'C3']:
    for cellObj in rowOfCellObject:
        print(cellObj.coordinate, cellObj.value)
    print('--- END OF ROW ---')
```