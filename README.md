# DAX
Data Analysis Expressions | [SQLBI](https://www.sqlbi.com/) | [DAX Guide](https://dax.guide/) | [DAX Formatter](https://www.daxformatter.com/) | [DAX Do](https://dax.do/) | [DAX Patterns](https://www.daxpatterns.com/)

`DAX` is a functional language, the execution flows with function calls.

```DAX
Amount = SUM (
           FILTER ( VALUES ( 'Date'[Year] ), 'Date'[Year] < 2005 ),
           IF ( 'Date'[Year] >= 2000, [Sales Amount] * 100, [Sales Amount] * 90 )
         )
```

### Important Terms

1. Data Table or `Fact` Table : Contains measurable values (cost, quantity and prices)
2. Lookup or `Dimension` Table : Provides descriptive attributes about each dimension.
3. `Foreign` Key : Contains multiple instances of each value, and are used to match the `Primary` keys in related Lookup tables.
4. `Primary` Key : Uniquely identifies each `Row` of a table, and match `Foreign` keys in related Data tables.

<table align=center>
           <tr><th colspan=3><h3>DAX Operators</h3></th></tr>
           <tr>
                      <td>
                                 <table>
                                            <tr><th colspan=3>Arithmetic Operator</th></tr>
                                            <tr><td>Addition</td><td>+</td><td>1 + 3</td></tr>
                                            <tr><td>Subtraction</td><td>-</td><td>7 - 3</td></tr>
                                            <tr><td>Multiplication</td><td>*</td><td>5 * 3</td></tr>
                                            <tr><td>Division</td><td>/</td><td>10 / 5</td></tr>
                                            <tr><td>Exponent</td><td>^</td><td>5 ^ 2</td></tr>
                                 </table>
                      </td>
                      <td>
                                 <table>
                                            <tr><th colspan=3>Comparison Operator</th></tr>
                                            <tr><td>Equal to</td><td>=</td><td>[City] = 'Mumbai'</td></tr>
                                            <tr><td>Greater than</td><td>></td><td>[Age] > 18</td></tr>
                                            <tr><td>Less than</td><td><</td><td>[Age] < 18</td></tr>
                                            <tr><td>Greater than or Equal to</td><td>>=</td><td>[Age] >= 18</td></tr>
                                            <tr><td>Less than or Equal to</td><td><=</td><td>[Age] <= 18</td></tr>
                                            <tr><td>Not equal to</td><td><></td><td>[City] <> "Mumbai"</td></tr>
                                 </table>
                      </td>
                      <td>
                                 <table>
                                            <tr><th colspan=3>String or Logical Operator</th></tr>
                                            <tr><td>Concatenate</td><td>&</td><td>[City] & " " & [State]</td</tr>
                                            <tr><td>AND</td><td>&&</td><td>[State] = "MH" && [Country] = "IND"</td</tr>
                                            <tr><td>OR</td><td>||</td><td>[State] = "MH" || [Country] = "IND"</td</tr>
                                            <tr><td>Multiple OR</td><td>IN</td><td>[Region] IN {"AMS","APJ","EMEA"}</td</tr>
                                 </table>
                      </td>
           </tr>         
</table>
