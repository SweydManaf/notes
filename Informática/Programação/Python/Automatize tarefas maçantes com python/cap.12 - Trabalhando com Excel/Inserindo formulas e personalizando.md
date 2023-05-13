# Personalizando e inserindo formulas

- Definindo o estilo de fonte das células

```python
import openpyexcel
from openpyexcel.styles import Font, NamedStyle

wb = openpyexcel.Workbook()
sheet = wb.get_sheet_by_name('Sheet')
italic24Font = Font(size=24, italic=True)
styleObj = NamedStyle(font=italic24Font)

sheet['A1'].style = styleObj
sheet['A1'] = 'Hello World'
wb.save('styled.xlsx')

# TODO: Encontrar o novo método para personalização
```

- Inserindo fórmulas

```python
import openpyexcel

wb = openpyexcel.Workbook()
sheet = wb.get_sheet_by_name('Sheet')

sheet['A1'] = 200
sheet['A2'] = 300
sheet['A3'] = '=SUM(A1:A2)'

wb.save('writeFormula.xlsx')
```

- Obtendo valores e formulas

```python
import openpyexcel

wbFormulas = openpyexcel.load_workbook('writeFormula.xlsx')
sheet = wbFormulas.get_active_sheet()
print(sheet['A3'].value)

wbDataOnly = openpyexcel.load_workbook('writeFormula.xlsx', data_only=True)
sheet = wbDataOnly.get_active_sheet()
print(sheet['A3'].value)
```

- Ajustando linhas e colunas

```python
import openpyexcel

wb = openpyexcel.Workbook()
sheet = wb.get_active_sheet()
sheet['A1'] = 'Tall row'
sheet['B2'] = 'Wide column'
sheet.row_dimensions[1].height = 70
sheet.column_dimensions['C'].width = 20

wb.save('dimensions.xlsx')
```

- Mesclar e separar células

```python
import openpyexcel

wb = openpyexcel.Workbook()
sheet = wb.get_active_sheet()

sheet.merge_cells('A1:D3')
sheet['A1'] = 'Twelve cells merged toguether.'

sheet.merge_cells('C5:D5')
sheet['C5'] = 'Two merged cells.'

wb.save('merged.xlsx')
```

- Separando células

```python
import openpyexcel

wb = openpyexcel.load_workbook('merged.xlsx')
sheet = wb.get_active_sheet()

sheet.unmerge_cells('A1:D3')
sheet.unmerge_cells('C5:D5')
wb.save('merged.xlsx')
```

- Painéis congelados

```python
import openpyexcel

wb = openpyexcel.load_workbook('produceSales.xlsx')

sheet = wb.get_active_sheet()
sheet.freeze_panes = 'A2'

wb.save('freezeExample.xlsx')
```