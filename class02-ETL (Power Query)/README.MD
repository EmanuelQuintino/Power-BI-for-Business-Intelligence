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

## TO ORDER MONTH

```m
Table.AddColumn(Fonte, "Personalizar", each
    if [Mês] = "Jan" then 1
    else if [Mês] = "Fev" then 2
    else if [Mês] = "Mar" then 3
    else if [Mês] = "Abr" then 4
    else if [Mês] = "Mai" then 5
    else if [Mês] = "Jun" then 6
    else if [Mês] = "Jul" then 7
    else if [Mês] = "Ago" then 8
    else if [Mês] = "Set" then 9
    else if [Mês] = "Out" then 10
    else if [Mês] = "Nov" then 11
    else if [Mês] = "Dez" then 12
    else null)
```
