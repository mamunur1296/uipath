# About String<a id="sec-3" name="sec-3"></a>


StingManipulation uipath-community  ([https://forum.uipath.com/t/how-to-manipulate-a-part-of-string-split-trim-substring-replace-remove-left-right/140180](https://forum.uipath.com/t/how-to-manipulate-a-part-of-string-split-trim-substring-replace-remove-left-right/140180))

## StingManipulation 

```sh
sbt clean coverage test
```

###### Removing Special Characters and Keeping in a Single Line

## Example:

### Input:
###### Hello My@$%^&*               name@                              $%^&* is@$%^&* Mamunur ¬!£$@$%^&* Rushid
###### Nezam £$$Uddin @$%^&*is 			a@$%^&* Good %^$%>,><Man >>><and 
###### He @$%^&* is@$%^&*  ><>vary Helpfull Parsone@$%^&*


```scala
System.Text.RegularExpressions.Regex.Replace(strString, "[^a-zA-Z0-9]", " ")
```
### Output: 

```scala
Hello My                     name                                     is       Mamunur            Rushid Nezam    Uddin       is    a       Good         Man     and  He        is           vary Helpfull Parsone
```


======================================================================================

###### Removing Special Character Tab and white spaces and keeping in the single line

## Example:

### Input:
###### Hello My@$%^&*               name@                              $%^&* is@$%^&* Mamunur ¬!£$@$%^&* Rushid
###### Nezam £$$Uddin @$%^&*is 			a@$%^&* Good %^$%>,><Man >>><and 
###### He @$%^&* is@$%^&*  ><>vary Helpfull Parsone@$%^&*


```scala
System.Text.RegularExpressions.Regex.Replace(strString, "[^a-zA-Z0-9]+", " ")
```
### Output: 

```scala
Hello My name is Mamunur Rushid Nezam Uddin is a Good Man and He is vary Helpfull Parsone
```


======================================================================================

###### Removing Special Character Tab and white spaces and keeping in the multi line

## Example:

### Input:
###### Hello My@$%^&*               name@                              $%^&* is@$%^&* Mamunur ¬!£$@$%^&* Rushid
###### Nezam £$$Uddin @$%^&*is 			a@$%^&* Good %^$%>,><Man >>><and 
###### He @$%^&* is@$%^&*  ><>vary Helpfull Parsone@$%^&*


```scala
System.Text.RegularExpressions.Regex.Replace(strString, "[^a-zA-Z0-9]+", " ")
```
### Output: 

```scala
Hello My name is Mamunur Rushid
Nezam Uddin is a Good Man and 
He is vary Helpfull Parsone
```


======================================================================================

###### Removing Tab and all spaces and keeping in the single line

## Example:

### Input:
###### Hello My@$%^&*               name@                              $%^&* is@$%^&* Mamunur ¬!£$@$%^&* Rushid
###### Nezam £$$Uddin @$%^&*is 			a@$%^&* Good %^$%>,><Man >>><and 
###### He @$%^&* is@$%^&*  ><>vary Helpfull Parsone@$%^&*


```scala
System.Text.RegularExpressions.Regex.Replace(strString,"\s","")
```
### Output: 

```scala
HelloMy@$%^&*name@$%^&*is@$%^&*Mamunur¬!£$@$%^&*RushidNezam£$$Uddin@$%^&*isa@$%^&*Good%^$%>,><Man>>><andHe@$%^&*is@$%^&*><>varyHelpfullParsone@$%^&*
```


======================================================================================

###### Removing Tab and just white spaces and keeping in the single line

## Example:

### Input:
###### Hello My@$%^&*               name@                              $%^&* is@$%^&* Mamunur ¬!£$@$%^&* Rushid
###### Nezam £$$Uddin @$%^&*is 			a@$%^&* Good %^$%>,><Man >>><and 
###### He @$%^&* is@$%^&*  ><>vary Helpfull Parsone@$%^&*


```scala
System.Text.RegularExpressions.Regex.Replace(strString, "\s+", " ")
```
### Output: 

```scala
Hello My@$%^&* name@ $%^&* is@$%^&* Mamunur ¬!£$@$%^&* Rushid Nezam £$$Uddin @$%^&*is a@$%^&* Good %^$%>,><Man >>><and He @$%^&* is@$%^&* ><>vary Helpfull Parsone@$%^&*
```


======================================================================================

###### Removing Tab and just  spaces and keeping in the multi line

## Example:

### Input:
###### Hello My@$%^&*               name@                              $%^&* is@$%^&* Mamunur ¬!£$@$%^&* Rushid
###### Nezam £$$Uddin @$%^&*is 			a@$%^&* Good %^$%>,><Man >>><and 
###### He @$%^&* is@$%^&*  ><>vary Helpfull Parsone@$%^&*


```scala
System.Text.RegularExpressions.Regex.Replace(strString, " ", "").Replace(vbTab, "")
```
### Output: 

```scala
HelloMy@$%^&*name@$%^&*is@$%^&*Mamunur¬!£$@$%^&*Rushid
Nezam£$$Uddin@$%^&*isa@$%^&*Good%^$%>,><Man>>><and
He@$%^&*is@$%^&*><>varyHelpfullParsone@$%^&*
```




======================================================================================

###### Removing Tab and just white spaces and keeping in the multi line 

## Example:

### Input:
###### Hello My@$%^&*               name@                              $%^&* is@$%^&* Mamunur ¬!£$@$%^&* Rushid
###### Nezam £$$Uddin @$%^&*is 			a@$%^&* Good %^$%>,><Man >>><and 
###### He @$%^&* is@$%^&*  ><>vary Helpfull Parsone@$%^&*


```scala
String.Join(" ",strString.Split({" "},StringSplitOptions.RemoveEmptyEntries)).Replace(vbTab, "")
```
###### or
```scala
String.Join(" ",Regex.Replace(strString,"\t","").Split({" "},StringSplitOptions.RemoveEmptyEntries))
```
### Output: 

```scala
Hello My@$%^&* name@ $%^&* is@$%^&* Mamunur ¬!£$@$%^&* Rushid
Nezam £$$Uddin @$%^&*is a@$%^&* Good %^$%>,><Man >>><and 
He @$%^&* is@$%^&* ><>vary Helpfull Parsone@$%^&*
```


======================================================================================