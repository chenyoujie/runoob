# runoob
## 编写readme.md
<br><br>
直接输入回车，不能换行。<br>
需要输入\<br>
<br>
部分文字高亮显示<br>

`利用tab键上方的按键来包围内容`
<br>
同样的方式，三个\`，可以输入代码片段<br>
``` c#  
try
                {
                    DateTime startTime = DateTime.Now;
                    SqlConnection conn = new SqlConnection(connStr);
                    SqlCommand command = new SqlCommand();
                    command.CommandTimeout = 0;
                    command.Connection = conn;
                    string tablename = "GPS_TABLE_" + orderdate;
                    string commText = "BULK INSERT "+tablename +" FROM " + path + " WITH(FIELDTERMINATOR =',',ROWTERMINATOR ='\n',BATCHSIZE =100000)";
                    //commText += "UPDATE GPS_TABLE SET DATE = " + orderdate.ToString();
                    command.CommandText = commText;
                    conn.Open();
                    command.ExecuteNonQuery();
                    conn.Close();
                    TimeSpan ts = DateTime.Now - startTime;
                    Console.WriteLine("导入数据执行完成,用时："+ts.ToString()+" 秒");
                    Console.WriteLine("*************************");
                }
```
