# 4d-generic-structure

a structure with `255` tables, `511` text fields each

## about

* created with version 2004
* table `1` created manually **pro tip**: do this first!
* all other tables created using 4D Pack command `AP Add table and fields`

```4d
ARRAY TEXT($fieldNames;0)
ARRAY LONGINT($fieldTypes;0)
ARRAY LONGINT($fieldLengths;0)

For ($i;1;511)
	APPEND TO ARRAY($fieldNames;"Field"+String($i))
	APPEND TO ARRAY($fieldTypes;Is Text )
	APPEND TO ARRAY($fieldLengths;0)
End for 

For ($i;2;255)
	$tableName:="Table"+String($i)
	$tableNumber:=AP Add table and fields ($tableName;$fieldNames;$fieldTypes;$fieldLengths;"";"")
End for 

```
