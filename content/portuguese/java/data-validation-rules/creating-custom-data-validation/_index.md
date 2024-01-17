---
title: Criando validação de dados personalizada
linktitle: Criando validação de dados personalizada
second_title: API de processamento Aspose.Cells Java Excel
description: Aprenda como criar validação de dados personalizada usando Aspose.Cells for Java. Guia passo a passo com código-fonte.
type: docs
weight: 10
url: /pt/java/data-validation-rules/creating-custom-data-validation/
---

## Introdução

validação de dados ajuda a manter a integridade dos dados, evitando que os usuários insiram dados incorretos ou inválidos em planilhas do Excel. Embora o Excel ofereça opções integradas de validação de dados, há cenários em que você precisa definir regras de validação personalizadas. Aspose.Cells for Java permite que você consiga isso de forma eficiente.

## Pré-requisitos

Antes de mergulhar no código, certifique-se de ter os seguintes pré-requisitos:

-  Aspose.Cells for Java: Baixe e instale a biblioteca em[aqui](https://releases.aspose.com/cells/java/).

## Etapa 1: configurando seu projeto Java

Para começar, crie um novo projeto Java em seu ambiente de desenvolvimento integrado (IDE) preferido. Adicione a biblioteca Aspose.Cells for Java ao classpath do seu projeto.

## Etapa 2: Criando uma pasta de trabalho do Excel

Vamos começar criando uma nova pasta de trabalho do Excel usando Aspose.Cells for Java.

```java
// Código Java para criar uma nova pasta de trabalho do Excel
Workbook workbook = new Workbook();
```

## Etapa 3: adicionar uma planilha

Agora, vamos adicionar uma planilha à pasta de trabalho onde aplicaremos nossa validação de dados personalizada.

```java
// Código Java para adicionar uma planilha
Worksheet worksheet = workbook.getWorksheets().get(0);
```

## Etapa 4: definição de critérios de validação personalizados

Nesta etapa, definiremos os critérios de validação personalizados aos quais nossos dados devem aderir. Digamos que queremos restringir a idade inserida em uma célula entre 18 e 60 anos.

```java
// Código Java para definir critérios de validação customizados
Validation validation = worksheet.getValidations().add();
validation.setType(ValidationType.WHOLE);
validation.setOperator(OperatorType.BETWEEN);
validation.setFormula1("18");
validation.setFormula2("60");
validation.setShowError(true);
validation.setAlertStyle(ValidationAlertType.STOP);
validation.setErrorTitle("Invalid Age");
validation.setErrorMessage("Age must be between 18 and 60.");
```

## Etapa 5: aplicando validação de dados a um intervalo

Agora que definimos nossos critérios de validação personalizados, vamos aplicá-los a um intervalo específico de células.

```java
// Código Java para aplicar validação de dados a um intervalo
CellArea area = new CellArea();
area.startRow = 0;
area.startColumn = 0;
area.endRow = 9; // Aplicar validação às primeiras dez linhas
area.endColumn = 0;

validation.addArea(area);
```

## Etapa 6: salvando o arquivo Excel

Por fim, salve o arquivo Excel com as regras personalizadas de validação de dados aplicadas.

```java
// Código Java para salvar o arquivo Excel
workbook.save("CustomDataValidation.xlsx");
```

## Conclusão

Neste tutorial, exploramos como criar regras de validação de dados personalizadas usando Aspose.Cells para Java. Seguindo essas etapas, você pode garantir que seus dados do Excel atendam a critérios específicos, melhorando a integridade e a precisão dos dados.

## Perguntas frequentes

### Como faço o download do Aspose.Cells para Java?

 Você pode baixar Aspose.Cells for Java do site em[aqui](https://releases.aspose.com/cells/java/).

### Posso aplicar validação de dados personalizada a vários intervalos na mesma planilha?

Sim, você pode aplicar a validação de dados personalizada a vários intervalos na mesma planilha, repetindo a Etapa 5 para cada intervalo desejado.

### Existem outros tipos de validação de dados suportados pelo Aspose.Cells for Java?

Sim, Aspose.Cells for Java oferece suporte a vários tipos de validação de dados, incluindo número inteiro, decimal, data, hora, comprimento de texto e muito mais.

### Como posso personalizar a mensagem de erro exibida quando a validação de dados falha?

 Você pode personalizar a mensagem de erro modificando o arquivo`setErrorMessage` método na Etapa 4, onde você define os critérios de validação.

### O Aspose.Cells for Java funciona com arquivos Excel em diferentes formatos?

Sim, Aspose.Cells for Java oferece suporte a uma ampla variedade de formatos de arquivo Excel, incluindo XLS, XLSX, XLSM e muito mais.