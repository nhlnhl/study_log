# Forward vs Redirect
Sometimes, we need to move a Servlet request to another URL.  
There are two ways to do so in Java.
1. Forward
```
request.getRequestDispatcher("www.example.com").forward(request, response);
```
You can use forward() method implemented in javax.servlet.RequestDispatcher class.  
In this way, the request and response will be shared along with all the information a requester has sent.  
But the requester won't be able to know which URL he or she is looking at.
2. Redirect
```
respond.sendRedirect("www.example.com");
```
This sendRedirect() method leads the requester to move on.  
The requester will send a new connection request to the given URL and previous information will be forgotten.