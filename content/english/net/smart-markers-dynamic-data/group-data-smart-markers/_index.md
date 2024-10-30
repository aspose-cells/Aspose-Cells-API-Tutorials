---
title: Group Data with Smart Markers in Aspose.Cells .NET
linktitle: Group Data with Smart Markers in Aspose.Cells .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 15
url: /net/smart-markers-dynamic-data/group-data-smart-markers/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System.Data;

namespace Aspose.Cells.Examples.CSharp.SmartMarkers
{
    public class GroupingData
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Create a connection object, specify the provider info and set the data source.
            OleDbConnection con = new OleDbConnection("provider=microsoft.jet.oledb.4.0;data source=" + dataDir + "Northwind.mdb");

            // Open the connection object.
            con.Open();

            // Create a command object and specify the SQL query.
            OleDbCommand cmd = new OleDbCommand("Select * from [Order Details]", con);

            // Create a data adapter object.
            OleDbDataAdapter da = new OleDbDataAdapter();

            // Specify the command.
            da.SelectCommand = cmd;

            // Create a dataset object.
            DataSet ds = new DataSet();

            // Fill the dataset with the table records.
            da.Fill(ds, "Order Details");

            // Create a datatable with respect to dataset table.
            DataTable dt = ds.Tables["Order Details"];

            // Create WorkbookDesigner object.
            WorkbookDesigner wd = new WorkbookDesigner();

            // Open the template file (which contains smart markers).
            wd.Workbook = new Workbook(dataDir + "Designer.xlsx");

            // Set the datatable as the data source.
            wd.SetDataSource(dt);

            // Process the smart markers to fill the data into the worksheets.
            wd.Process(true);

            // Save the excel file.
            wd.Workbook.Save(dataDir+ "output.xlsx");
           
            
        }
    }

		class OleDbCommand
    {
        private string p;
        private OleDbConnection con;

        public OleDbCommand(string p, OleDbConnection con)
        {
            // TODO: Complete member initialization
            this.p = p;
            this.con = con;
        }
    }

    class OleDbConnection
    {
        private string p;

        public OleDbConnection(string p)
        {
            // TODO: Complete member initialization
            this.p = p;
        }

        internal void Open()
        {
            
        }
    }

    class OleDbDataAdapter
    {
        public OleDbCommand SelectCommand { get; set; }

        internal void Fill(System.Data.DataSet ds, string p)
        {
           
        }
    }
    // ExEnd:1
}
```
