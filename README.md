# jwtblog PHP API Task Solution 


## Requirements
This project built using **laravel 8.0**, so your php version must be >= **8.0**


## Using JWT for api authentication


## Installation
1. Clone the source code. `git clone https://github.com/embabby/jwtblog.git`
2. Go to inside the project. `cd jwtblog`
3. Run `composer install` to install all the dependencies.
4. Copy configrations file. `cp .env.example .env`
5. Create a new database.
6. Open .env file and set database configrations
```php
      DB_DATABASE= YOUR_DATABASE_NAME_HERE
      DB_USERNAME= YOUR_USERNAME_HERE
      DB_PASSWORD= YOUR_PASSWORD_HERE
```
7. Migrate and Seed the tables `php artisan migrate --seed`   
   - seed command will creates one user in your database (check UserSeeder.php file)  
   - user credentials is [`email` => `test@user.user` , `password` => `testuser`]

8. Run those commands needed to Run (VERY IMPORTANT STEP):  
        `php artisan key:generate`  
	`php artisan jwt:secret` 
	`php artisan optimize`  
	

9. Run the project! `php artisan serve`
10. Run /api/login and pass email and password 
11. This api will respond by a JWT token, use it through your session and pass it in header section to authenticate this user {Authorization = Bearer $generated_JWT }
12. Then try to hit post api CRUD (create, update, and delete)
13. DO NOT forget to put the generated token in the Headers section with key 'Authorization' and value `Bearer (generated token)`
14. Useful commands i think you may need it  
	- `php artisan optimize`  
	- `php artisan key:generate`  


