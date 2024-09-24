---------------------------------------register----------------------------------------
1. user ne request send ki with data
 
2. route -> user/register 

3. postRegisterRequest customer handler ne data check kiya and error bhej diya 
 
4. postRegisterRequest controler -> 
   db me save karne se pahle password to bcrypt kiya 
   data liya db me save
   token generate kiya for 3 days exp
   browser ki cookies me jwt token add kr diya 
   and response me use id send kr diya

5. user id browser pr milne ke bad /products pr get request bheja

6. product pr get request bhejne pr pahle 
   authantication check karna hai is liye middle ware pr bheja

7. auth middle pr req.cookies.jwt ko get kiya 

8. agar token nahi hai to user/login page pr bhej diya 

9. agar user hai token ko verify kiya agar token sahi nahi hai to login pr bhej diya 

10. agar token sahi hai 
    decodedToken me se userId ko nikala and req ke sath userID ko attached kr diya

11 . product.find or all product se product ko get kiya 
     res.render se prducts page ko render kiya and products or userid send kr diya
     products array ko store karge

12 . product variable ki value ko products.html me store kr lege 

---------------------------------------login----------------------------------------

11. user me get request kiya users/login -> login page pr bhej diya 

12 . username: email, password ko send kiya post method me
  
13. router pr gaya postLoginRequest controller 
    db me se user table se username se user object ko get kr liya

14. user get karne ke bad check kiya if username nahi hai true  and password nahi hai true

15. agar dono me se koi ek bhi true nahi hota hai to res.status(400) and invalided bhej diya

16 agar detail sahi hai to token create karta hoo and token cookies me set karta hoo

17 res me user id send kr deta hoo

18. get request to products

19. product pr get request bhejne pr pahle 
   authantication check karna hai is liye middle ware pr bheja

20. auth middle pr req.cookies.jwt ko get kiya 

21. agar token nahi hai to user/login page pr bhej diya 

22. agar user hai token ko verify kiya agar token sahi nahi hai to login pr bhej diya 

23. agar token sahi hai 
    decodedToken me se userId ko nikala and req ke sath userID ko attached kr diya

24 . product.find or all product se product ko get kiya 
     res.render se prducts page ko render kiya and products or userid send kr diya
     products array ko store karge

25 . product variable ki value ko products.html me store kr lege 


------------------------------------------------logout------------------------------------

1. user clicked on logout btn href - users/logout
2. users/logout pr request gai 
3. getLogout controller 

------------------------------------------------add to cart------------------------------------

1. on add to cart button click action post method call - action="/cart/add"
2. add to cart verifyToken id attached to userId
3. add to cart and emit updated cart
4. View cart from aap.js route 
5. send data to cart page and userId: req.userId
6. show cart data in view cart page

------------------------------------------------plus click to add------------------------------------

1. updateQuantity method call with arrgument 1
2. request on /cart/update post method
3. verifyToken then updateCartItemQuantity
4.  

  

  


 
