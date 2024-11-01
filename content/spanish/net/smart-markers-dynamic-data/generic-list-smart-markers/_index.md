---
title: Usar lista genérica en marcadores inteligentes Aspose.Cells
linktitle: Usar lista genérica en marcadores inteligentes Aspose.Cells
second_title: API de procesamiento de Excel Aspose.Cells .NET
description: Domine Aspose.Cells para .NET con listas genéricas y marcadores inteligentes para crear sin esfuerzo informes dinámicos de Excel. Guía sencilla para desarrolladores.
type: docs
weight: 20
url: /es/net/smart-markers-dynamic-data/generic-list-smart-markers/
---
## Introducción
La creación de informes dinámicos y aplicaciones basadas en datos es una habilidad esencial en el panorama tecnológico actual. Si trabaja con archivos .NET y Excel, probablemente haya oído hablar de Aspose.Cells, una potente biblioteca diseñada específicamente para manipular hojas de cálculo de Excel mediante programación. Esta guía completa le mostrará cómo utilizar listas genéricas con marcadores inteligentes en Aspose.Cells y le proporcionará un enfoque paso a paso para optimizar el manejo de datos en sus aplicaciones.
## Prerrequisitos
Antes de sumergirnos en el código, repasemos rápidamente lo que necesitarás:
### Conocimientos básicos de C#
Debes tener conocimientos básicos de C# y de cómo trabajar con clases y objetos. Si tienes experiencia con la programación orientada a objetos, ya estás en el camino correcto.
### Aspose.Cells para .NET instalado
 Asegúrese de tener Aspose.Cells instalado en su proyecto .NET. Puede descargar la biblioteca desde[Sitio web de Aspose](https://releases.aspose.com/cells/net/). 
### Entorno de Visual Studio
Es fundamental tener Visual Studio instalado en su equipo. Es el entorno de desarrollo más común en el que escribirá su código C#.
### Un archivo de plantilla
Para este tutorial, utilizaremos una plantilla de Excel sencilla que puedes configurar con antelación. Solo necesitarás un libro de trabajo en blanco para la demostración.
## Importar paquetes
Ahora que tenemos lo esencial en su lugar, comencemos por importar los paquetes necesarios. Una buena regla general es incluir el siguiente espacio de nombres:
```csharp
using System.IO;
using Aspose.Cells;
using System;
using System.Drawing;
using System.Collections.Generic;
```
Estos espacios de nombres proporcionarán las funcionalidades necesarias para trabajar con archivos de Excel y aplicar estilos a celdas.
## Paso 1: Define tus clases
¡Lo primero es lo primero! Necesitamos definir nuestra`Person` y`Teacher` Clases. Aquí te explicamos cómo:
### Definir la clase Persona
 El`Person` La clase contendrá atributos básicos como nombre y edad.
```csharp
public class Person
{
    int _age;
    string _name;
    
    public int Age
    {
        get { return _age; }
        set { _age = value; }
    }
    
    public string Name
    {
        get { return _name; }
        set { _name = value; }
    }
    
    public Person(string name, int age)
    {
        _age = age;
        _name = name;
    }
}
```
### Definir la clase del profesor
 El siguiente es el`Teacher` clase, que hereda de la`Person` Clase. Esta clase encapsulará además una lista de estudiantes.
```csharp
public class Teacher : Person
{
    private IList<Person> m_students;
    public IList<Person> Students
    {
        get { return m_students; }
        set { m_students = value; }
    }
    
    public Teacher(string name, int age) : base(name, age)
    {
        m_students = new List<Person>();
    }
}
```
## Paso 2: Inicializar el libro de trabajo y crear un diseñador
Ahora que tenemos nuestras clases en su lugar, es hora de inicializar nuestro libro de trabajo:
```csharp
string dataDir = "Your Document Directory"; // Especifique el directorio de su documento
Workbook workbook = new Workbook(); // Nueva instancia de libro de trabajo
Worksheet worksheet = workbook.Worksheets[0];
```
## Paso 3: Configurar marcadores inteligentes en la hoja de trabajo
Vamos a configurar marcadores inteligentes en la hoja de cálculo de Excel, indicando dónde se colocarán nuestros valores dinámicos.
```csharp
worksheet.Cells["A1"].PutValue("Teacher Name");
worksheet.Cells["A2"].PutValue("&=Teacher.Name");
worksheet.Cells["B1"].PutValue("Teacher Age");
worksheet.Cells["B2"].PutValue("&=Teacher.Age");
worksheet.Cells["C1"].PutValue("Student Name");
worksheet.Cells["C2"].PutValue("&=Teacher.Students.Name");
worksheet.Cells["D1"].PutValue("Student Age");
worksheet.Cells["D2"].PutValue("&=Teacher.Students.Age");
```
## Paso 4: Aplicar estilo para mejorar la presentación
¡Todo buen informe debe ser visualmente atractivo! Apliquemos algo de estilo a nuestros encabezados:
```csharp
Range range = worksheet.Cells.CreateRange("A1:D1");
Style style = workbook.CreateStyle();
style.Font.IsBold = true;
style.ForegroundColor = Color.Yellow;
style.Pattern = BackgroundType.Solid;
StyleFlag flag = new StyleFlag();
flag.All = true;
range.ApplyStyle(style, flag);
```
## Paso 5: Crear las instancias de profesor y alumno
 Ahora, vamos a crear instancias de nuestro`Teacher` y`Person` clases y rellenarlas con datos:
```csharp
System.Collections.Generic.List<Teacher> list = new System.Collections.Generic.List<Teacher>();
// Crear el primer objeto docente
Teacher h1 = new Teacher("Mark John", 30);
h1.Students = new List<Person>
{
    new Person("Chen Zhao", 14),
    new Person("Jamima Winfrey", 18),
    new Person("Reham Smith", 15)
};
//Crear el segundo objeto profesor
Teacher h2 = new Teacher("Masood Shankar", 40);
h2.Students = new List<Person>
{
    new Person("Karishma Jathool", 16),
    new Person("Angela Rose", 13),
    new Person("Hina Khanna", 15)
};
// Añadir a la lista
list.Add(h1);
list.Add(h2);
```
## Paso 6: Establezca la fuente de datos para el diseñador
Ahora necesitamos vincular nuestros datos con la hoja de trabajo que hemos preparado. 
```csharp
WorkbookDesigner designer = new WorkbookDesigner();
designer.Workbook = workbook;
designer.SetDataSource("Teacher", list);
```
## Paso 7: Procesar los marcadores
El siguiente paso es procesar todos los marcadores inteligentes que colocamos anteriormente:
```csharp
designer.Process();
```
## Paso 8: Ajustar automáticamente las columnas y guardar el libro de trabajo
Para asegurarnos de que todo se vea profesional, ajustemos automáticamente las columnas y guardemos nuestro libro de trabajo:
```csharp
worksheet.AutoFitColumns();
designer.Workbook.Save(dataDir + "output.xlsx"); // Guardar en el directorio especificado
```
## Conclusión
¡Y ya está! Acaba de crear una hoja de cálculo de Excel de forma dinámica, aprovechando el poder de las listas genéricas y los marcadores inteligentes con Aspose.Cells para .NET. Esta habilidad le permitirá crear informes complejos fácilmente e incorporar funcionalidades basadas en datos en sus aplicaciones. Ya sea que esté generando informes escolares, análisis de negocios o cualquier contenido dinámico, las técnicas de esta guía lo ayudarán a optimizar significativamente su flujo de trabajo.
## Preguntas frecuentes
### ¿Qué es Aspose.Cells?
Aspose.Cells es una biblioteca .NET para crear y administrar archivos de Excel sin necesidad de tener instalado Microsoft Excel.
### ¿Puedo utilizar Aspose.Cells para otros formatos de archivo?
¡Sí! Aspose ofrece bibliotecas para PDF, Word y otros formatos, lo que lo hace versátil para la gestión de documentos.
### ¿Necesito una licencia para utilizar Aspose.Cells?
 Puedes comenzar con una prueba gratuita desde[aquí](https://releases.aspose.com/), pero se requiere una licencia paga para su uso en producción.
### ¿Qué son los marcadores inteligentes?
Los marcadores inteligentes son marcadores de posición en las plantillas de Excel que se reemplazan con datos reales cuando son procesados por Aspose.Cells.
### ¿Aspose.Cells es adecuado para grandes conjuntos de datos?
¡Por supuesto! Aspose.Cells está optimizado para el rendimiento, lo que le permite manejar grandes conjuntos de datos de manera eficiente.