# Values

Values are run-time values available for all properties in each report. You can directly drag and drop these common values from the **Report Explorer** onto the design surface or add and modify the values from the **Expression Editor**. Following is a list of the values that you can see under the **Common Values** node in the **Report Explorer** and the **Expression Editor**. following tables list various common values with description, syntax and exmaple availble to all reports in Wyn Enterprise,


## **COMMON VALUES**

| **Value**  | **Description**   | **Expression**   |
|---     |---           |---          |
|  **Current Date and Time**  |Displays the current date and time. It can be used in the Page Header and Page Footer.   | {&ExecutionTime}  |  
|  **Page Number** | Displays the current page number. It can be used in the Page Header and Page Footer.  | {&PageNumber}  |  
|  **Total Pages** | Displays the total number of pages. It can be used in the Page Header and Page Footer.  | {&TotalPages}  |  
|  **Page N of M** | Displays the current page number (N) and the total number of pages (M) in the format 'N of M'. It can be used in the Page Header and Page Footer.  | Page {&PageNumber} of {&TotalPages}  |  
| **Page Number (Section)**  | Displays the current page number of the section to which the function belongs. The section can be a report or a data region.  | {&PageNumberInSection}  |  
| **Total Pages (Section)**  | Displays the total number of pages of the section to which the function belongs. The section can be a report or a data region.  | {&TotalPagesInSection}  |  
| **Page N of M (Section)**  | Displays the current page number (N) and the total number of pages (M) in the format 'N of M,' of the section to which the function belongs. The section can be a report or a data region.  | Page {&PageNumberInSection} of {&TotalPagesInSection}  |   
| **Report Name**  | Displays the name of the report.  | {&ReportName}  |  
| **User ID**   | Displays the User ID of the user previewing the report.  | {User!UserID}  |   
| **User Language**  | Displays the Language of the user previewing the report as per system settings.  | {User!Language}  |  
| **User Context**  | "Use only with function, e.g. UserContext.GetValue(""name""), UserContext.NumberToWords(123)." | \{UserContext}|



## **OPERATIONS**

### **Arithmetic**

| **Value** | **Description** | **Syntax (S) and Example (E)** |
|:---|:---|:---|
| ^ |  Raises a number to the power of another number. | **S**: \<Number1> ^ \<Number2><br /> **E**: {Quantity ^ 2}  |
| *  | Evaluates the multiplication of two numbers.  | **S**: \<Number1> * \<Number2><br /> **E**: {Quantity * 5}   | 
| **/**  | Divides two numbers (numerator by denominator) and returns the quotient as a floating-point number.  | **S**: \<Number1> / \<Number2><br /> **E**: {AnnualSales / 2} | 
| **\**  | Divides two numbers and returns an integer result.  | **S**: \<Number1> \ \<Number2><br /> **E**: {AnnualSales \ 2} | 
| **Mod**  | Divides two numbers and returns the remainder.  | **S**: \<Number1> Mod \<Number2><br /> **E**: {AnnualSales Mod 12} |
| **+**  | Evaluates the sum of two numbers or concatenates two strings.  | **S**: \<Value1> + \<Value2><br /> **E**: {Quantity + 2} | 
| **-**  | Evaluates the difference between two numbers or negates the value of a numeric expression.  | **S**: \<Number1> - \<Number2><br /> **E**: {Quantity - 2} |

### **Comparision**

| **Value**  |  **Description** | **Syntax (S) and Example (E)**  | 
|:---|:---|:---|
| **<**  | Returns True if the left operand is less than the right operand.  | **S**: \<Value1> < \<Value2><br />  **E**: {AnnualSales < 80000}  | 
| **<=**  | Returns True if the left operand is less than or equal to the right operand.  | **S**: \<Value1> <= \<Value2><br />  **E**: {AnnualSales <= 80000}  | 
| **>**  | Returns True if the left operand is greater than the right operand.  | **S**: \<Value1> > \<Value2><br />  **E**: {AnnualSales > 80000}  | 
| **>=**  | Returns True if the left operand is greater than or equal to the right operand.  | **S**: \<Value1> >= \<Value2><br />  **E**: {AnnualSales >= 80000}  | 
| **=**  | Returns True if the left operand is equal to the right operand.  | **S**: \<Value1> = \<Value2><br />  **E**: {AnnualSales = 80000}  | 
| **<>**  | Returns True if the left operand is not equal to the right operand.  | **S**: \<Value1> <> \<Value2><br />  **E**: {AnnualSales <> 80000}  | 
| **Like**  | Compares two strings and returns True if the left operand is the same as the right operand.  | **S**: \<String1> Like \<String2><br />  **E**: {FirstName Like "A*"}  | 
| **Is**  | Compares two object references and returns True if the left operand is identical to the right operand.  | **S**: \<Value1> Is \<Value2><br />  **E**: {FirstName Is LastName}  | 

### **Concatenation**

| **Value**  |  **Description** | **Syntax (S) and Example (E)**  | 
|:---|:---|:---|
| **&**  | Returns the string value of the concatenation of two expressions that individually evaluate to strings.  | **S**: \<String1> & \<String2><br /> **E**: {FirstName & " " & LastName}  | 
| **+**  | Evaluates the sum of two numbers or concatenates two strings.  | **S**: \<String1> + \<String2><br /> **E**: {FirstName + " " + LastName} | 

### **Logical / Bitwise**

| **Value**  |  **Description** | **Syntax (S) and Example (E)**  |  
|:---|:---|:---|
| **And**  | Returns the logical conjunction of two Boolean expressions, or the bitwise conjunction of two numeric expressions.  | **S**:\<Value1> And \<Value2><br />  **E**: {AnnualSales > 80000 And Quantity > 5}  | 
| **Not**  | Returns the logical negation of a Boolean expression, or the bitwise negation of a numeric expression.  | **S**: Not \<Value><br /> **E**: {Not AnnualSales > 80000}  | 
| **Or**  | Returns the logical disjunction of two Boolean expressions, or the bitwise disjunction of two numeric values.  | **S**: \<Value1> Or \<Value2><br /> **E**: {AnnualSales > 80000 Or Quantity > 5}  | 
| **Xor**  | Returns a logical exclusion operation of two Boolean expressions, or a bitwise exclusion of two numeric expressions.  | **S**: \<Value1> Xor \<Value2><br /> **E**: {AnnualSales > 80000 Xor Quantity > 5}  | 
| **AndAlso**  | Returns the logical conjunction of two Boolean expressions by skipping evaluation of the other expression if the evaluation of the first expression provides the result.  | **S**: \<Boolean1> AndAlso \<Boolean2><br /> **E**: {AnnualSales > 80000 AndAlso Quantity > 1}  | 
| **OrElse**  | Returns the logical disjunction of two Boolean expressions by skipping evaluation of one expression if the evaluation of the other expression provides the result.  | **S**: \<Boolean1> OrElse \<Boolean2><br /> **E**: {AnnualSales > 80000 OrElse Quantity > 1}  | 


### **Bit Shift**

| **Value**  | **Description** | **Syntax (S) and Example (E)**  | 
|:---|:---|:---|
| **<<** | Performs an arithmetic left shift on a bit pattern.  | **S**: \<Number1> << \<Number2><br /> **E**: {RegionID << 2} | 
| **>>**  | Performs an arithmetic right shift on a bit pattern.  | **S**: \<Number1> >> \<Number2><br /> **E**: {RegionID >> 2} | 




## **DOCUMENT MAP**

| **Value**  |  **Description** | **Expression**  | 
|:---|:---|:---|
| **Path**  |  Returns the path of the TOC level. | \{DocumentMap.Path} This is Heading 1 | 





