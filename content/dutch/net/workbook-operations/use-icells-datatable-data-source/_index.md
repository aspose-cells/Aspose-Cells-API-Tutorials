---
title: Gebruik ICellsDataTableDataSource voor Workbook Designer
linktitle: Gebruik ICellsDataTableDataSource voor Workbook Designer
second_title: Aspose.Cells .NET Excel-verwerkings-API
description: Leer hoe u ICellsDataTableDataSource met Aspose.Cells voor .NET kunt gebruiken om Excel-sheets dynamisch te vullen. Perfect voor het automatiseren van klantgegevens in werkmappen.
type: docs
weight: 21
url: /nl/net/workbook-operations/use-icells-datatable-data-source/
---
## Invoering
 Geavanceerde spreadsheets maken met geautomatiseerde data-integratie kan een game-changer zijn, vooral in zakelijke applicaties. In deze tutorial duiken we in hoe je`ICellsDataTableDataSource`voor een werkboekontwerper in Aspose.Cells voor .NET. We leiden u door het bouwen van een eenvoudige, voor mensen leesbare oplossing om aangepaste gegevens dynamisch in een Excel-bestand te laden. Dus als u werkt met klantenlijsten, verkoopgegevens of iets dergelijks, dan is deze gids iets voor u!
## Vereisten
Om te beginnen, moet u ervoor zorgen dat u het volgende bij de hand hebt:
-  Aspose.Cells voor .NET-bibliotheek – U kunt het downloaden van[hier](https://releases.aspose.com/cells/net/) of ontvang een gratis proefversie.
- .NET-ontwikkelomgeving – Visual Studio is een uitstekende keuze.
- Basiskennis van C# – Kennis van klassen en gegevensverwerking helpt u de cursus te volgen.
Voordat we verdergaan, moet u ervoor zorgen dat uw ontwikkelomgeving is ingesteld met de benodigde pakketten.
## Pakketten importeren
Om Aspose.Cells effectief te gebruiken, moet u essentiële pakketten importeren. Hieronder vindt u een snelle referentie voor de vereiste naamruimten:
```csharp
using Aspose.Cells.Rendering;
using Aspose.Cells.WebExtensions;
using System;
using System.Collections;
```
## Stap 1: Definieer een klantgegevensklasse
 Om te beginnen, maak een eenvoudige`Customer` klasse. Deze klasse bevat basisgegevens van klanten, zoals`FullName` En`Address`Zie het als een manier om de 'vorm' van uw gegevens te definiëren.
```csharp
public class Customer
{
    public Customer(string aFullName, string anAddress)
    {
        FullName = aFullName;
        Address = anAddress;
    }
    public string FullName { get; set; }
    public string Address { get; set; }
}
```
## Stap 2: Stel de klantenlijstklasse in
 Definieer vervolgens een`CustomerList` klasse die zich uitstrekt`ArrayList` . Deze aangepaste lijst bevat instanties van`Customer` en geïndexeerde toegang tot elk item toestaan.
```csharp
public class CustomerList : ArrayList
{
    public new Customer this[int index]
    {
        get { return (Customer)base[index]; }
        set { base[index] = value; }
    }
}
```
In deze stap verpakken we onze gegevens in een formaat dat Aspose.Cells kan herkennen en verwerken.
## Stap 3: De klantgegevensbronklasse maken
 Hier wordt het interessant. We gaan een`CustomerDataSource` klasse implementeren`ICellsDataTable` om onze gegevens compatibel te maken met de werkmapontwerper van Aspose.Cells.
```csharp
public class CustomerDataSource : ICellsDataTable
{
    internal string[] m_Columns;
    internal ICollection m_DataSource;
    private Hashtable m_PropHash;
    private IEnumerator m_IEnumerator;
    private PropertyInfo[] m_Properties;
    public CustomerDataSource(CustomerList customers)
    {
        this.m_DataSource = customers;
        this.m_Properties = customers[0].GetType().GetProperties();
        this.m_Columns = new string[this.m_Properties.Length];
        this.m_PropHash = new Hashtable(this.m_Properties.Length);
        for (int i = 0; i < m_Properties.Length; i++)
        {
            this.m_Columns[i] = m_Properties[i].Name;
            this.m_PropHash.Add(m_Properties[i].Name, m_Properties[i]);
        }
        this.m_IEnumerator = this.m_DataSource.GetEnumerator();
    }
    public string[] Columns => this.m_Columns;
    public int Count => this.m_DataSource.Count;
    public void BeforeFirst()
    {
        this.m_IEnumerator = this.m_DataSource.GetEnumerator();
    }
    public object this[int index] => this.m_Properties[index].GetValue(this.m_IEnumerator.Current, null);
    public object this[string columnName] => ((PropertyInfo)this.m_PropHash[columnName]).GetValue(this.m_IEnumerator.Current, null);
    public bool Next()
    {
        if (this.m_IEnumerator == null)
            return false;
        return this.m_IEnumerator.MoveNext();
    }
}
```
 Deze gewoonte`CustomerDataSource` klasse maakt het mogelijk voor Aspose.Cells om elk`Customer` object als een rij in het Excel-bestand.
## Stap 4: Initialiseer de klantgegevens
Laten we nu wat klanten aan onze lijst toevoegen. Hier laden we de gegevens die in de werkmap moeten worden geschreven. Voel je vrij om meer items toe te voegen als dat nodig is.
```csharp
CustomerList customers = new CustomerList();
customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));
```
In dit voorbeeld werken we met een kleine dataset. U kunt deze lijst echter eenvoudig uitbreiden door gegevens uit een database of andere bronnen te laden.
## Stap 5: Laad de werkmap
Laten we nu een bestaande Excel-werkmap openen die de benodigde Smart Markers bevat. Deze werkmap zal dienen als onze template, en Aspose.Cells zal Smart Markers dynamisch vervangen met de klantgegevens.
```csharp
string sourceDir = "Your Document Directory";
Workbook workbook = new Workbook(sourceDir + "SmartMarker1.xlsx");
```
 Zorg ervoor dat`"SmartMarker1.xlsx"` bevat tijdelijke aanduidingen zoals`&=Customer.FullName` En`&=Customer.Address` waar gegevens moeten worden ingevuld.
## Stap 6: Stel de werkmapontwerper in
Laten we nu de werkmapontwerper configureren om onze klantgegevensbron te koppelen aan de slimme markeringen van de werkmap.
```csharp
WorkbookDesigner designer = new WorkbookDesigner(workbook);
designer.SetDataSource("Customer", new CustomerDataSource(customers));
```
 De`SetDataSource` methode bindt onze`CustomerDataSource` naar de Smart Markers in de werkmap. Elke marker is gelabeld`&=Customer` in Excel worden nu vervangen door de bijbehorende klantgegevens.
## Stap 7: Verwerk en sla de werkmap op
Tot slot gaan we de werkmap verwerken om de gegevens in te vullen en de resultaten op te slaan.
```csharp
string outputDir = "Your Document Directory";
designer.Process();
workbook.Save(outputDir + "dest.xlsx");
```
Deze code activeert de verwerking van Smart Marker, vervangt alle tijdelijke aanduidingen door gegevens en slaat het resultaat op als`dest.xlsx`.
## Conclusie
 Gefeliciteerd! U hebt succesvol geïmplementeerd`ICellsDataTableDataSource` voor een werkboekontwerper die Aspose.Cells voor .NET gebruikt. Deze aanpak is ideaal voor het automatiseren van het vullen van gegevens in spreadsheets, vooral bij het werken met dynamische gegevens zoals klantenlijsten of productinventarissen. Met deze vaardigheden bent u goed op weg om datagestuurde applicaties te bouwen die Excel-gebaseerde rapportage een fluitje van een cent maken!
## Veelgestelde vragen
###  Wat is`ICellsDataTable` in Aspose.Cells?  
Het is een interface waarmee aangepaste gegevensbronnen kunnen worden gekoppeld aan Aspose.Cells Smart Markers voor dynamische gegevensinvulling.
### Hoe kan ik gegevens in de werkmapsjabloon aanpassen?  
 Plaatsaanduidingen die slimme markeringen worden genoemd, zoals`&=Customer.FullName`, worden gebruikt. Deze markers worden tijdens de verwerking vervangen door echte gegevens.
### Is Aspose.Cells voor .NET gratis?  
 Aspose.Cells biedt een gratis proefperiode, maar voor volledige toegang is een betaalde licentie vereist. Bekijk hun[gratis proefperiode](https://releases.aspose.com/) of[kopen](https://purchase.aspose.com/buy) opties.
### Kan ik dynamisch meer klantgegevens toevoegen?  
 Absoluut! Vul gewoon de`CustomerList`met aanvullende vermeldingen voordat u het programma uitvoert.
### Waar kan ik hulp krijgen als ik ergens niet uitkom?  
 Aspose heeft een[ondersteuningsforum](https://forum.aspose.com/c/cells/9) waar gebruikers vragen kunnen stellen en hulp kunnen krijgen van de community en het Aspose-team.