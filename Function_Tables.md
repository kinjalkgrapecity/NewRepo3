# Functions

You can use a function in an expression to perform actions on data in data regions, groups, and datasets. You can access these functions under the **Functions** node within the **Expression Editor** dialog. In any property that accepts expressions, you can drop down the property and select **<Expression...>** to open the dialog.

Refer to the following tables that contain details of the common functions included in Wyn Enterprise for use **Expression Editor**:

## **Date & Time**

| **Function**  |  **Description** | **Syntax (S) and Example (E)**  | 
|:---|:---|:---|
| **DateAdd**  | Returns a date and time value that is the result of adding the interval to the date and time field of the specified unit.  | **S**: DateAdd(\<DateInterval>, \<Number>, \<DateTime>)<br/>  **E**: {DateAdd("d", 5, SaleDate)}; {DateAdd(DateInterval.Day, 5, SaleDate)}  | 
| **DateDiff**  | Returns the difference between the start date and time and end date and time of the specified unit.  | **S**: DateDiff(\<DateInterval>, \<DateTime1>, \<DateTime2>[, \<DayOfWeek>[, \<WeekOfYear>]])<br/> **E**: {DateDiff("yyyy", SaleDate, "1/1/2015")}; {DateDiff(DateInterval.Year, SaleDate, "1/1/2015")}  | 
| **DatePart**  | Returns the Integer value that represents the specified part of the given date.  | **S**: DatePart(\<DateInterval>, \<DateTime>[, \<FirstDayOfWeek>[, \<FirstWeekOfYear>]])<br/> **E**: {DatePart("m", SaleDate)} | 
| **DateSerial**  | Returns a Date value that represents a specified year, month, and day, with the time information set to midnight (00:00:00).  | **S**: DateSerial(\<Year Number>, \<Month Number>, \<Day Number>)<br/> **E**: {DateSerial(DatePart("yyyy", SaleDate) - 10, DatePart("m", SaleDate) + 5, DatePart("d", SaleDate) - 1)}  | 
| **DateString**  | Returns the String value that represents the current date in your system.  | **S**: DateString()<br/> **E**: {DateString()}; {DatePart("m", DateString())}  | 
| **DateValue**  | Returns a Date value that contains the information on date represented by a string, with the time set to midnight (00:00:00).  | **S**: DateValue(\<StringDate>)<br/> **E**: {DateValue("December 12, 2015")}  | 
| **Day**  | Returns an Integer value from 1 through 31 that represents the day of the month.  | **S**: Day(\<DateTime>)<br/> **E**: {Day(SaleDate)} | 
| **Hour**  | Returns an Integer value from 0 through 23 that represents the hour of the day.  | **S**: Hour(\<DateTime>)<br/> **E**: {Hour(SaleDate)} | 
| **Minute**  | Returns an Integer value from 0 through 59 that represents the minute of the hour.  | **S**: Minute(\<DateTime>)<br/> **E**: {Minute(SaleDate)} | 
| **Month**  | Returns an Integer value from 1 through 12 that represents the month of the year.  | **S**: Month(\<DateTime>)<br/> **E**: {Month(SaleDate)} | 
| **MonthName**  | Returns the name of the month specified in the date as a String.  | **S**: MonthName(\<Month Number>[, \<Abbreviate>])<br/> **E**: {MonthName(MonthNumber)} | 
| **Now**   | Returns the current date and time in your system.  | **S**: Now()<br/> **E**: {Now()}  | 
| **Second**  | Returns an Integer value from 0 through 59 that represents the second of the minute.  | **S**: Second(\<DateTime>)<br/> **E**: {Second(SaleDate)}  | 
| **TimeOfDay**  | Returns a Date value containing the current time of day in your system.  | **S**: TimeOfDay()<br/> **E**: {TimeOfDay()}  | 
| **Timer**  | Returns a Double value that represents the number of seconds elapsed since midnight.  | **S**: Timer()<br/> **E**: {Timer()}  | 
| **TimeSerial**  | Returns a Date value that represents a specified hour, minute, and second, with the date information set relative to January 1 of the year 0001.  | **S**: TimeSerial(\<Hour Number>, \<Minute Number>, \<Second Number>)<br/> **E**: {TimeSerial(DatePart("h", SaleDate), DatePart("n", SaleDate), DatePart("s", SaleDate))}  | 
| **TimeString**  | Returns the String value that represents the current time of day in your system.  | **S**: TimeString()<br/> **E**: {TimeString()} | 
| **TimeValue**  | Returns a Date value that contains the information on time represented by a string, with the date set to January 1 of the year 0001.  | **S**: TimeValue(\<StringTime>)<br/> **E**: {TimeValue("15:25:45")}; {TimeValue(SaleDate)} | 
| **Today**  | Returns a Date value that contains the current date in your system.  | **S**: Today()<br/> **E**: {Today()} | 
| **Weekday**  | Returns an Integer value that contains a number representing the day of the week.  | **S**: Weekday(\<DateTime>[, \<DayOfWeek>])<br/> **E**: {Weekday(SaleDate, 0)} | 
| **WeekdayName**  | Returns a String value that contains the name of the specified weekday.  | **S**: WeekdayName(\<WeekDay>[, \<Abbreviate>[, \<FirstDayOfWeek>]])<br/> **E**: {WeekdayName(3, true, 0)}; {WeekDayName(DatePart("w", SaleDate), true, 0)} | 
| **Quarter**  | Returns an Integer value from 1 through 4 that represents the quarter of the year.  | **S**: Quarter(\<DateTime>)<br/> **E**: {Quarter(SaleDate)} | 
| **QuarterName**  | Returns a String value that represents the quarter of the year.  | **S**: QuarterName(\<DateTime>)<br/> **E**: {QuarterName(SaleDate)} | 
| **Year**  | Returns an Integer value from 1 through 9999 representing the year.  | **S**: Year(\<DateTime>)<br/> **E**: {Year(SaleDate)} | 
| **AddYears**  | Returns a date and time value that is a result of adding the date interval in years. The specified date interval can be negative.  | **S**: \<DateTime>.AddYears(\<Number><br/>) **E**: {OrderDate.AddYears(3)}  | 
| **AddMonths**  | Returns a date and time value that is a result of adding the date interval in months. The specified date interval can be negative.  | **S**: \<DateTime>.AddMonths(\<Number>)<br/> **E**: {OrderDate.AddMonths(2)}  | 
| **AddDays**  | Returns a date and time value that is a result of adding the date interval in days. The specified date interval can be negative.  | **S**: \<DateTime>.AddDays(\<Number>)<br/> **E**: {OrderDate.AddDays(5)}  | 
| **AddHours**  | Returns a date and time value that is a result of adding the time interval in hours. The specified time interval can be negative.  | **S**: \<DateTime>.AddHours(\<Number>)<br/> **E**: {OrderDate.AddHours(12)}  | 
| **AddMinutes**  | Returns a date and time value that is a result of adding the time interval in minutes. The specified time interval can be negative.  | **S**: \<DateTime>.AddMinutes(\<Number>)<br/> **E**: {OrderDate.AddMinutes(30)}  | 
| **AddSeconds**  | Returns a date and time value that is a result of adding the time interval in seconds. The specified time interval can be negative.  | **S**: \<DateTime>.AddSeconds(\<Number>)<br/> **E**: {OrderDate.AddSeconds(30)}  | 
| **AddMilliseconds**  | Returns a date and time value that is a result of adding the time interval in milliseconds. The specified time interval can be negative. | **S**: \<DateTime>.AddMilliseconds(\<Number>)<br/> **E**: {OrderDate.AddMilliseconds(500)}  | 
| **DateTime.Parse**  | Converts the specified string value to a date and time value.  | **S**: DateTime.Parse(\<String>[, \<String>])<br/> **E**: {DateTime.Parse("01/01/1970")}  | 





## **Math**

| **Function**  |  **Description** | **Syntax (S) and Example (E)**  | 
|:---|:---|:---|
| **Abs**  | Returns the absolute or positive value of a single-precision floating-point number.  | **S**: Abs(\<Number>)<br/> **E**: {Abs(-5.5)}; {Abs(YearlyIncome - 80000)}  | 
| **Acos**  | Returns the angle whose cosine is the specified number.  | **S**: Acos(\<Number>)<br/> **E**: {Acos(0.5)}; {Acos(Angle)}  | 
| **Asin**  | Returns the angle whose sine is the specified number.  | **S**: Asin(\<Number>)<br/> **E**:  {Asin(0.5)}; {Asin(Angle)} | 
| **Atan**  | Returns the angle whose tangent is the specified number.  | **S**: Atan(\<Number>)<br/> **E**: {Atan(0.5)}; {Atan(Angle)}  | 
| **Atan 2**  | Returns the angle whose tangent is the quotient of two specified numbers.  | **S**: Atan2(\<Number1>, \<Number2>)<br/> **E**: {Atan2(3, 7)}; {Atan2(CoordinateY, CoordinateX)}  | 
| **BigMul**  | Returns the multiplication of two 32-bit numbers.  | **S**: BigMul(\<Number1>, \<Number2>)<br/> **E**: {BigMul(4294967295, -2147483647)}; {BigMul(Int32Value, Int32Value)} | 
| **Ceiling**  | Returns the smallest integer greater than or equal to the specified double-precision floating-point number.  | **S**: Ceiling(\<Number>)<br/> **E**: {Ceiling(98.4331)}; {Ceiling(AnnualSales / 6)}  | 
| **Cos**  | Returns the smallest integer greater than or equal to the specified double-precision floating-point number.  | **S**: Cos(\<Number>)<br/> **E**: {Cos(60)} | 
| **Cosh**  | Returns the hyperbolic cosine of the specified angle.  | **S**: Cosh(\<Number>)<br/> **E**: {Cosh(60)}  | 
| **E**  | Returns the value of E, which is 2.71828182845905.  | **S**: E<br/> **E**: {E * 2} | 
| **Exp**  | Returns e raised to the specified power, where e is Euler's number. It is the inverse of the Log function.  | **S**: Exp(\<Number>)<br/> **E**: {Exp(3)}; {Exp(IntegerCounter)}  | 
| **Fix** | Returns the integer portion of a number.  | **S**: Fix(\<Number>)<br/> **E**: {Fix(-7.15)}; {Fix(AnnualSales / -5)}  | 
| **Floor**  | Returns the largest integer less than or equal to the specified double-precision floating-point number.  | **S**: Floor(\<Number>)<br/> **E**: {Floor(4.67)}; {Floor(AnnualSales / 12)}  | 
| **IEEERemainder**  | Returns the remainder after division of one number by another according to IEEE standards.  | **S**: IEEERemainder(\<Number1>, \<Number2>)<br/> **E**: {IEEERemainder(9, 8)}  | 
| **Log**  | Returns the logarithm of the specified number.  | **S**: Log(\<Number>)<br/> **E**: {Log(20.5)}; {Log(NumberValue)}  | 
| **Log10**  | Returns the logarithm of the specified number to the base 10.  | **S**: Log10(\<Number>)<br/> **E**: {Log10(20.5)}; {Log10(NumberValue)}  | 
| **Max**  | Returns the maximum non-null value from the specified expression.  | **S**: Max(\<Values>)<br/> **E**: {Max(OrderTotal)}  | 
| **Min**  | Returns the minimum non-null value from the specified expression.  | **S**: Min(\<Values>)<br/> **E**: {Min(OrderTotal)}  | 
| **PI**  | Returns the value of PI, which is 3.14159265358979.  | **S**: PI<br/> **E**: {2 * PI * Radius}  | 
| **Pow**  | Returns one number raised to the power of another number.  | **S**: Pow(\<Number1>, \<Number2>)<br/> **E**: {Pow(Quantity, 2)}  | 
| **Round**  | Returns the round-off of a decimal number to the nearest integer or to the nearest decimal number up to the specified digits.  | **S**: Round(\<Number>)<br/> **E**: {Round(12.456)}; {Round(AnnualSales / 12.3)}  | 
| **Sign**  | Returns a value indicating the sign of an 8-bit signed integer.  | **S**: Sign(\<Number>)<br/> **E**: {Sign(AnnualSales - 60000)}  | 
| **Sin**  | Returns the sine of the specified number.  | **S**: Sin(\<Number>)<br/> **E**: {Sin(60)}  | 
| **Sinh**  | Returns the hyperbolic sine of the specified angle.  | **S**: Sinh(\<Number>)<br/> **E**: {Sinh(60)}  | 
| **Sqrt**  | Returns the square root of the specified number.  | **S**: Sqrt(\<Number>)<br/> **E**: {Sqrt(121)}  | 
| **Tan**  | Returns the tangent of the specified number.  | **S**: Tan(\<Number>)<br/> **E**: {Tan(60)}  | 
| **Tanh**  | Returns the hyperbolic tangent of the specified angle.  | **S**: Tanh(\<Number>)<br/> **E**: {Tanh(60)}  | 
| **Truncate**  | Removes the digits after decimal point without rounding-off, and returns the integer value.  | **S**: Truncate(\<Number>)<br/> **E**: {Truncate(UnitPrice)}  | 


## **Text**

| **Function**  |  **Description** | **Syntax (S) and Example (E)**  | 
|:---|:---|:---|
| **Contains**   | Returns True if the string contains the specified substring.  | **S**: \<String>.Contains(\<String>)<br/> **E**: {ShipAddress.Contains("street")}  | 
| **EndsWith**  | Returns True if the string ends with the specified substring.  | **S**: \<String>.EndsWith(\<String>)<br/> **E**: {Description.EndsWith("documents")}  | 
| **IndexOf**  | Returns the index of the first occurrence of the specified substring within the string.  | **S**: \<String>.IndexOf(\<String>[, \<Number>])<br/> **E**: {Description.IndexOf("documents")}  | 
| **InStr**  | Returns the start position of the first occurrence of the specified substring within the string.  | **S**: InStr(\<String>, \<String>)<br/> **E**: {InStr(Description, "documents")}  | 
| **LastIndexOf**  | Returns the index of the last occurrence of the specified substring within the string.  | **S**: \<String>.LastIndexOf(\<String>[, \<Number>])<br/> **E**: {Description.LastIndexOf("documents")}  | 
| **Replace**  | Replaces all the occurrences of the first specified substring with the second specified substring within the string.  | **S**: \<String>.Replace(\<String>, \<String>)<br/> **E**: {Description.Replace("documents", "invoices")}  | 
| **StartsWith**  | Returns True if the string starts with the specified substring.  | **S**: \<String>.StartsWith(\<String>)<br/> **E**: {Description.StartsWith("Invoice")}  | 
| **Substring**  | Returns the substring at the specified position (zero-based) of the specified length.  | **S**: \<String>.Substring(\<Number>, \<Number>)<br/> **E**: {Description.Substring(1, 10)}  | 
| **ToLower**  | Returns the specified string in lower case.  | **S**: \<String>.ToLower()<br/> **E**: {ShipCountry.ToLower()}  | 
| **ToUpper**  | Returns the specified string in upper case.  | **S**: \<String>.ToUpper()<br/> **E**: {ShipCountry.ToUpper()}  | 
| **Trim**  | Returns the string after removing all the white-space characters from both the start and the end of the specified string.  | **S**: \<String>.Trim()<br/> **E**: {@Info.Trim()}  | 
| **TrimEnd**  | Returns the string after removing all the white-space characters from the end of the specified string.  | **S**: \<String>.TrimEnd()<br/> **E**: {@Info.TrimEnd()}  | 
| **TrimStart** | Returns the string after removing all the white-space characters from the start of the specified string. | **S**: \<String>.TrimStart()<br/> **E**: {@Info.TrimStart()}  | 


## **Inspection**

| **Function**  |  **Description** | **Syntax (S) and Example (E)**  | 
|:---|:---|:---|
| **IsArray**  | Returns True if the expression can be evaluated as an array.  | **S**: IsArray(\<Expression>)<br/> **E**: {IsArray(@Initials)}  | 
| **IsDate**  | Returns True if the expression represents a valid Date value.  | **S**: IsDate(\<Expression>)<br/> **E**: {IsDate(BirthDate)}; {IsDate("31/12/2010")}  | 
| **IsDBNull**  | Returns True if the expression evaluates to a null.  | **S**: IsDBNull(\<Expression>)<br/> **E**: {IsDBNull(MonthlySales)}  | 
| **IsError**  | Returns True if the expression evaluates to an error.  | **S**: IsError(\<Expression>)<br/> **E**: {IsError(AnnualSales = 80000)}  | 
| **IsNothing**   | Returns True if the expression evaluates to nothing.  | **S**: IsNothing(\<Expression>)<br/> **E**: {IsNothing(MiddleInitial)}  | 
| **IsNumeric**  | Returns True if the expression can be evaluated as a number.  | **S**: IsNumeric(\<Expression>)<br/> **E**: {IsNumeric(AnnualSales)}  | 
| **DBNull.Value**  | Allows checking whether a value is a DBNull value.  | **S**: DBNull.Value<br/> **E**: {IIF(Organization is DBNull.Value, "\<NULL>", Organization)}  | 


## **Program Flow**

| **Function**  |  **Description** | **Syntax (S) and Example (E)**  | 
|:---|:---|:---|
| **Choose**  | Returns a value from a list of arguments.  | **S**: Choose(\<Index>, \<Value1>[, \<Value2>,...[, \<ValueN>]])<br/> **E**: {Choose(3, "10", "15", "20", "25")}  | 
| **IIF**  | Returns the first value if the expression evaluates to True, and the second value if the expression evaluates to False.  | **S**: IIF(\<Condition>, \<TruePart>, \<FalsePart>)<br/> **E**: {IIF(AnnualSales >= 80000, "Above Average", "Below Average")}  | 
| **Partition**  | Returns a string (in the form x : y) that represents the calculated range based on the specified interval containing the specified number.  | **S**: Partition(\<Value>, \<Start>, \<End>, \<Interval>)<br/> **E**: {Partition(1999, 1980, 2000, 10)}  | 
| **Switch**  | Returns the value of the first expression that evaluates to True among a list of expressions.  | **S**: Switch(\<Condition1>, \<Value1>[, \<Condition2>, \<Value2>,...[, \<ConditionN>, \<ValueN>]])<br/> **E**: {Switch(FirstName = "Abraham", "Adria", FirstName = "Charelotte", "Cherrie")}  |



## **Aggregate**

| **Function**  |  **Description** | **Syntax (S) and Example (E)**  | 
|:---|:---|:---|
| **AggregateIf**  | Calculates the aggregate of the values from the specified expression if the Boolean expression meets the given condition.  | **S**: AggregateIf(\<Condition>, \<AggregateFunction>, \<AggregateArguments>)<br/> **E**: {AggregateIf(Discontinued = true, "Sum", InStock)}  | 
| **AggregateIf (with scope)**  | Calculates the aggregate of the values from the specified expression if the Boolean expression meets the given condition, within the specified scope.  | **S**: AggregateIf(\<Condition>, \<AggregateFunction>, \<AggregateArguments>, \<Scope>)<br/> **E**: {AggregateIf(Discontinued = true, "Sum", InStock, "Category")}  | 
| **Avg**  | Calculates the average of all non-null numeric values from the specified expression.  | S: Avg(\<Values>) E: {Avg(LifeExpentancy)}  | 
| **Avg (with scope)**  | Calculates the average of all non-null numeric values from the specified expression within the specified scope.  | **S**: Avg(\<Values>, \<Scope>)<br/> **E**: {Avg(LifeExpentancy, "GroupByCountry")}  | 
| **Count**  | Calculates the number of non-null values from the specified expression.  | S: Count(\<Values>) E: {Count(EmployeeID)}  | 
| **Count (with scope)**  | Calculates the number of non-null values from the specified expression within the specified scope.  | **S**: Count(\<Values>, \<Scope>)<br/> **E**: {Count(EmployeeID, "Title")}  | 
| **CountDistinct**  | Calculates the number of non-repeated values from the specified expression.  | **S**: CountDistinct(\<Values>)<br/> **E**: {CountDistinct(OrderID)}  | 
| **CountDistinct (with scope)**  | Calculates the number of non-repeated values from the specified expression within the specified scope.  | **S**: CountDistinct(\<Values>, \<Scope>)<br/> **E**: {CountDistinct(OrderID, "GroupByCategory")}  | 
| **CountRows**  | Calculates the number of rows.  | **S**: CountRows()<br/> **E**: {CountRows()}  | 
| **CountRows (with Scope)**  | Calculates the number of rows within the specified scope.  | **S**: CountRows(\<Scope>)<br/> **E**: {CountRows("Title")}  | 
| **CrossAggregate**  | Calculates the specified function with specified expression as an argument in the cross of specified row and column.  | **S**: CrossAggregate(\<Expression>, \<FunctionName>, \<ColumnGroupName>, \<RowGroupName>)<br/> **E**: {CrossAggregate(Amount, "Sum", "YearGroup", "CategoryGroup")}  | 
| **CumulativeTotal**  | Calculates the sum of page-level aggregates returned by the expression for current and previous pages.  | **S**: CumulativeTotal(\<Expression>, \<Aggregate>)<br/> **E**: {CumulativeTotal(OrderID, "Count")}  | 
| **DistinctSum** | Calculates the sum of values from the specified expression when the value of the other expression is not repeated.  | **S**: DistinctSum(\<Values>, \<Value>)<br/> **E**: {DistinctSum(OrderID, OrderFreight)}  | 
| **DistinctSum (wih scope)**  | Calculates the sum of values of the specified expression when the value of the other expression is not repeated, within the specified scope.  | **S**: DistinctSum(\<Values>, \<Value>, \<Scope>)<br/> **E**: {DistinctSum(OrderID, OrderFreight, "Order")}  | 
| **First**  | Returns the first value from the specified expression.  | **S**: First(\<Values>)<br/> **E**: {First(ProductNumber)}  | 
| **First (with scope)**  | Returns the first value from the specified expression within the specified scope.  | **S**: First(\<Values>, \<Scope>)<br/> **E**: {First(ProductNumber, "Category")}  | 
| **Last**  | Returns the last value from the specified expression.  | **S**: Last(\<Values>)<br/> **E**: {Last(ProductNumber)}  | 
| **Last (with scope)**  | Returns the last value from the specified expression within the specified scope.  | **S**: Last(\<Values>, \<Scope>)<br/> **E**: {Last(ProductNumber, "Category")}  | 
| **Max**  | Returns the maximum non-null value from the specified expression.  | **S**: Max(\<Values>)<br/> **E**: {Max(OrderTotal)}  | 
| **Max (with scope)**  | Returns the maximum non-null value from the specified expression within the specified scope.  | **S**: Max(\<Values>, \<Scope>)<br/> **E**: {Max(OrderTotal, "Year")}  | 
| **Median**  | Returns the value that is the mid-point of the values in the specified expression. Median is the center value in a sequence of values.  | **S**: Median(\<Values>)<br/> **E**: {Median(OrderTotal)}  | 
| **Median (with scope)**  | Returns the value that is the mid-point of the ordered values in the specified expression, within the specified scope. Median is the center value in a sequence of values.  | **S**: Median(\<Values>, \<Scope>)<br/> **E**: {Median(OrderTotal, "Year")}  | 
| **Min**  | Returns the minimum non-null value from the specified expression.  | **S**: Min(\<Values>)<br/> **E**: {Min(OrderTotal)}  | 
| **Min (with scope)**  | Returns the minimum non-null value from the specified expression within the specified scope.  | **S**: Min(\<Values>, \<Scope>)<br/> **E**: {Min(OrderTotal, "Year")}  | 
| **Mode**  | Returns the most frequently occurring value from the specified expression.  | **S**: Mode(\<Values>)<br/> **E**: {Mode(OrderTotal)}  | 
| **Mode (with scope)**  | Returns the most frequently occurring value from the specified expression, within the specified scope.  | **S**: Mode(\<Values>, \<Scope>)<br/> **E**: {Mode(OrderTotal, "Year")}  | 
| **RunningValue**   | Calculates a running aggregate of all non-null numeric values from the specified expression, using another aggregate function as a parameter.  | **S**: RunningValue(\<Values>, \<AggregateFunction>)<br/> **E**: {RunningValue(Price, "Sum")}  | 
| **RunningValue (with scope)**  | Calculates a running aggregate of all non-null numeric values from the specified expression, using another aggregate function as a parameter, within the specified scope.  | **S**: RunningValue(\<Values>, \<AggregateFunction>, \<Scope>)<br/> **E**: {RunningValue(Price, "Sum", "Nwind")}  | 
| **StDev**  | Calculates the standard deviation of all non-null values of the specified expression.  | **S**: StDev(\<Values>)<br/> **E**: {StDev(LineTotal)}  | 
| **StDev (with scope)**  | Calculates the standard deviation of all non-null values of the specified expression, within the specified scope.  | **S**: StDev(\<Values>, \<Scope>)<br/> **E**: {StDev(LineTotal, "Nwind")}  | 
| **StDevP**  | Calculates the population standard deviation of all non-null values of the specified expression.  | **S**: StDevP(\<Values>)<br/> **E**: {StDevP(LineTotal)}  | 
| **StDevP (with scope)**  | Calculates the population standard deviation of all non-null values of the specified expression within the specified scope.  | **S**: StDevP(\<Values>, \<Scope>)<br/> **E**: {StDevP(LineTotal, "Order")}  | 
| **Sum**  | Calculates the sum of the values of the specified expression.  | **S**: Sum(\<Values>)<br/> **E**: {Sum(Price)}  | 
| **Sum (with scope)**  | Calculates the sum of the values of the specified expression within the specified scope.  | **S**: Sum(\<Values>, \<Scope>)<br/> **E**: {Sum(Price, "Category")}  | 
| **Var**  | Calculates the variance (standard deviation squared) of all non-null values of the specified expression.  | **S**: Var(\<Values>)<br/> **E**: {Var(LineTotal)}  | 
| **Var (with scope)**  | Calculates the variance (standard deviation squared) of all non-null values of the specified expression.  | **S**: Var(\<Values>, \<Scope>)<br/> **E**: {Var(LineTotal, "Order")}  | 
| **VarP**   | Calculates the population variance (population standard variation squared) of all non-null values of the specified expression.  | **S**: VarP(\<Values>)<br/> **E**: {VarP(LineTotal)}  | 
| **VarP (with scope)**  | Calculates the population variance (population standard variation squared) of all non-null values of the specified expression, within the specified scope.  | **S**: VarP(\<Values>, \<Scope>)<br/> **E**: {VarP(LineTotal, "Order")}  | 

## **Conversion**

| **Function**  |  **Description** | **Syntax (S) and Example (E)**  | 
|:---|:---|:---|
| **ToBoolean**  | Converts the specified value to Boolean.  | **S**: ToBoolean(\<Value>)<br/> **E**: {ToBoolean(HouseOwnerFlag)}  | 
| **ToByte**  | Converts the specified value to Byte.  | **S**: ToByte(\<Value>)<br/> **E**: {ToByte(ProductNumber)}  | 
| **ToChar**  | Converts the specified value to Char.  | **S**: ToChar(\<Value>)<br/> **E**: {ToChar(OrderStatus)}; {ToChar(“Hello”)}  | 
| **ToDateTime**  | Converts the specified value to a Date and Time value.  | **S**: ToDateTime(\<Value>)<br/> **E**: {ToDateTime(SaleDate)}; {ToDateTime("1 January, 2017")}  | 
| **ToDecimal**  | Converts the specified value to Decimal.  | **S**: ToDecimal(\<Value>)<br/> **E**: {ToDecimal(Sales)}  | 
| **ToDouble**   | Converts the specified value to Double .  | **S**: ToDouble (\<Value>)<br/> **E**: {ToDouble(AnnualSales)}; {ToDouble(535.85 * 0.2691 * 67483)}  | 
| **ToInt16**  | Converts the specified value to a 16-bit signed Integer.  | **S**: ToInt16(\<Value>)<br/> **E**: {ToInt16(AnnualSales)}; {ToInt16(535.85)}  | 
| **ToInt32**  | Converts the specified value to a 32-bit signed Integer.  | **S**: ToInt32(\<Value>)<br/> **E**: {ToInt32(AnnualSales)}  | 
| **ToInt64**  | Converts the specified value to a 64-bit signed Integer.  | **S**: ToInt64(\<Value>)<br/> **E**: {ToInt64(AnnualSales)}  | 
| **ToSingle**  | Converts the specified value to a single-precision floating-point number.  | **S**: ToSingle(\<Value>)<br/> **E**: {ToSingle(AnnualSales)}; {ToSingle(15.857692134)}  | 
| **ToString**  | Converts the specified value to String.  | **S**: ToString(\<Value>)<br/> **E**: {ToString(YearlyIncome)}; {ToString(13.5)}  | 
| **.ToString**  | Converts the value to String in the specified format.  | **S**: .ToString(\<Value>)<br/> **E**: {OrderDate.ToString("dd MMM yyyy")}  | 
| **ToUInt16**  | Converts the specified value to a 16-bit unsigned Integer.  | **S**: ToUInt16(\<Value>)<br/> **E**: {ToUInt16(AnnualSales)}  | 
| **ToUInt32**  | Converts the specified value to a 32-bit unsigned Integer.  | **S**: ToUInt32(\<Value>)<br/> **E**: {ToUInt32(AnnualSales)}  | 
| **ToUInt64**  | Converts the specified value to a 64-bit unsigned Integer.  | **S**: ToUInt64(\<Value>)<br/> **E**: {ToUInt64(AnnualSales)}  | 
| **Format**  | Converts the specified value to rmat.  | **S**: Format(\<Value>)<br/> **E**: {Format(OrderDate, "dd MMM yyyy")}  | 
| **NumberToWords**  | Converts the specified value to words. Single argument function uses the current language from the portal. A function with two arguments uses the language passed by the second argument(Supported cultures: "zh-cn", "en-us", "ja-jp").  | **S**: NumberToWords(<Value>)<br/> **E**: {UserContext.NumberToWords(123.5)}; {UserContext.NumberToWords(981, "zh-CN")}  | 
 


 ## **Miscellaneous**

| **Function**  |  **Description** | **Syntax (S) and Example (E)**  | 
|:---|:---|:---|
| **GetFields**  | Returns an IDictionary<string,Field> object that contains the current contents of the Fields collection. Only valid when used within a data region. This function makes it easier to write code that deals with complex conditionals. To write the equivalent function without GetFields() would require passing each of the queried field values into the method which could be prohibitive when dealing with many fields.  | **S**: GetFields()<br/> **E**: {GetFields()}; {Code.DisplayAccountID(GetFields())} | 
| **InScope**  | Evaluates to true or false depending on whether the current value is in the specified scope.  | **S**: InScope(\<Scope>)<br/> **E**: {InScope("Order")}| 
| **Level**  | Returns a zero-based integer representing the current level of depth in a recursive hierarchy in the current scope. The first level in the hierarchy is 0.  | **S**: Level()<br/> **E**: {Level()}| 
| **Level (with scope)**  | Returns a zero-based integer representing the current level of depth in a recursive hierarchy in the specified scope. The first level in the hierarchy is 0. | **S**: Level(\<Scope>)<br/> **E** {Level("Order")}| 
| **Level (with scope)**  | Returns a zero-based integer representing the current level of depth in a recursive hierarchy in the specified scope. The first level in the hierarchy is 0. | **S**: Level(\<Scope>)<br/> **E**: {Level("Order")}| 
| **Lookup**  | Returns the first matching value for the specified name from the dataset with name and value pairs.  | **S**: Lookup(\<Source>, \<Destination>, \<Result>, \<DataSet>)<br/> **E**: {Lookup(ProductID, ProductID, Quantity, "DataSet2")}  | 
| **LookupSet**  | Returns the set of matching values for the specified name from the dataset that contains name/value pairs.  | **S**: LookupSet(\<Source>, \<Destination>, \<Result>, \<DataSet>)<br/> **E**: {LookupSet(ProductID, ProductID, Quantity, "DataSet2")}  | 
| **Previous**  | Calculates the value of the expression for the previous row of data.  | **S**: Previous(\<Expression>)<br/> **E**: {Previous(OrderID)}  | 
| **Previous (with scope)**  | Calculates the value of the expression for the previous row of data within the specified scope.  | **S**: Previous(\<Expression>, \<Scope>)<br/> **E**: {Previous(OrderID, "Order")}  | 
| **RowNumber**  | Returns the running count of all the rows.  | **S**: RowNumber()<br/> **E**: {RowNumber()}  | 
| **RowNumber (with scope)**  | Returns the running count of all the rows in the specified scope.  | **S**: RowNumber(\<Scope>)<br/> **E**: {RowNumber("OrderID")}  | 
| **GetLength**  | Returns the number of elements in the specified array.  | **S**: \<Collection>.GetLength(\<Number>)<br/> **E**: {@MultiValueParameter.GetLength(0)}  | 
| **Item**  | Returns an item by its name from Fields/Parameters/ReportItems.  | **S**: <Object \| Record>.Item(\<String>)<br/> **E**: {Fields.Item("Company Name").Name}; {Parameters.Item("Parameter1").Name}; {ReportItems.Item("TextBox1").Value}  | 
| **Join**  | Returns a string that is a result of joining the elements of an array, using the specified delimiter between elements.  | **S**: Join(\<Values>, \<String>)<br/> **E**: {Join(@MultiValueParameter, ", ")}  | 
| **GetUserValue**  | Displays the user context value for specified property, e.g. "name","email".  | **S**: UserContext.getValue(\<String>)<br/> **E**: {UserContext.getValue("name")}  | 
| **UserContext.T**  | Displays the user translation for specified key.  | **S**: UserContext.T(\<String>)<br/> **E**: {UserContext.T("translationKey")}  | 