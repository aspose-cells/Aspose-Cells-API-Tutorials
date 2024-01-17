---
title: Permitir que o usuário edite intervalos na planilha do Excel
linktitle: Permitir que o usuário edite intervalos na planilha do Excel
second_title: Referência da API Aspose.Cells para .NET
description: Permita que os usuários editem intervalos específicos em uma planilha do Excel usando Aspose.Cells for .NET. Guia passo a passo com código fonte em C#.
type: docs
weight: 10
url: /pt/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
Neste guia, orientaremos você sobre como usar Aspose.Cells for .NET para permitir ao usuário editar intervalos específicos em uma planilha do Excel. Siga as etapas abaixo para realizar esta tarefa.

## Passo 1: Configurando o ambiente

Certifique-se de ter configurado seu ambiente de desenvolvimento e instalado o Aspose.Cells for .NET. Você pode baixar a versão mais recente da biblioteca no site oficial do Aspose.

## Etapa 2: importar namespaces necessários

No seu projeto C#, importe os namespaces necessários para trabalhar com Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Etapa 3: definir o caminho para o diretório de documentos

 Declarar um`dataDir` variável para especificar o caminho para o diretório onde deseja salvar o arquivo Excel gerado:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Certifique-se de substituir`"YOUR_DOCUMENT_DIRECTORY"` com o caminho correto em seu sistema.

## Etapa 4: Criando um objeto de pasta de trabalho

Instancie um novo objeto Workbook que represente a pasta de trabalho do Excel que você deseja criar:

```csharp
Workbook book = new Workbook();
```

## Passo 5: Acesso à primeira planilha

Navegue até a primeira planilha da pasta de trabalho do Excel usando o seguinte código:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Etapa 6: recuperar intervalos de modificação autorizados

 Obtenha a coleção de intervalos de edição permitidos usando o`AllowEditRanges` propriedade:

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## Etapa 7: definir um intervalo protegido

 Defina um intervalo protegido usando o`Add` método do`AllowEditRanges` coleção:

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

Aqui criamos um intervalo protegido “r2” que vai da célula A1 à célula C3.

## Etapa 8: Especificando a senha

 Especifique uma senha para o intervalo protegido usando o`Password` propriedade:

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

 Certifique-se de substituir`"YOUR_PASSWORD"` com a senha desejada.

## Passo 9: Protegendo a planilha

 Proteja a planilha usando o`Protect` método do`Worksheet` objeto:

```csharp
sheet.Protect(ProtectionType.All);
```

Isso protegerá a planilha, evitando qualquer modificação fora dos intervalos permitidos.

## Passo 10: Registrando o

  Arquivo Excel

 Salve o arquivo Excel gerado usando o`Save` método do`Workbook` objeto:

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

Certifique-se de especificar o nome do arquivo desejado e o caminho correto.

### Exemplo de código-fonte para permitir que o usuário edite intervalos na planilha do Excel usando Aspose.Cells for .NET 
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
proteced_range.Password = "123";
// Proteja a folha
sheet.Protect(ProtectionType.All);
// Salve o arquivo Excel
book.Save(dataDir + "protectedrange.out.xls");
```

## Conclusão

Agora você aprendeu como usar Aspose.Cells for .NET para permitir ao usuário editar intervalos específicos em uma planilha do Excel. Sinta-se à vontade para explorar ainda mais os recursos oferecidos pelo Aspose.Cells para atender às suas necessidades específicas.


### Perguntas frequentes

#### 1. Como permitir ao usuário editar intervalos específicos em planilha Excel?

 Você pode usar o`ProtectedRangeCollection` classe para definir intervalos permitidos de modificação. Use o`Add` método para criar um novo intervalo protegido com as células desejadas.

#### 2. Posso definir uma senha para intervalos de modificação autorizados?

 Sim, você pode especificar uma senha usando o`Password` propriedade do`ProtectedRange` objeto. Isso restringirá o acesso apenas aos usuários com a senha.

#### 3. Como protejo a planilha depois de definidos os intervalos permitidos?

 Use o`Protect` método do`Worksheet` objeto para proteger a planilha. Isso evitará quaisquer alterações fora dos intervalos permitidos, possivelmente solicitando uma senha, caso você tenha especificado uma.