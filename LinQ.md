# About LinQ<a id="sec-3" name="sec-3"></a>


# List

```sh
sbt clean coverage test
```

```scala
dtWhitelistData.Select().Where(Function(x) x.Item("DomainName").ToString.ToLower.Equals(emailSenderHost.ToLower)).ToArray
```

```scala
dtData.AsEnumerable.Where(Function (x) x("CCode").toString.Trim.ToUpper.Equals(strCCFilter.ToUpper)).ToList
```

```scala
(from item in arrStrSplit where Not item.Contains("Page")).ToArray
```

```scala
(from item in arrStrSplit where Not String.IsNullOrWhiteSpace(item.Trim)).ToArray
```

```scala
String.Join(" ", regexMatch.Cast(Of match).Select(function(d) d.ToString).ToArray)
```

```scala
(from item in lstNewData where item.Contains("3059 Subtotal") or item.Contains("8155 Subtotal")).ToList
```

```scala
(from item in lstNewData where item.Contains("3059 Subtotal") or item.Contains("8155 Subtotal")).ToList
```

# arr_Rows


```scala
(From row In dtOutput.Select("[ColoumName]='RowValue'")
```

```scala
Where CDate(row("Date").ToString) >= Date.Today.AddDays(-11) And CDate(row("Date").ToString) <= Date.Today.AddDays(-5)
```

```scala
Select row).ToArray
```



# str_Row


```scala
rows.Sum(Function (x) If(Double.TryParse(x.item("Actual_Amount").ToString, Nothing), Double.Parse(x.Item("Actual_Amount").ToString), 0))
```

```scala
Dt.Rows(2).itemArray
```



# groupRows


```scala
(From r In dtConfig.Select()
```

```scala
Group r By rowitem=New With { Key.ROW_NO = r.Item("ROW_NO") } Into Group
```

```scala
Select Group.ToArray).ToArray()
```

```scala
targetLine.ToLower.Contains(parserKeywords(index).ToLower)
```


# DataTable


```scala
customersDT.AsEnumerable().Where(Function (row) row("First Name").ToString().StartsWith("J")).CopyToDataTable
```


# int


```scala
customersDT.AsEnumerable().Min(Function (row) row("First Name").ToString().Length)
```


# DataTable


```scala
if(dtData.RowCount=0,dtData.clone,Result.CopyToDataTable)
```

```scala
String.Join(", ", customersDT.AsEnumerable().Where(Function (row) row.Field(of String)("First Name").Length=4).Select(Function (row) row.Field(Of String)("Email")))
```

```scala
string.Join(Environment.NewLine, customersDT.AsEnumerable().Where(Function (row) row.Field(Of String)("First Name").Length = 4).Select(Function (row) row.Field(of String)("First Name")))
```

```scala
dt_OutPutDataTable_Email.AsEnumerable().Take(7).CopyToDataTable
```


# array


```scala
dt_items.AsEnumerable().Select(Function(x) x.Field(Of String)("name")).Distinct().ToArray()
```

# list


```scala
dt_items.AsEnumerable().Select(Function(x) x.Field(Of String)("name")).Distinct().ToList()
```

```scala
dt_items.AsEnumerable().GroupBy(Function(x) x.Field(Of String)("name")).Where(Function(y) y.Count() > 1).Select(Function(z) z.Key).ToList()
```

```scala
dt_items.AsEnumerable().GroupBy(Function(x) x.Field(Of String)("name")).Where(Function(y) y.Count() > 1).Select(Function(z) z.Key).ToArray()
```

```scala
dt_items.AsEnumerable().GroupBy(Function(i) i.Field(Of String)("name")).Where(Function(g) g.Count() > 1).SelectMany(Function(g) g).CopyToDataTable()
```

```scala
dt_items.AsEnumerable().GroupBy(Function(row) row.Field(Of string)("id")).Select(Function(x) x.First).CopyToDatatable
```

```scala
dt_items.AsEnumerable().GroupBy(Function(i) i.Field(Of String)("name")).Where(Function(g) g.Count() > 1).SelectMany(Function(g) g).CopyToDataTable()
```

```scala
dt_items.AsEnumerable().GroupBy(Function(i) i.Field(Of String)("name")).Where(Function(g) g.Count() = 1).SelectMany(Function(g) g).CopyToDataTable()
```

```scala
dt_items.DefaultView.ToTable(True,"Col1","Col2")
```

```scala
dt_items.AsEnumerable().GroupBy(Function(x) x.Field(Of String)("name")).Where(Function(y) y.Count() = 1).Select(Function(z) z.Key).ToArray()
```

```scala
dt_items.AsEnumerable().GroupBy(Function(x) x.Field(Of String)("name")).Where(Function(y) y.Count() = 1).Select(Function(z) z.Key).ToList()
```

```scala
dt_items.AsEnumerable().GroupBy(Function(i) i.Field(Of String)("name")).Where(Function(g) g.Count() = 1).SelectMany(Function(g) g).CopyToDataTable()
```

```scala
dt_items.AsEnumerable().GroupBy(Function(x) x.Field(Of String)("name")).Where(Function(y) y.Count() > 1).Select(Function(z) z.Key).ToList()
```

```scala
dt_items.AsEnumerable().GroupBy(Function(x) x.Field(Of String)("name")).Where(Function(y) y.Count() > 1).Select(Function(z) z.Key).ToArray()
```

```scala
dt_items.AsEnumerable().GroupBy(Function(i) i.Field(Of String)("name")).Where(Function(g) g.Count() > 1).SelectMany(Function(g) g).CopyToDataTable()
```

```scala
dt_items.AsEnumerable().Select(Function(x) x.Field(Of String)("name")).Distinct().ToArray()
```

```scala
dt_items.AsEnumerable().Select(Function(x) x.Field(Of String)("name")).Distinct().ToList()
```

```scala
dt_items.AsEnumerable().GroupBy(Function(row) row.Field(Of string)("id")).Select(Function(x) x.First).CopyToDatatable
```


# Double


```scala
dt_items.AsEnumerable().Sum(Function(x) Convert.ToDouble(x.Field(Of Object)("id")))
```



# IEnu - DataRow


```scala
customersDT.AsEnumerable.Where(Function (row) row.Field(Of String)("Email").Contains("shamm@sugarwell.org"))
```

```scala
customersDT.AsEnumerable.Where(Function (row) row.Field(Of String)("Email").Contains("shamm@sugarwell.org")).ToList()
```

```scala
dt.AsEnumerable().Where(Function(row) row("ColName").ToString="abc").CopyToDataTable()
```





















You can read more ([https://github.com/rpa92/uipath/blob/main/README.md](https://github.com/rpa92/uipath/blob/main/README.md))

# Conclusion<a id="sec-3" name="sec-3"></a>

While you may want to structure your projects different. This set up works and is the one that I will continue to update. If you want to contribute please feel free to submit a pull request!
