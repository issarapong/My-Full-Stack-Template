# My Full Stack Template

## Frontend/Backend  basic CRUD member system

-Register  
-Login  
-member  

## Project Folder Structure

📦My-Full-Stack-Template  
 ┣ 📂backend-api  
 ┣ 📂fontend-web  
 ┗ 📜users.sql  


## Global Package  Install
```
npm i -g pnpm 
```

## Backend-api Package Install
```
pnpm init 
pnpm add express
pnpm add mysql2
pnpm add sequelize
pnpm add dotenv
pnpm add cors
pnpm add -D morgan 
pnpm add helmet
pnpm add express-rate-limit
pnpm add joi
pnpm add bcryptjs
pnpm add jsonwebtoken
pnpm add multer
pnpm add cloudinary
```


```
mkdir public
mkdir public/images
mkdir src
mkdir src/constants
touch src/constants/index.js
mkdir src/controllers
touch src/controllers/auth-controller.js
touch src/controllers/user-controller.js
mkdir src/initialize
touch src/initialize/database.js
mkdir src/middlewares
touch src/middlewares/authenticate.js
touch src/middlewares/error.js
touch src/middlewares/not-found.js
mkdir src/repositories
touch src/repositories/user-repository.js
mkdir src/routes
touch src/routes/auth-route.js
touch src/routes/user-route.js
mkdir src/services
touch src/services/bcrypt-service.js
touch src/services/token-service.js
touch src/services/user-service.js
mkdir src/utils
mkdir src/utils/create-error.js
mkdir src/validators
touch src/validators/auth-validator.js
touch src/validators/validate.js
touch .env
touch app.js
touch .sequelizerc


```
```
sequelize init:models
touch src/models/user.js
sequelize init:config
mv config.json database.js
sequelize db:create
```
## Config Enviroment to .env


```
# Node and network enviroment
NODE_ENV=development
PORT=8888

# Database enviroment
DB_USERNAME=root
DB_PASSWORD=yourpassword
DB_NAME=yourdb
DB_HOST=localhost

# JWT security
HASH_SALT=12

JWT_SECRET_KEY=hvhjvjhvhhjvjvjjvj
JWT_EXPIRE_IN =15d
```



## Backend-api Folder and file Structure

📦Backend-api  
 ┣ 📂public  
 ┃ ┗ 📂images  
 ┣ 📂src  
 ┃ ┣ 📂config  
 ┃ ┃ ┣ 📜<s>cloudinary.js</s>  
 ┃ ┃ ┗ 📜database.js  
 ┃ ┣ 📂constants  
 ┃ ┃ ┗ 📜index.js  
 ┃ ┣ 📂controllers  
 ┃ ┃ ┣ 📜auth-controller.js  
 ┃ ┃ ┣ 📜<s>friend-controller.js</s>    
 ┃ ┃ ┣ 📜<s>post-controller.js</s>    
 ┃ ┃ ┣ 📜user-controller.js  
 ┃ ┣ 📂initialize  
 ┃ ┃ ┗ 📜database.js  
 ┃ ┣ 📂middlewares  
 ┃ ┃ ┣ 📜authenticate.js  
 ┃ ┃ ┣ 📜error.js  
 ┃ ┃ ┣ 📜not-found.js  
 ┃ ┃ ┗ 📜upload.js  
 ┃ ┣ 📂models  
 ┃ ┃ ┣ <s>📜comment.js</s>    
 ┃ ┃ ┣ <s>📜friend.js</s>    
 ┃ ┃ ┣ 📜index.js  
 ┃ ┃ ┣ <s>📜like.js</s>  
 ┃ ┃ ┣ <s>📜post.js</s>    
 ┃ ┃ ┗ 📜user.js  
 ┃ ┣ 📂repositories  
 ┃ ┃ ┗ 📜user-repository.js  
 ┃ ┣ 📂routes  
 ┃ ┃ ┣ 📜auth-route.js  
 ┃ ┃ ┣ <s>📜friend-route.js</s>  
 ┃ ┃ ┣ <s>📜post-route.js</s>    
 ┃ ┃ ┗ 📜user-route.js  
 ┃ ┣ 📂services  
 ┃ ┃ ┣ 📜bcrypt-service.js  
 ┃ ┃ ┣ 📜<s>friend-service.js</s>  
 ┃ ┃ ┣ 📜token-service.js  
 ┃ ┃ ┣ 📜<s>upload-service.js</s>    
 ┃ ┃ ┗ 📜user-service.js  
 ┃ ┣ 📂utils  
 ┃ ┃ ┗ 📜create-error.js  
 ┃ ┣ 📂validators  
 ┃ ┃ ┣ 📜auth-validator.js  
 ┃ ┃ ┗ 📜validate.js  
 ┃ ┗ 📜app.js  
 ┣ 📜.env  
 ┣ 📜.sequelizerc  
 ┣ 📜README.md  
 ┣ 📜package.json  
 ┗ 📜pnpm-lock.yaml  


<hr>
# Frontend
## Frontend-api Package Install

```
pnpm create vite . --template react
pnpm add axios
pnpm add react-toastify   
pnpm add react-redux @reduxjs/toolkit
pnpm add javascript-time-ago
```










## Frontend-api Folder and file Structure

```
📦Frontend-web
 ┣ 📂public
 ┃ ┗ 📜vite.svg
 ┣ 📂src
 ┃ ┣ 📂api
 ┃ ┃ ┣ 📜auth-api.js
 ┃ ┃ ┣ 📜axios.js
 ┃ ┃ ┣ 📜friend-api.js
 ┃ ┃ ┗ 📜user-api.js
 ┃ ┣ 📂assets
 ┃ ┃ ┣ 📜blank.png
 ┃ ┃ ┗ 📜cover.jpg
 ┃ ┣ 📂components
 ┃ ┃ ┣ 📜Avatar.jsx
 ┃ ┃ ┣ 📜Loading.jsx
 ┃ ┃ ┗ 📜Modal.jsx
 ┃ ┣ 📂config
 ┃ ┃ ┗ 📜env.js
 ┃ ┣ 📂features
 ┃ ┃ ┣ 📂auth
 ┃ ┃ ┃ ┣ 📂components
 ┃ ┃ ┃ ┃ ┣ 📜LoginForm.jsx
 ┃ ┃ ┃ ┃ ┣ 📜LoginInput.jsx
 ┃ ┃ ┃ ┃ ┣ 📜ProtectedRoute.jsx
 ┃ ┃ ┃ ┃ ┣ 📜RedirectIfAuthenticated.jsx
 ┃ ┃ ┃ ┃ ┣ 📜RegisterContainer.jsx
 ┃ ┃ ┃ ┃ ┣ 📜RegisterForm.jsx
 ┃ ┃ ┃ ┃ ┣ 📜RegisterInput.jsx
 ┃ ┃ ┃ ┃ ┗ 📜inputErrorMessage.jsx
 ┃ ┃ ┃ ┣ 📂slice
 ┃ ┃ ┃ ┃ ┗ 📜auth-slice.js
 ┃ ┃ ┃ ┗ 📂validators
 ┃ ┃ ┃ ┃ ┣ 📜validate-login.js
 ┃ ┃ ┃ ┃ ┗ 📜validate-register.js
 ┃ ┃ ┣ 📂post
 ┃ ┃ ┃ ┣ 📂components
 ┃ ┃ ┃ ┃ ┣ 📜CreatePostBox.jsx
 ┃ ┃ ┃ ┃ ┣ 📜Post.jsx
 ┃ ┃ ┃ ┃ ┣ 📜PostContainer.jsx
 ┃ ┃ ┃ ┃ ┣ 📜PostContainer_nowok.jsx
 ┃ ┃ ┃ ┃ ┣ 📜PostFooter.jsx
 ┃ ┃ ┃ ┃ ┣ 📜PostForm.jsx
 ┃ ┃ ┃ ┃ ┣ 📜PostHeader.jsx
 ┃ ┃ ┃ ┃ ┗ 📜PostList.jsx
 ┃ ┃ ┗ 📂profile
 ┃ ┃ ┃ ┣ 📂components
 ┃ ┃ ┃ ┃ ┣ 📜CoverImage.jsx
 ┃ ┃ ┃ ┃ ┣ 📜EditProfileForm.jsx
 ┃ ┃ ┃ ┃ ┣ 📜FormButton.jsx
 ┃ ┃ ┃ ┃ ┣ 📜FriendAction.jsx
 ┃ ┃ ┃ ┃ ┣ 📜MeAction.jsx
 ┃ ┃ ┃ ┃ ┣ 📜PictureForm.jsx
 ┃ ┃ ┃ ┃ ┣ 📜ProfileContainer.jsx
 ┃ ┃ ┃ ┃ ┣ 📜ProfileInfo.jsx
 ┃ ┃ ┃ ┃ ┣ 📜ProfileWrapper.jsx
 ┃ ┃ ┃ ┃ ┣ 📜ReceiverAction.jsx
 ┃ ┃ ┃ ┃ ┣ 📜RequesterAction.jsx
 ┃ ┃ ┃ ┃ ┗ 📜UnknownAction.jsx
 ┃ ┃ ┃ ┣ 📂context
 ┃ ┃ ┃ ┃ ┗ 📜ProfileContextProvider.jsx
 ┃ ┃ ┃ ┗ 📂hooks
 ┃ ┃ ┃ ┃ ┗ 📜useProfile.js
 ┃ ┣ 📂hooks
 ┃ ┃ ┗ 📜useForm.js
 ┃ ┣ 📂icons
 ┃ ┃ ┗ 📜index.jsx
 ┃ ┣ 📂layouts
 ┃ ┃ ┣ 📜Container.jsx
 ┃ ┃ ┣ 📜Dropdown.jsx
 ┃ ┃ ┣ 📜Header.jsx
 ┃ ┃ ┣ 📜Menu.jsx
 ┃ ┃ ┗ 📜MenuItem.jsx
 ┃ ┣ 📂pages
 ┃ ┃ ┣ 📜FriendPage.jsx
 ┃ ┃ ┣ 📜HomePage.jsx
 ┃ ┃ ┣ 📜LoginPage.jsx
 ┃ ┃ ┗ 📜ProfilePage.jsx
 ┃ ┣ 📂route
 ┃ ┃ ┗ 📜Router.jsx
 ┃ ┣ 📂store
 ┃ ┃ ┗ 📜index.js
 ┃ ┣ 📂utils
 ┃ ┃ ┣ 📜create-classes.js
 ┃ ┃ ┣ 📜localstorage.js
 ┃ ┃ ┗ 📜timeago.js
 ┃ ┣ 📜App.jsx
 ┃ ┣ 📜index.css
 ┃ ┗ 📜main.jsx
 ┣ 📜.eslintrc.cjs
 ┣ 📜.gitignore
 ┣ 📜README.md
 ┣ 📜index.html
 ┣ 📜package.json
 ┣ 📜pnpm-lock.yaml
 ┣ 📜postcss.config.js
 ┣ 📜tailwind.config.js
 ┗ 📜vite.config.js
 ```

## Database

### Table members/users schema


| id | first_name | last_name | email            | mobile     | password | profile_image  | cover_image    | created_at          | updateted_at        |
|----|------------|-----------|------------------|------------|----------|----------------|----------------|---------------------|---------------------|
| 1  | John       | Doe       | jonhn.d@mail.com | 0665544478 | 123456   | http://xxx.com | http://xxx.com | 2023-05-26 10:56:51 | 2023-06-01 09:08:39 |
| 2  | Jame       | Deen      | jame.d@mail.com  | 0235547789 | 123456   | http://ddd.com | http://aaa.com | 2023-05-26 10:56:51 | 2023-06-01 09:08:39 |
| 3  | Joe        | jim       | joe.j@mail.com   | 0556687749 | 123456   | http://xxx.com | http://ggg.com  | 2023-05-26 10:56:51 | 2023-06-01 09:08:39 |

## Sql Command
```
CREATE TABLE `users` (
  `id` int NOT NULL AUTO_INCREMENT,
  `first_name` varchar(255) NOT NULL,
  `last_name` varchar(255) NOT NULL,
  `email` varchar(255) DEFAULT NULL,
  `mobile` varchar(255) DEFAULT NULL,
  `password` varchar(255) NOT NULL,
  `profile_image` varchar(255) DEFAULT NULL,
  `cover_image` varchar(255) DEFAULT NULL,
  `created_at` datetime NOT NULL,
  `updated_at` datetime NOT NULL,
  PRIMARY KEY (`id`),
  UNIQUE KEY `email` (`email`),
  UNIQUE KEY `mobile` (`mobile`)
) ENGINE=InnoDB AUTO_INCREMENT=53 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
```