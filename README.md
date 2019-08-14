# Movie Ticket Booking Mini Project

## Important Functionalities in Project
1. Register
```java
  String email=request.getParameter("ei");
			String pw=request.getParameter("pw");
			HttpSession session=request.getSession();
			//session.setAttribute("login",null);
			int flag=0;
			Connection con=null;
			Statement st=null;
			ResultSet rs=null;
			//HttpSession session=request.getSession();
			PreparedStatement pr=null;
			try
			{
				Class.forName("com.mysql.jdbc.Driver");
				con=DriverManager.getConnection("jdbc:mysql://localhost/moviedb?"+"user=root&password=root");
				System.out.println("After Connection");
				st=con.createStatement();
				rs=st.executeQuery("Select * from customer");
				while(rs.next())
				{
					//System.out.println(rs.getString(1)+rs.getString(3)+email+pw);
					if(rs.getString(1).equals(email) && rs.getString(3).equals(pw))
					{
						session.setAttribute("login",email);
						flag=1;
						response.sendRedirect("home.jsp");
						break;
					}				
				}
				if(flag==0)
				{
					response.sendRedirect("loginfail.jsp");
				}
				
			}
			catch(Exception e)
			{
				System.out.println(e);
			}
			
		}
```
1. Login
1. Form Validation
1. Booking
1. Add New Shows

## Interface

> Login Page

[<img src="https://firebasestorage.googleapis.com/v0/b/tixflix-18877.appspot.com/o/login.png?alt=media&token=831c4df3-3495-434f-bd1b-362f8cb3e399" alt="Login" />](https://console.firebase.google.com)

> Register Page

[<img src="https://firebasestorage.googleapis.com/v0/b/tixflix-18877.appspot.com/o/register.png?alt=media&token=1ddced00-830a-44c0-a901-3380bca23e7b" alt="Register" />](https://console.firebase.google.com)

> Latest Movies Page

[<img src="https://firebasestorage.googleapis.com/v0/b/tixflix-18877.appspot.com/o/latestmovies.png?alt=media&token=0b065382-9fa2-4e2a-8b33-a5391ccef3af" alt="Latest Movies" />](https://console.firebase.google.com)

> Booking Page

[<img src="https://firebasestorage.googleapis.com/v0/b/tixflix-18877.appspot.com/o/booking.png?alt=media&token=6c69a3fe-9120-45eb-9344-16573c1f3bba" alt="Booking" />](https://console.firebase.google.com)


## Backend
> Java

[<img src="https://cdn.worldvectorlogo.com/logos/java-4.svg" alt="HTML" width="100px;" />](https://worldvectorlogo.com/logo/java-4)

> MySql

[<img src="https://cdn.worldvectorlogo.com/logos/mysql.svg" alt="HTML" width="100px;" />](https://worldvectorlogo.com/logo/mysql)


## Frontend
> HTML

[<img src="https://cdn.worldvectorlogo.com/logos/html5.svg" alt="HTML" width="100px;" />](https://worldvectorlogo.com/logo/html5)

> CSS

[<img src="https://cdn.worldvectorlogo.com/logos/css-5.svg" alt="CSS" width="100px;" />](https://worldvectorlogo.com/logo/css-5)

> JavaScript

[<img src="https://cdn.worldvectorlogo.com/logos/javascript.svg" alt="JS" width="100px;" />](https://worldvectorlogo.com/logo/javascript)


## Contributors

| Name | Github |
| ----- | ------ |
| Rutvik Kulkarni | https://github.com/Rutvik2598 | 
| Rajat Marathe | https://github.com/rajatrmarathe |
| Vishal Mourya | https://github.com/weshall13 |
