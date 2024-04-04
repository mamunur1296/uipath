# About String<a id="sec-3" name="sec-3"></a>


StingManipulation uipath-community  ([https://forum.uipath.com/t/how-to-manipulate-a-part-of-string-split-trim-substring-replace-remove-left-right/140180](https://forum.uipath.com/t/how-to-manipulate-a-part-of-string-split-trim-substring-replace-remove-left-right/140180))

## StingManipulation 

```sh
sbt clean coverage test
```

# Removing Special Characters and Keeping in a Single Line

## Example

### Input:
Hello My@$%^&*               name@                              $%^&* is@$%^&* Mamunur ¬!£$@$%^&* Rushid

Nezam £$$Uddin @$%^&*is 			a@$%^&* Good %^$%>,><Man >>><and 

He @$%^&* is@$%^&*  ><>vary Helpfull Parsone@$%^&*

### Output: 
Hello My                     name                                     is       Mamunur            Rushid Nezam    Uddin       is    a       Good         Man     and  He        is           vary Helpfull Parsone
```scala
System.Text.RegularExpressions.Regex.Replace(strString, "[^a-zA-Z0-9]", " ")
```