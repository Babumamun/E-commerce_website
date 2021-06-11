# E-commerce_website
 A Dynamic ssm(spring,springmvc,mybatis) website, the website is about  e-commerce website, where user can buy varies kind of products and They also can search different products according to their interest.for the admin,he can add products and modify products and delete products after he log in to the website
To make this website i have to use some key knowledge such as:

JSP
Maven 
Bootstrap 
JavaScript 
JSP
Spring 
Spring mvc
MyBaits
Annotations
JDBC
CRUD
JST
Let me explain how does my project created, first for the homepage which one is the home page for an online products buyer , here i did read all the data from the database, for that i had to create a java class inside com.nsu bean package the class name is product.java this class pojo, are used for increasing the readability and re-usability of a program.To fetch data from the database and display,To do that i have used spring framework and mybatis configuration. By using pom.xml file i have downloaded all the spring mvc, mybatis, sql connector, maven dependency for my project. In the web.xml file i have define a dispatcherServlet. This dispatcherServlet will intercept all request from the server.the dispatcherServlet name is springmvc-servlet.xml. Here i have used component-scan to scan base-package and resources to mapping all the files. And used bean as well. To connect workbench to my project i created applicationContext.xml, inside this i created jdbc driver and transaction manger and sql session factory.After that i create a productMapper.xml , here i’ve connected Product class by using namespace,where i wrote all the sql statements with id then created a productDao interface to connect sql statements with id and use two annotations Repository and Mapper .Repository annotation is used to indicate that the class provides the mechanism for storage, retrieval, search, update and delete operation on objects.and mapper annotation is used by the MapStruct code generator to automatically generate a working implementation of this Java file at build-time
 Then i create service class with service annotation to  provide logic to operate on the data sent to and from the DAO and the client and autowired annotation which use to  inject the object dependency implicitly.where define the methods name is selectAll that came from productDAO interface. Then i created ProductController with Controller annotation. which allows a class to be recognized as a Spring-managed component. The @Controller annotation extends the use-case of @Component and marks the annotated class as a business or presentation layer. And requestmapping annotation which is capable of handling HTTP request methods. In the productController class i create a method call getAllProducts.here we got request from the server and then we retrieve data from the database and show it in the home.jsp page.
 then i create a method inside productController class for search any products from the website, that’s why i created sql statement in the productMapper.xml and gave id is GetByName and create a method name getByName in the ProductDAO interface and call it in the service class. And then got the user search string and pass in the Search method in the ProductController and we can see the search result in the homepage. After that i focused on admin side so that admin can modify data  for that i create a account.jsp page. Inside account.jsp page page for the validation i used two classes one for user and another for register. If both of any field is empty or didn’t fill-up the requirements then it’s shows prompt.if admin can fill the requirement for log-in .Then admin can log in to the website. If admin log-in success then admin will see a page that’s call admin.jsp, in this page i fetch all the data from the database and show it. For this i have used same method as homepage.jsp.But in the admin.jsp have some button for add products and delete products and modify products .if admin click on add button it take on the add.jsp page, here admin can add data. To add data need to create a method in the ProductController that method will call service class and from the service class it will connect to interface method new addProduct.and this addProduct nothing but an id  from the productMapper.xml when addmin click on submit then it will show added students success to do that need to create a alert.jsp. For the modify button i kept id unchanged if admin click on modify button it will take him to update.jsp page. So do update i had to create a method inside productCotroller  the method name is update.and write sql statement in productMapper.xml then connect it in the interface name ProductDAO interface from the service class need to autowired to  ProductDAO interface. then from method update called productService.update and update the database and we can see it in the homepage, To delete data and add another method inside the productCotroller class same way created sql statement then interface method and service class and then call that productService.delete method. After delete success it will take you alert.jsp page to main page.
 
 ![image](https://user-images.githubusercontent.com/62865086/121632944-bd56e280-caa3-11eb-8de2-d0240581954a.png)
 
 ![image](https://user-images.githubusercontent.com/62865086/121633011-e2e3ec00-caa3-11eb-9103-c86fe39d612f.png)
 
 ![image](https://user-images.githubusercontent.com/62865086/121633024-ea0afa00-caa3-11eb-9d75-7e0af56360c5.png
 
 ![image](https://user-images.githubusercontent.com/62865086/121633037-eecfae00-caa3-11eb-9362-086992dcdb3d.png)
 
 ![image](https://user-images.githubusercontent.com/62865086/121633068-f68f5280-caa3-11eb-9184-a88d6e345d07.png)
 
 
![image](https://user-images.githubusercontent.com/62865086/121633104-060e9b80-caa4-11eb-9f3b-65fa06ec0bce.png)



![image](https://user-images.githubusercontent.com/62865086/121633116-0ad34f80-caa4-11eb-8d23-9d155165d563.png)





                                              next part is for the admin 
                                              
![image](https://user-images.githubusercontent.com/62865086/121633221-33f3e000-caa4-11eb-9936-bd461231ad5d.png)


![image](https://user-images.githubusercontent.com/62865086/121633247-3f470b80-caa4-11eb-9b67-23786e24c433.png)




