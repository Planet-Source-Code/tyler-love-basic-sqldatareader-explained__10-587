<div align="center">

## Basic SqlDataReader Explained


</div>

### Description

This is a short tutorial explaining how you would go about reading data from your database on to an application or an ASP.NET web page.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Tyler Love](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/tyler-love.md)
**Level**          |Beginner
**User Rating**    |3.6 (32 globes from 9 users)
**Compatibility**  |C\#, ASP\.NET
**Category**       |[Databases](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/databases__10-5.md)
**World**          |[\.Net \(C\#, VB\.net\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/net-c-vb-net.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/tyler-love-basic-sqldatareader-explained__10-587/archive/master.zip)





### Source Code

<size="12px">1. Create a sqlConnection to your database using the sqlConnection tool in your tool box. Name it sqlMyCon
<BR><BR>
2. Create a sql command using the sqlCommand tool in your toolbox that will query and return a row that you are wanting. Name it sqlMyCmd. In this case I am wanting to return a specific row so I would do something like this:<BR><BR>
<color="#0000FF">
SELECT * FROM MyTable<BR>
WHERE (ColumnName = '1234567')<BR>
</color>
That would return all the columns in the the table "MyTable". Where there was a row in the Column "ColumnName" that has the integer "1234567" in it.
<BR><BR>
3. Now you have done with that you get to write a few lines of code. So here is the example of how I would go about reading the data that is returned and inserting it into a web page or application. (Pretend I have a label named "lblData")<BR><BR><BR>
<color="#0088FF">
sqlMyCon.Open();<BR>
</color><color="#3CF13C">
// This creates a datareader<BR>
</color><color="#0088FF">
SqlDataReader reader = sqlMyCmd.ExecuteReader();<BR>
reader.Read();<BR>
</color><color="#3CF13C">
//This will select what column's data it will<BR>
// return using "GetString" remember it is zerobased<br>
</color><color="#0088FF">
lblData.Text = reader.GetString(2);<Br>
sqlMyCon.Close();<br>
</color>
<Br><br>
4. Run it and make sure it works. If you would like to see something that uses that and does work go to http://www.junebughunter.net I made that site and all the content comes from a database using almost that exact same thing.
</size>

