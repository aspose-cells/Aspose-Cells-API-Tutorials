---
title: Editar intervalos na planilha do Excel
linktitle: Editar intervalos na planilha do Excel
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda a editar intervalos específicos em uma planilha do Excel com Aspose.Cells for .NET. Tutorial passo a passo em C#.
type: docs
weight: 20
url: /pt/net/protect-excel-file/edit-ranges-in-excel-worksheet/
---
O Microsoft Excel é uma ferramenta poderosa para criação e gerenciamento de planilhas, oferecendo diversos recursos para controlar e proteger dados. Um desses recursos é permitir que os usuários editem intervalos específicos em uma planilha enquanto protegem outras partes. Neste tutorial, iremos guiá-lo passo a passo para implementar essa funcionalidade usando Aspose.Cells for .NET, uma biblioteca popular para trabalhar com arquivos Excel programaticamente.

Usar Aspose.Cells for .NET permitirá manipular intervalos em uma planilha do Excel com facilidade, fornecendo uma interface amigável e recursos avançados. Siga as etapas abaixo para permitir que os usuários editem intervalos específicos em uma planilha do Excel usando Aspose.Cells for .NET.
## Passo 1: Configurando o ambiente

Certifique-se de ter o Aspose.Cells for .NET instalado em seu ambiente de desenvolvimento. Baixe a biblioteca do site oficial do Aspose e verifique a documentação para obter instruções de instalação.

## Etapa 2: inicializando a pasta de trabalho e a planilha

Para começar, precisamos criar uma nova pasta de trabalho e obter a referência da planilha onde queremos permitir a alteração dos intervalos. Use o seguinte código para conseguir isso:

```csharp
// Caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Crie o diretório se ele ainda não existir.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

// Instanciar uma nova pasta de trabalho
Workbook workbook = new Workbook();

// Obtenha a primeira planilha (padrão)
Worksheet sheet = workbook.Worksheets[0];
```

 Neste trecho de código, primeiro definimos o caminho para o diretório onde o arquivo Excel será salvo. A seguir, criamos uma nova instância do`Workbook` class e obtenha a referência para a primeira planilha usando o`Worksheets` propriedade.

## Etapa 3: obtenha intervalos editáveis

Agora precisamos recuperar os intervalos nos quais queremos permitir modificações. Use o seguinte código:

```csharp
// Obtenha os intervalos modificáveis
ProtectedRangeCollection EditableRanges = Sheet.AllowEditRanges;
```

## Etapa 4: definir intervalo protegido

Antes de permitir a modificação de intervalos, precisamos definir um intervalo protegido. Veja como:

```csharp
// Defina um intervalo protegido
ProtectedRange ProtectedRange;

// Crie o intervalo
int index = ModifiableRanges.Add("r2", 1, 1, 3, 3);
rangeProtected = rangesEditable[index];
```

 Neste código, criamos uma nova instância do`ProtectedRange` classe e use o`Add` método para especificar o intervalo a ser protegido.

## Etapa 5: especifique a senha

Para aumentar a segurança, você pode especificar uma senha para o intervalo protegido. Veja como:

```csharp
// Especifique a senha
protectedBeach.Password = "YOUR_PASSWORD";
```

## Etapa 6: proteja a planilha

Agora que definimos o intervalo protegido, podemos proteger a planilha para evitar modificações não autorizadas. Use o seguinte código:

```csharp
// Proteja a planilha
leaf.Protect(ProtectionType.All);
```

## Etapa 7: salve o arquivo Excel

Por fim, salvamos o arquivo Excel com as alterações feitas. Aqui está o código necessário:

```csharp
// Salve o arquivo Excel
workbook.Save(dataDir + "protectedrange.out.xls");
```

### Exemplo de código-fonte para editar intervalos na planilha do Excel usando Aspose.Cells for .NET 
```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Crie um diretório se ainda não estiver presente.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);

// Instanciar uma nova pasta de trabalho
Workbook book = new Workbook();

// Obtenha a primeira planilha (padrão)
Worksheet sheet = book.Worksheets[0];

// Obtenha os intervalos de edição permitidos
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;

// Definir intervalo protegido
ProtectedRange proteced_range;

// Crie o intervalo
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];

// Especifique a senha
proteced_range.Password = "YOUR_PASSWORD";

// Proteja a folha
sheet.Protect(ProtectionType.All);

// Salve o arquivo Excel
book.Save(dataDir + "protectedrange.out.xls");
```

## Conclusão

Parabéns! Você aprendeu como permitir que os usuários editem intervalos específicos em uma planilha do Excel usando Aspose.Cells for .NET. Agora você pode aplicar esta técnica em seus próprios projetos e melhorar a segurança de seus arquivos Excel.


#### Perguntas frequentes

#### P: Por que devo usar Aspose.Cells for .NET para editar intervalos em uma planilha do Excel?

R: Aspose.Cells for .NET oferece uma API poderosa e fácil de usar para trabalhar com arquivos Excel. Ele fornece recursos avançados, como manipulação de intervalo, proteção de planilha, etc.

#### P: Posso definir vários intervalos editáveis em uma planilha?

 R: Sim, você pode definir vários intervalos editáveis usando o`Add` método do`ProtectedRangeCollection` coleção. Cada faixa pode ter suas próprias configurações de proteção.

####  P: É possível excluir um intervalo editável após defini-lo?

 R: Sim, você pode usar o`RemoveAt` método do`ProtectedRangeCollection` coleção para remover um intervalo editável específico especificando seu índice.

#### P: Como posso abrir o arquivo Excel protegido depois de salvá-lo?

R: Você precisará fornecer a senha especificada ao criar o intervalo protegido para abrir o arquivo Excel protegido. Certifique-se de manter a senha em um local seguro para evitar perda de acesso aos dados.