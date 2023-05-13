# Escrevendo percorrendo células

- Editando o nome da folha de uma planilha

```python
import openpyexcel

wb = openpyexcel.load_workbook('example.xlsx')
sheet = wb.get_active_sheet()
sheet.title = 'Spam Spam Spam'
wb.save('example_copy.xlsx')
```

- Criando e removendo planilhas

```python
import openpyexcel

wb = openpyexcel.Workbook()
print(wb.get_sheet_names())

wb.create_sheet()
print(wb.get_sheet_names())

wb.create_sheet(index=0, title='First Sheet')
print(wb.get_sheet_names())

wb.create_sheet(index=2, title='Middle Sheet')
print(wb.get_sheet_names())

wb.remove_sheet(wb.get_sheet_by_name('Middle Sheet'))
wb.remove_sheet(wb.get_sheet_by_name('Sheet1'))
print(wb.get_sheet_names())
```

- Escrevendo valores em células

```python
import openpyexcel

wb = openpyexcel.Workbook()
sheet = wb.get_sheet_by_name("Sheet")
sheet['A1'] = 'Hello World!'
print(sheet['A1'].value)
```

- Percorrendo uma planilha e fazendo o match para edição dos valores

```python
import openpyexcel

wb = openpyexcel.load_workbook('produceSales.xlsx')
sheet = wb.get_sheet_by_name('Sheet')

# Os tipos de produto e seus preços atualizados
PRICE_UPDATES = {'Garlic': 3.07, 'Celery': 1.19, 'Lemon': 1.27}

# Percore as linhas em um loop e atualiza os preços
for rowNum in range(2, sheet.max_row): # pula a primeira linha
    produceName = sheet.cell(row=rowNum, column=1).value
    if produceName in PRICE_UPDATES:
        sheet.cell(row=rowNum, column=2).value = PRICE_UPDATES[produceName]

wb.save('updateProduceSales.xlsx')
```