- # Database java UNIT3
	- ## Database Connect
	  collapsed:: true
		- ```
		  import java.sql.*;
		  
		  public class Connections{
		  	static String url = "jdbc:mysql://localhost:3306/dbname";
		  	static String driver = "com.mysql.jdbc.Driver";
		  	static String user = "root";
		  	static String pass = "test";
		  
		  	public static void main(String[] args){
		      	Connection conn = null;
		          try{
		          	Class.forName(driver);
		              conn = DriverManager.getConnection(url,user,pass);
		              ...
		          }catch(ClassNotFoundException e){
		          }catch(SqlException e){
		          }finally{
		          try{
		          	conn.close();
		          }
		          }
		      }
		  
		  
		  }
		  ```
	- ## Statement Execution
	  collapsed:: true
		- ## Prepared Statement
			- ```
			  
			  
			  //Prepared Statement
			  String Query = "insert into Movies values(?,?,?,?,?)";
			  PreparedStatement ps = conn.prepareStatement(Query);
			  ps.setInt(1,5);
			  ps.setString(2,"Avatar");
			  ps.setString(3,"Nicholas Cage");
			  ps.setString(4,"Movie monger");
			  ps.setString(5,"James Cameron")
			  
			  ps.executeUpdate();
			  
			  
			  
			  ```
		- ## Statement
			- ```
			  Statement st = conn.createStatement();
			  
			  st.executeUpdate("Insert Into Student (name,phone,email) values('"+name+"','"+phone+"','"+email+"')" ");
			  st.executeQuery("Select * from Students");
			  
			  
			  ```
	- ## DRIVER TYPES
	  collapsed:: true
		- Type 1: Java JDBC-ODBC driver
			- Advantage
				- easy to use
				- can be easily connected to any database
			- Disadvantage
				- degraded performance because JDBC call is converted to ODBC function call
				- the ODBC driver has to be installed on the client machine
				- Platform dependent
		- Type 2: Native API / Partly Driver / Native Driver
			- Advantage
				- Better performance compared to JDBC-ODBC
			- Disadvantage
				- need to install Native Driver on client machine
				- vendor library needs to be installed
				- platform and vendor dependent
		- Type 3: Java Net Protocol / Network Protocol Driver
			- Client side library is not required
			-
		- Type 4:  Pure Java / Thin Driver
		-
- JSP UNIT 5