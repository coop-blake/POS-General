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
`=LEFT(A4,(FIND("*",A4,1)-1))`
#### Return Substring After First Character
`=RIGHT(A4,LEN(A4)-FIND("*",A4))`
#### Check expected Magic
`=SWITCH(E7, 
Value(0.2), "5/$1", 
Value(0.25), "4/$1", 
Value(0.34), "3/$1",
Value(0.4), "5/$2",
Value(0.5), "2/$1",
Value(0.6), "5/$3",
Value(0.67), "3/$2",
Value(0.75), "4/$3",
Value(0.8), "5/$4",
Value(1), "5/$5",
Value(1.2), "5/$6",
Value(1.25), "4/$5",
Value(1.34), "3/$4",
Value(1.4), "5/$7",
Value(1.5), "2/$3",
Value(1.6), "5/$8",
Value(1.67), "3/$5",
Value(1.75), "4/$7",
Value(1.8), "5/$9",
Value(2), "2/$4",
Value(2.25), "4/$9",
Value(2.34), "3/$7",
Value(2.5), "2/$5",
Value(2.67), "3/$8",
Value(3), "2/$6",
Value(3.34), "3/$10",
Value(3.5), "2/$7",
Value(4), "2/$8",
Value(4.5), "2/$9",
Value(5), "2/$10",
Value(5.5), "2/$11",
Value(6), "2/$12",
Value(6.5), "2/$13",
Value(7), "2/$14",
Value(7.5), "2/$15",
Value(8), "2/$16",
Value(8.5), "2/$17",
Value(9), "2/$18",
Value(9.5), "2/$19")` 

### Use SupplierID tab to check if item has Distributor entry
`=IFERROR(COUNTIFS(SupplierIDs!$A$2:$A$60000, $A5, SupplierIDs!$B$2:$B$60000, "THRESHOLD") >0, "")`
