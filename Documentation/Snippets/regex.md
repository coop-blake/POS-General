# Regular Expressions
Powerful String Pattern Matching 

## Online Resources
### Practice/Testing expressions
  * [https://regex101.com/](https://regex101.com/)  
  * [https://regexr.com/](https://regexr.com/)

## Examples

### Find five digit numbers  
Could also be 12 or any number


| Syntax | Description |
| ----------- | ----------- |
| `^\d{5}$` | Find lines that are a 5 Digit number |
| `^(.*)\d{5}(.*)$` | Finds 5 Digit Numbers inside other characters in a line |
