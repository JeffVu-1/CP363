# <span style="color:#f3c00c;">CP363 Assignments</span>

This repository contains my assignments for CP363, which focuses on MySQL databases. The assignments include various tasks and exercises that I completed to reinforce concepts such as database design, SQL queries, and database management.

## Task for Each Assignment

<details>
<summary style="font-weight:bold; font-size:1.2rem;">Assignment 1 - Simple Queries</summary>
<ol>
    <li>Selects all rows from the broad table sorted by the broad category description.</li>
    <li>Selects rows from the broad table that start with the word 'Military' sorted by the broad category description.</li>
    <li>Selects rows from the broad table that contain the word 'Military' sorted by the broad category description. (This is not the same query as the previous task.)</li>
    <li>Selects the publication title and authors for all rows in the pub table sorted by the publication title.</li>
    <li>Selects the publication title for rows in the pub table for member William Bain sorted by the publication title.</li>
    <li>Selects the publication title of books in the pub table sorted by the publication title.</li>
    <li>Selects the publication title of books in the pub table written by Allan English sorted by the publication title.
        <ul>
            <li>Note: "Written by" in this context means that Allan English owns the books listed in the sense that it is his member ID given in the publication tuple, not that his name appears in the pubAuthors attribute.</li>
        </ul>
    </li>
    <li>Selects the broad category description for rows in the vMemberBroad view for Terry Copp sorted by the broad category description.</li>
    <li>Selects the member surname and forename for rows in the vMemberBroad table for the broad category Military History sorted by the member surname then forename.</li>
    <li>Selects all rows from the narrow table sorted by the narrow category description then the broad category ID.</li>
    <li>Selects the broad and narrow descriptions for all rows from the vBroadNarrow view sorted by broad category description then the narrow category description.</li>
    <li>Selects the narrow category descriptions for rows in the vBroadNarrow view for the broad category Military History sorted by the narrow category description.</li>
</ol>
</details>

<details>
<summary style="font-weight:bold; font-size:1.2rem;">Assignment 2 - Joins and Aggregation</summary>
<ol>
    <li>Selects the full member name, the full publication type, and the publication title for all members, sorted by the full member name, then the full publication type, then the publication title.</li>
    <li>Selects the full member name, the full publication type, and the publication title for members associated with Laurier, sorted by the full member name.</li>
    <li>Selects the full member name and the publication title for conference papers with the word 'Nuclear' in the title, sorted by the publication title.</li>
    <li>Selects the publication title and the full publication type for William Bain, sorted by the publication title.</li>
    <li>Selects the full member name and the number of publications for each member, sorted by the full member name. (Hint: some members have no publications, but we still want the count for them).</li>
    <li>Selects the full member name and the number of books for each member, sorted by the full member name. (Hint: some members have no books, but we still want the count for them).</li>
    <li>Selects the full publication type and the number of publications for each type, sorted by the full publication type.</li>
    <li>Selects the full member name and the number of broad expertises for each member, sorted by the full member name.</li>
    <li>Selects the broad expertise descriptions and the number of members who have that expertise, sorted by the expertise description.</li>
    <li>Selects the full member name and the number of narrow expertises for each member, sorted by the full member name.</li>
    <li>Selects the narrow expertise descriptions and the number of members who have that expertise, sorted by the expertise description.</li>
    <li>Selects the member full name, the member's narrow expertises, and the broad expertise that the narrow expertises belong to, sorted by the full member name then the narrow expertise description.</li>
</ol>
</details>


<details>
<summary style="font-weight:bold; font-size:1.2rem;">Assignment 3 - Subqueries</summary>
<ol>
    <li>Selects the full member name and the number of publications for each member of each publication type. Name publication type fields books, articles, and papers. Sort the results by the full member name.</li>
    This is an example of a subset of the results:
        <table border="1">
            <tr>
                <th>memberSurname</th>
                <th>memberForename</th>
                <th>books</th>
                <th>articles</th>
                <th>papers</th>
            </tr>
            <tr>
                <td>Bain</td>
                <td>William</td>
                <td>4</td>
                <td>2</td>
                <td>0</td>
            </tr>
        </table>
    <li>Selects the full member name and the number of broad and narrow expertises for each member. Name these expertise count fields broadCount and narrowCount. Sort the results by the full member name.</li>
    This is an example of a subset of the results:
        <table border="1">
            <tr>
                <th>memberSurname</th>
                <th>memberForename</th>
                <th>broadCount</th>
                <th>narrowCount</th>
            </tr>
            <tr>
                <td>Bedeski</td>
                <td>Robert</td>
                <td>6</td>
                <td>5</td>
            </tr>
            </table>
    <li>Selects the full member name and narrow expertise descriptions for members who have a narrow expertise in the Environmental Security broad category, but who have not declared that they have a broad expertise in the Environmental Security. Sort the results by the full member name.</li>
    <li>There are members who have a certain narrow expertise but who have not declared that they have the matching broad expertise. For example, Alistair D. Edgar has a narrow expertise in the Second World War, but does not claim to have a broad expertise in Military History, which is the category that Second World War belongs to.</li>
    <li>Selects the full member name and broad expertise descriptions for members who do not have publications. Sort the results by the full member name and then broad expertise description.</li>
    <li>Selects the full member name and publication count for all members with four or more publications. Name the publication count pubCount. Sort the results by the full member name. You must do this with a subquery and not with the HAVING clause.</li>
    <li>Selects the narrow expertise descriptions of all narrow expertises that are not held by any member. Sort the results by the narrow expertise description.</li>
    <li>Selects the broad expertise descriptions of all broad expertises that are not held by any member. Sort the results by the broad expertise description.</li>
    <li>Selects the full member name and broad expertise count for all members with eight or more broad expertises. Name the broad expertise count broadCount. Sort the results by the full member name. You must do this with a subquery and not with the HAVING clause.</li>
    <li>Selects the full member name and narrow expertise count for all members with thirty or more narrow expertises. Name the narrow expertise count narrowCount. Sort the results by the full member name. You must do this with a subquery and not with the HAVING clause.</li>
    <li>Selects the broad expertise description for all broad expertises that do not have any associated narrow expertises. Sort the results by the broad expertise description.</li>
</ol>
</details>


<details>
<summary style="font-weight:bold; font-size:1.2rem;">Assignment 4 - Metadata</summary>
<ol>
    <li>Selects the TABLE_NAME, TABLE_TYPE, TABLE_ROWS, and TABLE_COMMENT attributes from the TABLES table. Sort the results by the table name.</li>
    This is an example of a subset of the results:
         <table border="1">
            <tr>
                <th>TABLE_NAME</th>
                <th>TABLE_TYPE</th>
                <th>TABLE_ROWS</th>
                <th>TABLE_COMMENT</th>
            </tr>
            <tr>
                <td>broad</td>
                <td>BASE TABLE</td>
                <td>19</td>
                <td>Contains broad categories of security expertise.</td>
            </tr>
        </table>
    <li>Selects the TABLE_NAME, TABLE_TYPE, TABLE_ROWS, and TABLE_COMMENT attributes from the TABLES table for tables with 100 or more rows. Sort the results by the table name.</li>
    <li>Selects the TABLE_NAME, IS_NULLABLE, COLUMN_NAME, and DATA_TYPE attributes from the COLUMNS table. Sort the results by the table name and then column name.</li>
    <li>Selects the TABLE_NAME, COLUMN_NAME, and DATA_TYPE attributes from the COLUMNS table for nullable columns. Sort the results by the table name and then column name.</li>
    <li>Selects the CONSTRAINT_NAME, TABLE_NAME, and CONSTRAINT_TYPE attributes from the TABLE_CONSTRAINTS table. Sort the results by the constraint name and then table name.</li>
    <li>Selects the CONSTRAINT_NAME and TABLE_NAME attributes from the TABLE_CONSTRAINTS table for UNIQUE constraints. Sort the results by the constraint name and then table name.</li>
    <li>Selects the CONSTRAINT_NAME, UPDATE_RULE, DELETE_RULE, TABLE_NAME, and REFERENCED_TABLE_NAME attributes from the TABLE_CONSTRAINTS REFERENTIAL_CONSTRAINTS table. Sort the results by the constraint name, then table name, then referenced table name.</li>
    <li>Selects the CONSTRAINT_NAME, UPDATE_RULE, TABLE_NAME, and REFERENCED_TABLE_NAME attributes from the TABLE_CONSTRAINTS REFERENTIAL_CONSTRAINTS table for constraints whose delete rule is not CASCADE. Sort the results by the constraint name, then table name, then referenced table name.</li>
    <li>Selects the CONSTRAINT_NAME, TABLE_NAME, COLUMN_NAME, REFERENCED_TABLE_NAME, and REFERENCED_COLUMN_NAME attributes from the KEY_COLUMN_USAGE table. Sort the results by the table name and then column name.</li>
    <li>Selects the TABLE_NAME, COLUMN_NAME, REFERENCED_TABLE_NAME, and REFERENCED_COLUMN_NAME attributes from the KEY_COLUMN_USAGE table for primary keys only. Sort the results by the table name and then column name.</li>
</ol>

</details>

## <span style="color:#f3c00c;">Disclaimer</span>  
This repository contains my personal work for **CP363**. Feel free to use it as a resource for learning and understanding MySQL. However, please do not submit this work as your own in any academic setting. I am not responsible for any misuse of this content.
