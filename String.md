# About String<a id="sec-3" name="sec-3"></a>


StingManipulation uipath-community  ([https://forum.uipath.com/t/how-to-manipulate-a-part-of-string-split-trim-substring-replace-remove-left-right/140180](https://forum.uipath.com/t/how-to-manipulate-a-part-of-string-split-trim-substring-replace-remove-left-right/140180))

# StingManipulation 

```sh
sbt clean coverage test
```

```scala
strPdfText.Split({Environment.NewLine},StringSplitOptions.None)
```

```scala
arrStrSplit.Reverse.ToArray
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
String.Join(Environment.NewLine,lstNewData.ToArray)
```

```scala
split(PDF_Data,environment.NewLine).ToList
```

```scala
split(PDF_Data,environment.NewLine).Reverse
```

```scala
split(line.ToString,"Account")(1).Replace("Batch Number","")
```

```scala
String.Format("Reading email subject - [{0}]", in_TransactionItem.Subject)
```

```scala
string.format("{0}\{1}\",Config("ReportFolder").ToString.Trim, "ExceptionScreenshots")
```

```scala
System.Text.RegularExpressions.Regex.Replace(str_RowText,"\s+"," ",System.Text.RegularExpressions.RegexOptions.Multiline).Trim
```

# Link


```scala
System.Text.RegularExpressions.Regex.Replace(Test_Data, "[\r?\n]{2,}", vbcrlf).Trim
```


```scala
If(str_MachineName(0).Groups(1).Value IsNot Nothing, str_MachineName(0).Groups(1).Value, " ")
```
