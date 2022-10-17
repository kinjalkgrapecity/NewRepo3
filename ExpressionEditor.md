
# Wyn Enterprise: Expression Editor

An expression is a syntactic entity that produces a desired output on execution. Expressions consists of functions, values (fields), operators, constants, queries, and identifiers. 

**Expression Editor** in Wyn Enterprise is a pop-up dialog that is used to create or edit meaningful expressions at run-time. **Expression Editor** is used to set the values of a control in reports and set conditions under which certain styles apply. 

![ExpressionEditorWindow]()

**Expression Editor** helps you customize raw data in a meaningful form using expressions. Following are a few examples of how Expression Editor are set in different scenarios:
    
   * **Concatenating Fields and Strings**
   
       You can concatenate fields with strings and with other fields. For example, use the following expression to get a result like "Customer Name: Bossert, Lewis":
   
          Customer Name: {LastName} , {FirstName}

   * **Conditional Formatting**
   
       You can use expressions in properties like Color, Font, Border, etc. on specific field values based on a condition, to highlight a part of data. The formula for conditional formatting is:

         {IIF(<Condition>, <TruePart>, <FalsePart>)}


       For example, if you enter the following expression in the Font > FontWeight property of a textbox that displays the names of people, you get the name "Denise" in bold.
   
         {IIF(FirstName { "Denise", "Bold", "Normal")}
           
        Similarly, if you enter the following expression in the Background >Color property of a textbox in a table, then you get alternating 'Transparent' and 'LightGray' colored textboxes in the rows of the table.
              
         {IIF(RowNumber(Nothing) mod 2, "Transparent", "LightGray")} 


   * **Functions**
   
       You can use a number of aggregate and other functions in your expressions. Wyn Enterprise includes a range of functions, including running value, population standard variance, standard deviation, count, minimum and maximum. For e.g., use the following expression to get a count of employees.

         {Count(EmployeeID, Nothing)}

## Attributes of Expression Editor

  Expression Editor has three major attributes,

   1. **Expression pane**
   2. **Values**
   3. **Functions**

### Expression pane

  **Expression pane** is the input area of the **Expression Editor Window** where you enter the expressions as strings.  
   > Note: All expressions are enclosed within curly braces **'{}'**. Even the expression for a field value for a TextBox is set as: `{LastName}`.

### Values
**Values** are the input fields available to the selected report. Following Values are available in the Expression Editor: 

   1. **Constants**: are static constants like numbers or strings. For example, 123, and “abc”.  

   2. **Common Values**: refers to the built-in field values of the report. For example, current page number and total number of pages.  

   3. **Parameters**: this node represents the parameters of the report defined in the report designer.  

   4. **Data Sets**: this node lists the datasets and fields linked to the selected report. 

   5. **Operations**: this node lists arithmetic, comparison, concatenation, logical/bitwise, and bit shift operators.  

   6. **Documents Map**: defines the labels of the TOC (Table of Content) members of the selected report. 

   7. **Theme**: lists the visual settings including fonts, colors, constant, and images. A combination of two or more theme elements are used to increase the graphical appeal of a table in the selected report.  

   8. **Report Items**: lists all the field items available as textboxes in the selected report. 


### Functions
**Functions** are used in an expression to perform actions on data in data regions, groups, and datasets. You can access these functions under the Functions node within the Expression Editor dialog. Following functions are available in Wyn Expression Editor,

   1. **Date & Time**: this node lists all procedures and properties from **DateAndTime class** available in Microsoft Visual Basic. Refer [this link](https://docs.microsoft.com/en-us/dotnet/api/microsoft.visualbasic.dateandtime?view=netframework-4.8) for more information.
   2. **Math**: lists all methods and fields from **System.Math class** of Visual Basic. Refer [this link](https://docs.microsoft.com/en-us/dotnet/api/system.math?view=netframework-4.8) for more information.
   3. **Text**: lists all the methods of the string functions used to manipulate the text data in reports. 
   4.	**Inspection**: lists functions used to inspect field values and other parameters of the selected report. Inspection functions are often used in process functions such as **IIF**.
   5.	**Program Flow**: lists methods from **Interaction class** in Visual Basic that are used to interact with objects in the selected report. Refer [this link](https://docs.microsoft.com/en-us/dotnet/api/microsoft.visualbasic.interaction?redirectedfrom=MSDN&view=netframework-4.8) for more information.
   6.	**Aggregate**: lists aggregate functions used to include aggregated values for pagination in the selected report. Refer [this link](https://learn.microsoft.com/en-us/sql/reporting-services/report-design/report-builder-functions-aggregate-functions-reference?view=sql-server-ver16) for more information.
   7.	**Conversion**: lists the methods from Convert class in **.Net Framework** that are used to convert one base data type to another base data type. Refer [this link](https://docs.microsoft.com/en-us/dotnet/api/system.convert?redirectedfrom=MSDN&view=netframework-4.8) for more information.
   8.	**Miscellaneous**: Wyn Report Designer offers several functions which do not aggregate data but are used with an **IIf** function to help determine which data to display or how to display it.


## To Create Expressions

To access the **Expression Editor** in Wyn Enterprise follow the below instructions,
1.	Navigate to the **Resource or Document Portal >> Categories** tab. 
2.	Select a report under Document pane. Either click the edit button on the top-right corner of the window or click the ellipses icon and choose the **Edit** option. Selected report will open in the edit mode. 
3.	Select the text box you wish to create or edit the expression for. Now, under **Properties** grid on right-side of your screen click the yellow square box next to the Value field in the Common section and click the **Expression** option. Expression Editor Window will appear on your screen. 

To create an expression or to edit the content of an expression, follow the below instructions,
1.	In the **Expression Editor Window**, select an expression element from the Values or Functions section or directly enter the expression in the Expression pane. You can either drag and drop or double-click the expression element to add in the Expression pane. 
2.	Click **Save** button to finish adding the expression.
3.	Following tables describe various expression elements available in Wyn Expression Editor. 


