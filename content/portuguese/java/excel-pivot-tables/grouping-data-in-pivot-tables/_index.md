---
title: Agrupando dados em tabelas dinâmicas
linktitle: Agrupando dados em tabelas dinâmicas
second_title: API de processamento Aspose.Cells Java Excel
description: Aprenda como criar tabelas dinâmicas no Excel usando Aspose.Cells for Java. Automatize o agrupamento e a análise de dados com exemplos de código-fonte.
type: docs
weight: 14
url: /pt/java/excel-pivot-tables/grouping-data-in-pivot-tables/
---

As tabelas dinâmicas são uma ferramenta poderosa para analisar e resumir dados em planilhas. Eles permitem agrupar e categorizar dados para obter insights valiosos. Neste artigo, exploraremos como agrupar dados de maneira eficaz em tabelas dinâmicas usando Aspose.Cells for Java, junto com exemplos de código-fonte.

## Introdução

As tabelas dinâmicas fornecem uma maneira flexível de organizar e resumir dados de grandes conjuntos de dados. Eles permitem que você crie visualizações personalizadas de seus dados agrupando-os em categorias ou hierarquias. Isso pode ajudá-lo a identificar tendências, padrões e valores discrepantes em seus dados com mais facilidade.

## Etapa 1: crie uma tabela dinâmica

Vamos começar criando uma tabela dinâmica usando Aspose.Cells for Java. Abaixo está um exemplo de como criar uma tabela dinâmica a partir de um arquivo Excel de amostra.

```java
// Carregue o arquivo Excel
Workbook workbook = new Workbook("sample.xlsx");

// Acesse a planilha contendo os dados
Worksheet worksheet = workbook.getWorksheets().get(0);

// Especifique o intervalo de dados
CellArea sourceData = new CellArea();
sourceData.startRow = 0;
sourceData.endRow = 19; // Supondo 20 linhas de dados
sourceData.startColumn = 0;
sourceData.endColumn = 3; // Supondo 4 colunas de dados

// Crie uma tabela dinâmica com base no intervalo de dados
int index = worksheet.getPivotTables().add(sourceData, "A1", "PivotTable1");

// Obtenha a tabela dinâmica por índice
PivotTable pivotTable = worksheet.getPivotTables().get(index);

// Adicione campos a linhas e colunas
pivotTable.addFieldToArea("Product", PivotFieldType.ROW);
pivotTable.addFieldToArea("Region", PivotFieldType.COLUMN);

// Adicione valores e aplique agregação
pivotTable.addFieldToArea("Sales", PivotFieldType.DATA);
pivotTable.getDataFields().get(0).setFunction(PivotFieldFunction.SUM);

// Salve o arquivo Excel modificado
workbook.save("output.xlsx");
```

## Etapa 2: dados do grupo

 No Aspose.Cells for Java, você pode agrupar dados na tabela dinâmica usando o`PivotField` aula. Aqui está um exemplo de como agrupar um campo na tabela dinâmica:

```java
// Acesse o campo “Produto” na tabela dinâmica
PivotField productField = pivotTable.getPivotFields().get("Product");

//Agrupe o campo “Produto” por um critério específico, por exemplo, por letra inicial
productField.setIsAutoSubtotals(false);
productField.setBaseField("Product");
productField.setAutoSort(true);
productField.setAutoShow(true);

// Salve o arquivo Excel modificado com dados agrupados
workbook.save("output_grouped.xlsx");
```

## Etapa 3: personalizar o agrupamento

Você pode personalizar ainda mais as configurações de agrupamento, como especificar intervalos de agrupamento baseados em datas ou regras de agrupamento personalizadas. Aqui está um exemplo de personalização do agrupamento baseado em data:

```java
// Acesse o campo “Data” na tabela dinâmica (supondo que seja um campo de data)
PivotField dateField = pivotTable.getPivotFields().get("Date");

// Datas do grupo por meses
dateField.setIsAutoSubtotals(false);
dateField.setIsDateGroup(true);
dateField.setDateGroupingType(PivotFieldDateGroupingType.MONTHS);

// Salve o arquivo Excel modificado com agrupamento de data personalizado
workbook.save("output_custom_grouping.xlsx");
```

## Conclusão

Agrupar dados em tabelas dinâmicas é uma técnica valiosa para analisar e resumir dados no Excel, e o Aspose.Cells for Java facilita a automatização desse processo. Com os exemplos de código-fonte fornecidos, você pode criar tabelas dinâmicas, personalizar agrupamentos e obter insights de seus dados com eficiência.

## Perguntas frequentes

### 1. Qual é a finalidade das tabelas dinâmicas no Excel?

As tabelas dinâmicas no Excel são usadas para resumir e analisar grandes conjuntos de dados. Eles permitem que você crie visualizações personalizadas de seus dados, facilitando a identificação de padrões e tendências.

### 2. Como posso personalizar o agrupamento de dados em uma tabela dinâmica?

 Você pode personalizar o agrupamento de dados em uma tabela dinâmica usando o`PivotField` classe em Aspose.Cells para Java. Isso permite especificar critérios de agrupamento, como intervalos baseados em datas ou regras personalizadas.

### 3. Posso automatizar a criação de tabelas dinâmicas usando Aspose.Cells for Java?

Sim, você pode automatizar a criação de tabelas dinâmicas no Excel usando Aspose.Cells for Java, conforme demonstrado nos exemplos de código-fonte fornecidos.