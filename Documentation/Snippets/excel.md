# Excel Snippets

### Master Inventory Data Lookup

`=VLOOKUP(A2,MasterInventory.xlsx!ecrs_v_InventoryMaster,5,FALSE)`

Finds the row in MasterInventory.xlsx that matches the Item ID(A2) and returns the data in the coesponding column number(5)

MasterInventory must be opened, use the column numbers below for the data you need

#### Column Numbers    

| Column | Number |
| ----------- | ----------- |
| BRAND |  2| 
| NAME  |  3| 
| SIZE |  4| 
| RECEIPT ALIAS |  5| 
| SUBDEPARTMENT |  7| 
| DEPARTMENT |  9| 
| SUPPLIER ID |  10| 
| BASE PRICE |  11| 
| QUANTITY| 12| 
| LASTCOST |  13| 
| AVERAGECOST |  14| 
| MARGIN |  15| 
| DEFAULT SUPPLIER |  16| 
| UNIT| 17| 
| LAST SOLD| 18|    

## Common Formulas
### Target Margin Price
`=ROUND(D3/(1-(F3*0.01)),2)`
Calculates a target price based on cost(D3) and margin(F3)

### Calculate Acheived Margin
`=1-(A2/B2)`
Calculates the acheived margin from Cost(A2) and Price(B2)

### Check Same Higher Pricing
`=IFS(H2<I2,"GOOD",H2>I2,"HIGHER",H2=I2,"SAME")`
Checks Base Price(I2) and Sale Price(H2) and returns descriptive text of the relationship

### Return cell substrings before and after first occurance of character
#### Return Substring Before First Character
=LEFT(A4,(FIND("*",A4,1)-1))
#### Return Substring After First Character
=RIGHT(A4,LEN(A4)-FIND("*",A4))
