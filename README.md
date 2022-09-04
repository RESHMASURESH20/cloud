Cloud Kitchen


Case Study

Application to order Takeaway food

The purpose of this project is to cover:


-Ordering of takeaway food from a restaurant
-Order and cancel of food 
-Manage order (Sales )
-Manage order(Customer)



Frontend

-login page
-Admin login - Admin Home page
		      -Order history
		      -Available Products
	  	      -Add products
		      -Edit products and delete products
-Customer login - Customer Home page
			   - Product page
			   - Customer Order history
			   - Make Order
 
Backend
		- Microservices
				-UserService - Details of user and authentication of user
				-AdminService-Inventory management
				-CartService - Managing of cart 
				-OrderService-Managing of orders
		- Kafka Calling : (Clear of cart after successful placement of order)
		- Redis : Used as cache memory for cart and inventory
		-Database
				-Postgres 
					- User Details
					- Inventory
				-MongoDb
					-Order Details
				-Redis
					-Cart Details

Procedural Steps to start the Application:

 	-Backend
		-Base Endpoints
				-http://localhost:8084 - User 
				-http://localhost:8888/admin -Inventory
				-http://localhost:8898/cart - card
				-http://localhost:8889/orders-Orders


	-cd Cloud Kitchen
			- Step 1 ( Create database in Postgres )
				-- run ```psql postgres```
		                 - create database user
		                 - create database inventory
			-Step 2 (Start Services)
				- run ```brew start kafka```
				- run ```brew start zookeeper```
				- run ```brew start postgres```
				-run  ```brew start mongodb-community@4.4```
				-run ```brew start redis```

			- Step 3 ( Run MicroServices in intelij)
	 			- open each services in intelij
				- then run the services

			-Step 4 (Add Mock data)
					
				-Login as admin:
							-username: Cloudkitchen
							-password: cloudkitchen
				-Add mock data:



