# Extração, Transformação e Carga (ETL)

## Transformar Tabelas com Power Query

### Combine

#### Abas (Planilhas Excel)

1. Escolher arquivo Excel.
2. Clicar em **Transformar Dados**.
3. Selecionar as colunas `name` e `data`, remover outras colunas.
4. Expandir a coluna `data`.

## FOLDER

1. Escolher a **pasta** e clicar em **Transformar Dados**.
2. Selecionar as colunas `name` e `data`, e remover as outras colunas.
3. Adicionar uma **coluna personalizada** com o seguinte código:

```m
Excel.Workbook([Content])
```

## FIX UPDATE DATA

```m
# get name columns
Table.ColumnNames(#"ETAPA"){0}
```
