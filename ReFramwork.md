# About ReFramwork<a id="sec-3" name="sec-3"></a>


# Condtion

```scala
IsNothing(out_TransactionData) or out_TransactionData.RowCount = 0
```

```scala
io_TransactionData.RowCount >= in_TransactionNumber
```

# o_str_TransactionItem

```scala
io_TransactionData.Rows(in_TransactionNumber-1).Item("Trans1").ToString
```

# o_str_TransactionItemRequire

```scala
Convert.ToBoolean(io_TransactionData.Rows(in_TransactionNumber-1).Item("IsRequired"))
```
