#Excel Challenges

Contact Ben Quigley at Berklee if you want help with any of this! Be sure to click the links, which go to the official Microsoft Excel documentation at [support.office.com](https://support.office.com/en-us/excel), if you get stuck.

1. Download the "Sample Data.xslx" file from this GitHub repo.

2. Copy and paste the Program field from column C into column F.  
Use the [Text to Columns](https://support.office.com/en-us/article/Split-names-by-using-the-Convert-Text-to-Columns-Wizard-2cd989db-2b1f-4d89-b17b-534250ff9905) wizard (under Data -> Data Tools -> Text to Columns) to split Column F into two columns, F and G.  
**Hint:** The delimiter should be whatever character separates the first column value from the second column value.  
**Note:** All of the challenges after #2 can be solved by writing a formula. With each formula, you only have to write it once. Write the formula in row 2 in the requested column, then copy and paste it down into all the other rows.

3. Write a formula in column G that displays "Bachelors" for students with the Program Code "BM4", "Diploma" for "PDM" or "TWO". Formulas that can help you with this are [IF](https://support.office.com/en-us/article/IF-function-69AED7C9-4E8A-4755-A9BC-AA8BBFF73BE2) and [OR](https://support.office.com/en-us/article/OR-function-7d17ad14-8700-4281-b308-00b131e22af0).  
Bonus points if the student in row 11, "Michel Foucault," throws an error, instead of incorrectly displaying "Diploma" or "Bachelors" (since his code is "SNM", something I never told you about).

4. Write a formula in column H that shows the Major String value. To do this, write a [VLOOKUP](https://support.office.com/en-us/article/VLOOKUP-function-0bbc8083-26fe-4963-8ab8-93a18ad188a1) function.  
**Hint:** The table_array (second argument) for this VLOOKUP should be:  
    'indexes'!$A$2:$B$42
The range_lookup argument can be 0.

5. Now that you know how to write VLOOKUPs 


Here is an example. The values in italics are what you are being asked to create.

**Program** | ... | **Program Code** | **Major** | **Program Name**
--- | --- | --- | --- | ---
BM4.UNDL | ... | *BM4* | *UNDL* | *Bachelors* | *Undeclared*