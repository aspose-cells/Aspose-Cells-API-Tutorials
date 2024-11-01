---
title: Detectando Referência Circular no Excel Programaticamente
linktitle: Detectando Referência Circular no Excel Programaticamente
second_title: API de processamento do Aspose.Cells .NET Excel
description: Detecte facilmente referências circulares no Excel usando Aspose.Cells para .NET. Siga nosso guia passo a passo para garantir cálculos precisos em suas planilhas.
type: docs
weight: 13
url: /pt/net/excel-formulas-and-calculation-options/detecting-circular-reference/
---
## Introdução
Quando se trata de trabalhar com arquivos do Excel, um dos problemas mais frustrantes que você pode encontrar é uma referência circular. Isso acontece quando uma fórmula faz referência à sua própria célula, direta ou indiretamente, criando um loop que pode confundir o mecanismo de cálculo do Excel. Mas não tenha medo! Com o Aspose.Cells para .NET, você pode detectar programaticamente essas referências circulares incômodas, garantindo que suas planilhas permaneçam funcionais e precisas. Neste guia, vamos orientá-lo no processo passo a passo, tornando-o tão simples quanto uma torta.
## Pré-requisitos
Antes de nos aprofundarmos nos detalhes da detecção de referências circulares, vamos garantir que você tenha tudo o que precisa para começar:
1. Visual Studio: Certifique-se de ter o Visual Studio instalado em sua máquina. Este será seu ambiente de desenvolvimento.
2. .NET Framework: certifique-se de estar usando uma versão compatível do .NET Framework (pelo menos .NET Framework 4.0).
3.  Biblioteca Aspose.Cells: Você precisa ter a biblioteca Aspose.Cells. Você pode baixá-la do[Site Aspose](https://releases.aspose.com/cells/net/).
4. Conhecimento básico de C#: Familiaridade com programação em C# será benéfica, pois escreveremos código nesta linguagem.
5. Arquivo Excel: Tenha um arquivo Excel pronto que contenha referências circulares para teste. Você pode criar um simples ou baixar um exemplo.
Agora que definimos nossos pré-requisitos, vamos para a parte divertida!
## Pacotes de importação
Antes de começar a codificar, você precisa importar os pacotes necessários. Veja como fazer isso:
### Criar um novo projeto
- Abra o Visual Studio e crie um novo projeto de aplicativo de console C#.
### Adicionar referência Aspose.Cells
- Clique com o botão direito do mouse no seu projeto no Solution Explorer.
- Selecione "Gerenciar pacotes NuGet".
- Procure por “Aspose.Cells” e instale a versão mais recente.
### Importar namespaces necessários
 No topo do seu`Program.cs` arquivo, importe os namespaces necessários:
```csharp
using System;
using System.Collections;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

Agora que configuramos tudo, vamos mergulhar no código para detectar referências circulares em um arquivo do Excel.
## Etapa 1: Defina o diretório de entrada
Primeiro, você precisa especificar o diretório onde seu arquivo Excel está localizado. É aqui que você carregará seu arquivo Excel.
```csharp
// Diretório de entrada
string sourceDir = "Your Document Directory";
```
 Substituir`"Your Document Directory"` com o caminho real para seu arquivo Excel.
## Etapa 2: Carregue a pasta de trabalho com LoadOptions
Em seguida, você carregará sua pasta de trabalho do Excel. É aqui que a mágica começa!
```csharp
LoadOptions loadOptions = new LoadOptions();
var objWB = new Aspose.Cells.Workbook(sourceDir + "Circular Formulas.xls", loadOptions);
```
 Aqui, estamos criando uma nova instância de`LoadOptions` e carregando a pasta de trabalho do caminho especificado. Certifique-se de que o nome do seu arquivo Excel corresponda!
## Etapa 3: Habilitar configurações de iteração
Para permitir referências circulares, você precisa habilitar as configurações de iteração na pasta de trabalho.
```csharp
objWB.Settings.Iteration = true;
```
Isso informa ao Aspose.Cells para permitir referências circulares durante o cálculo.
## Etapa 4: Criar opções de cálculo e monitor circular
Agora, vamos criar as opções de cálculo e nosso monitor circular personalizado.
```csharp
CalculationOptions copts = new CalculationOptions();
CircularMonitor cm = new CircularMonitor();
copts.CalculationMonitor = cm;
```
 Aqui, estamos criando uma instância de`CalculationOptions` e um costume`CircularMonitor`Este monitor ajudará a rastrear quaisquer referências circulares encontradas durante os cálculos.
## Etapa 5: Calcular as fórmulas
Agora, é hora de calcular as fórmulas na sua pasta de trabalho.
```csharp
objWB.CalculateFormula(copts);
```
Esta linha executa o cálculo e verifica referências circulares.
## Etapa 6: Contar referências circulares
Após o cálculo, você pode contar quantas referências circulares foram encontradas.
```csharp
long lngCircularRef = cm.circulars.Count;
Console.WriteLine("Circular References found - " + lngCircularRef);
```
Isso gerará o número de referências circulares detectadas no seu arquivo Excel.
## Etapa 7: Exibir resultados
Por fim, vamos exibir os resultados e confirmar que nosso método foi executado com sucesso.
```csharp
Console.WriteLine("DetectCircularReference executed successfully.\r\n");
```
## Etapa 8: Implementar a classe CircularMonitor
 Para concluir o processo, você precisará implementar o`CircularMonitor` classe. Esta classe herdará de`AbstractCalculationMonitor` e lidar com a detecção de referências circulares.
```csharp
public class CircularMonitor : AbstractCalculationMonitor
{
    public ArrayList circulars = new ArrayList();
    public ArrayList Circulars { get { return circulars; } }
    public override bool OnCircular(IEnumerator circularCellsData)
    {
        CalculationCell cc = null;
        ArrayList cur = new ArrayList();
        while (circularCellsData.MoveNext())
        {
            cc = (CalculationCell)circularCellsData.Current;
            cur.Add(cc.Worksheet.Name + "!" + CellsHelper.CellIndexToName(cc.CellRow, cc.CellColumn));
        }
        circulars.Add(cur);
        return true;
    }
}
```
Esta classe captura os detalhes de cada referência circular encontrada, incluindo o nome da planilha e o índice da célula.
## Conclusão
Detectar referências circulares no Excel usando o Aspose.Cells para .NET é um processo simples, uma vez que você o divide em etapas gerenciáveis. Ao seguir este guia, você pode identificar e manipular facilmente referências circulares em suas planilhas, garantindo que seus cálculos permaneçam precisos e confiáveis. Seja você um desenvolvedor experiente ou apenas começando, o Aspose.Cells fornece ferramentas poderosas para aprimorar seus recursos de manipulação do Excel. 
## Perguntas frequentes
### O que é uma referência circular no Excel?
Uma referência circular ocorre quando uma fórmula faz referência à sua própria célula, causando um loop infinito nos cálculos.
### Como posso detectar referências circulares programaticamente?
Você pode usar a biblioteca Aspose.Cells no .NET para detectar programaticamente referências circulares implementando um monitor de cálculo personalizado.
### Quais são os pré-requisitos para usar o Aspose.Cells?
Você precisa do Visual Studio, do .NET Framework e da biblioteca Aspose.Cells instalados.
### Posso usar o Aspose.Cells gratuitamente?
Sim, o Aspose.Cells oferece um teste gratuito que você pode usar para explorar seus recursos.
### Onde posso encontrar mais informações sobre o Aspose.Cells?
 Você pode visitar o[Documentação do Aspose.Cells](https://reference.aspose.com/cells/net/) para informações detalhadas e exemplos.