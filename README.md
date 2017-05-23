![GitHub Logo](https://s3.ap-south-1.amazonaws.com/greyatom-social/GreyAtom-logo.png)

# LIKE Clause

The SQL LIKE clause is used to compare a value to similar values using wildcard operators. There are two wildcards used in conjunction with the LIKE operator.

- The percent sign (%)
- The underscore (_)

The percent sign represents zero, one or multiple characters. The underscore represents a single number or character. These symbols can be used in combinations.

### Syntax

        SELECT FROM table_name
        WHERE column LIKE 'XXXX%'

        or

        SELECT FROM table_name
        WHERE column LIKE '%XXXX%'

        or

        SELECT FROM table_name
        WHERE column LIKE 'XXXX_'

        or

        SELECT FROM table_name
        WHERE column LIKE '_XXXX'

        or

        SELECT FROM table_name
        WHERE column LIKE '_XXXX_'

You can combine N number of conditions using AND or OR operators. Here, XXXX could be any numeric or string value.

The following table has a few examples showing the WHERE part having different LIKE clause with '%' and '_' operators −


| No | Statement | Description |
| ---------- | ------------ | ------- |
| 1 | WHERE SALARY LIKE '200%' | Finds any values that start with 200. |
| 2 | WHERE SALARY LIKE '%200%' | Finds any values that have 200 in any position. |
| 3 | WHERE SALARY LIKE '_00%' | Finds any values that have 00 in the second and third positions. |
| 4 | WHERE SALARY LIKE '2_%_%' | Finds any values that start with 2 and are at least 3 characters in length. |
| 5 | WHERE SALARY LIKE '%2' | Finds any values that end with 2. |
| 6 | WHERE SALARY LIKE '_2%3' | Finds any values that have a 2 in the second position and end with a 3. |
| 7 | WHERE SALARY LIKE '2___3' | Finds any values in a five-digit number that start with 2 and end with 3. |

Following is an example, which would display all the records from the Customers table, where the CustomerName starts with Fr.

        SELECT * FROM greyatom.Customers WHERE CustomerName LIKE 'Fr%';

This would produce the following result −

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
| ---------- | ------------ | ----------- | ------- | ---- | ---------- | ------- |
|25 |	Frankenversand |	Peter Franken |	Berliner Platz 43 |	München |	80805 |	Germany |
|26 |	France restauration |	Carine Schmitt |	54, rue Royale |	Nantes |	44000 |	France |
|27 |	Franchi S.p.A. |	Paolo Accorti |	Via Monte Bianco 34 |	Torino |	10100 |	Italy |
