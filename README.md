#Excel Challenges
Feel free to contact me if you want help with any of these. Try the hyperlinks on this page first, which go to the official Microsoft Excel documentation at [support.office.com](https://support.office.com/en-us/excel), if you get stuck. This isn't meant to be a tutorial, mostly because the tutorials at the official site are so amazingly in-depth and helpful. So unless you already know how to do something, click the links!

###Challenges

1. **Saving and Opening a File**  
Click the "Sample Data.xslx" file above to download it from this GitHub repository to your computer, and open it in Excel.

2. **The Text to Columns Wizard**  
Copy and paste the Program field from column C into column F.  
Use the [Text to Columns](https://support.office.com/en-us/article/Split-names-by-using-the-Convert-Text-to-Columns-Wizard-2cd989db-2b1f-4d89-b17b-534250ff9905) wizard (under Data -> Data Tools -> Text to Columns) to split Column F (like "BM4.UNDL") into two values: the value before the period (like "BM4") to remain in column F, and the value after the period (like "UNDL") to move to column G.  
**Hint:** Because the "." character is used to separate the first part of the program from the second, it is called a "delimiter."
**Note:** All of the challenges after this one (#2) can be solved by writing a formula. With each formula, you only have to write it once. Write the formula in row 2 in the requested column, then copy and paste it down into all the other rows.

3. **Using IF (and Nested Formulas, and OR)**  
Write a formula in column G that displays "Bachelors" for students with the Program Code "BM4", "Diploma" for "PDM" or "TWO". You can do this using the formula [IF](https://support.office.com/en-us/article/IF-function-69AED7C9-4E8A-4755-A9BC-AA8BBFF73BE2).  
**Bonus:** You get bonus points if the student in row 11, "Joe Problemchild," throws an error, instead of incorrectly displaying "Diploma" or "Bachelors" (since his code is "MM", something I never told you about). You can do this using a second IF formula nested inside the first one, and/or the formula [OR](https://support.office.com/en-us/article/OR-function-7d17ad14-8700-4281-b308-00b131e22af0).

4. **Using VLOOKUP (Easy Mode)**  
Write a formula in column H that shows the Major String value. To do this, write a [VLOOKUP](https://support.office.com/en-us/article/VLOOKUP-function-0bbc8083-26fe-4963-8ab8-93a18ad188a1) function.  
**Hint:** The table_array (the second argument) for this VLOOKUP should be:  
    'indexes'!$A$2:$B$42  
Don't worry too much about the range_lookup (the fourth, last, and optional argument) for this kind of VLOOKUP.

5. **Using VLOOKUP (Hard Mode)**  
Now that you know how to write VLOOKUP formulas, replace the "Program Name" formula you wrote in challenge 3 (column H) with a VLOOKUP. This time, you can write the range_lookup argument yourself.  
**Hint:** This lookup table is included in the Sample Data too, in the same place as the last one. It's the second sheet in the Excel workbook, named "indexes".  
**Hint 2:** You have to add in dollar signs before the column and row in the range, just like in the range_lookup that I gave you for the previous challenge ($A$2:$B$42). The dollar signs' purpose is to indicate that the range of majors is an [absolute reference](https://blogs.office.com/2011/08/17/making-sense-of-dollar-signs-in-excel/) (meaning the range doesn't change when this formula is copied and pasted to another cell).

6. **Using COUNTIF and Another Nested IF**  
Write a formula that compares the student ID to the range of all the student IDs, returning "DUPE" if it is a duplicate and "-" otherwise. You can use [COUNTIF](https://support.office.com/en-us/article/COUNTIF-function-e0de10c6-f885-4e71-abb4-1f464816df34) to determine if the ID is a duplicate, and [IF](https://support.office.com/en-us/article/IF-function-69AED7C9-4E8A-4755-A9BC-AA8BBFF73BE2) to show the words "DUPE" only in that case.  
**Hint:** Same as in challenge 5, the COUNTIF will not work properly unless its range argument has [absolute reference indicators](https://blogs.office.com/2011/08/17/making-sense-of-dollar-signs-in-excel/).

Here is an example showing the desired output for each field. The bold values are the sample data; the non-bold values are the requested output for each challenge.

Berklee ID | Name | Program | Status | Program Code | Major | Program Name | Major Name | Duplicate?
--- | --- | --- | --- | --- | --- | --- | --- | :---:
**0360009** | **Bob Kelso** | **BM4.UNDL** | **FT** | BM4 | UNDL | Bachelors | Undeclared | -
