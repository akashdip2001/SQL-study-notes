<div style="display: flex; align-items: center; gap: 10px;" align="center"> &nbsp; &nbsp;
   <a href="https://www.youtube.com/watch?v=WFFQw01EYHM"><img src="https://github.com/user-attachments/assets/deba559e-99fb-4a83-ac29-81c1d9210c93" width="47%" /></a> &nbsp;
   <a href="https://www.youtube.com/watch?v=WFFQw01EYHM"><img src="https://github.com/user-attachments/assets/bdbe46fd-4aaa-420d-9e40-c5b9827d5150" width="47%" /></a> &nbsp;
</div>

> Click to see the Cource `video`

</br>
</br>

<div style="display: flex; align-items: center; gap: 10px;" align="center"> &nbsp; &nbsp;
   <a href="#"><img src="https://github.com/user-attachments/assets/dcf9101f-3f00-4e37-9f17-6217a6e8f9b0" width="47%" /></a> &nbsp;
   <a href="#"><img src="https://github.com/user-attachments/assets/02fee3d1-1fca-4abf-ab93-08aa9dc32731" width="45%" /></a> &nbsp;
</div>

## SQL Injection Example

```sql
String DRIVER = "com.ora.jdbc.Driver";
String DataURL = "jdbc:db://localhost:5112/users";
String LOGIN = "admin";
String PASSWORD = "admin123";

Class.forName(DRIVER);

//Make connection to DB
Connection connection = DriverManager.getConnection(DataURL, LOGIN, PASSWORD);

String Username = request.getParameter("USER"); // From HTTP request
String Password = request.getParameter("PASSWORD"); // From HTTP request

int iUserID = -1;

String sLoggedUser = "";

String sel = "SELECT User_id, Username FROM USERS WHERE Username = '" +Username + "' AND Password = '" + Password + "'";

Statement selectStatement = connection.createStatement ();
ResultSet resultSet = selectStatement.executeQuery(sel);


if (resultSet.next()) {
       iUserID = resultSet.getInt(1);
       sLoggedUser = resultSet.getString(2);
}

PrintWriter writer = response.getWriter ();

if (iUserID >= 0) {
       writer.println ("User logged in: " + sLoggedUser);
} else {

       writer.println ("Access Denied!")
}
```

<img width="662" height="365" alt="image" src="https://github.com/user-attachments/assets/521932eb-4c86-4574-ae51-a7dc651d5780" />

### SQL Injection Example

When SQL statements are dynamically created as software executes, there is a window for a security breach as the input data can truncate, malform or even expand the original SQL query!

1. In the code snippet, the request.getParameter retrieves the data for the SQL query directly from the HTTP request without any data validation.
- This error gives rise to the ability to input SQL as the payload and alter the functionality in the statement.
2. The application places the payload directly into the statement causing the SQL vulnerability:

```sql
String sel = "SELECT User_id, Username FROM USERS WHERE Username = '" Username + "' AND Password = '" + Password + "'";
```

---

[<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/b51e322c-e451-4d8d-9b30-0ddbe92b1819"/>](https://www.youtube.com/watch?v=cbmBDiR6WaY)

> Click to see the Cource `video`

## XSS: Find the bug in the code

```xss
<%

1. fcount = RS.Fields.count-1
2. Response.Write("<div class='label'> Search Results </div><br / >")
3. Response.Write("You Searched for :" & Request.Form("txtsearch"))
4. Response.Write("<table border=1><tr bgcolor='#EEEEEE'>")
5. Response.Write("<table border=1><tr bgcolor='#EEEEEE'>")
6. For i=0 to fcount
7. 	Response.Write("<th> &  RS(i).name & "</th>")
8. 	Next
9. 	Response.Write("</tr>")
10. 	While Not RS.EOF
11. 			Response.Write("</tr>")
12.			For i=0 to fcount
13.				Response.Write("<td>" & RS.(i).value &  ("</td>")
14.			Next
15.			Response.Write("</tr>")
16.			RS.MoveNext()
17. 	End While
	
%>
```

## XSS - Solution

```xss
<%

1. fcount = RS.Fields.count-1
2. Response.Write("<div class='label'> Search Results </div><br / >")
3. Response.Write("You Searched for :" & Server.HtmlEncode(Request.Form("txtsearch")))
4. Response.Write("<table border=1><tr bgcolor='#EEEEEE'>")
5. Response.Write("<table border=1><tr bgcolor='#EEEEEE'>")
6. For i=0 to fcount
7. 	Response.Write("<th> &  Server.HtmlEncode(RS(i).name) & "</th>")
8. 	Next
9. 	Response.Write("</tr>")
10. 	While Not RS.EOF
11. 			Response.Write("</tr>")
12.			For i=0 to fcount
13.				Response.Write("<td>" & Server.HtmlEncode(RS.(i).value) &  ("</td>")
14.			Next
15.			Response.Write("</tr>")
16.			RS.MoveNext()
17. 	End While
	
%>
```

`Server.HtmlEncode` function will help in encoding all html tags during output. (Line number 3)

Also we can see line number 7 and 13 where data is being displayed through database content. We have used output encoding also for those kind of output.


</br>
</br>

[<img width="1365" height="577" alt="image" src="https://github.com/user-attachments/assets/68d6ad13-8e3d-459b-87f1-ab2cb28c8bc2"/>](https://pentesterlab.com/exercises/codereview/course)

