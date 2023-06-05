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

## Create folder and file *** Base on fackbuck project ***
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
## crete config
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
pnpm add react-router-dom
pnpm add react-hook-form
pnpm add @hookform/resolvers
pnpm add react-redux @reduxjs/toolkit
pnpm add axios
pnpm add react-toastify   
pnpm add react-redux @reduxjs/toolkit
pnpm add joi
pnpm add javascript-time-ago
pnpm add font-awesome
pnpm add daisyui
pnpm add -D tailwindcss postcss autoprefixer
pnpm exec tailwindcss init -p
```
## Create folder and file *** Base on fackbuck project ***
```
rm src/App.css
mkdir src/api
touch src/api/auth-api.js
touch src/api/axios.js
touch src/api/user-api.js
mkdir src/components
touch src/components/Avatar.jsx
touch src/components/Loading.jsx
touch src/components/Modal.jsx
mkdir src/config
touch src/config/env.js
mkdir src/features
mkdir src/features/auth
mkdir src/features/auth/components
touch src/features/auth/components/LoginForm.jsx
touch src/features/auth/components/LoginInput.jsx
touch src/features/auth/components/ProtectedRoute.jsx
touch src/features/auth/components/RedirectIfAuthenticated.jsx
touch src/features/auth/components/RegisterContainer.jsx 
touch src/features/auth/components/RegisterForm.jsx
touch src/features/auth/components/RegisterInput.jsx
touch src/features/auth/components/inputErrorMessage.jsx
mkdir src/features/auth/slice
touch src/features/auth/auth-slice.js
mkdir src/features/auth/validators
touch src/features/auth/validators/validate-login.js
touch src/features/auth/validators/validate-register.js
mkdir src/features/post
mkdir src/features/post/components
touch src/features/post/components/CreatePostBox.jsx
touch src/features/post/components/Post.jsx
touch src/features/post/components/PostContainer.jsx
touch src/features/post/components/PostFooter.jsx
touch src/features/post/components/PostForm.jsx
touch src/features/post/components/PostHeader.jsx
touch src/features/post/components/PostList.jsx
mkdir src/features/profile
mkdir src/features/profile/components
touch src/features/profile/components/CoverImage.jsx
touch src/features/profile/components/EditProfileForm.jsx
touch src/features/profile/components/FormButton.jsx
touch src/features/profile/components/FriendAction.jsx
touch src/features/profile/components/MeAction.jsx
touch src/features/profile/components/PictureForm.jsx
touch src/features/profile/components/ProfileContainer.jsx
touch src/features/profile/components/ProfileInfo.jsx
touch src/features/profile/components/ProfileWrapper.jsx
touch src/features/profile/components/ReceiverAction.jsx 
touch src/features/profile/components/RequesterAction.jsx 
touch src/features/profile/components/UnknownAction.jsx
mkdir src/features/profile/context
touch src/features/profile/context/ProfileContextProvider.jsx
mkdir src/features/profile/hooks
touch src/features/profile/hooks/useProfile.js
mkdir src/hooks
touch src/hooks/useForm.js
mkdir src/icons
touch src/icons/index.jsx
mkdir src/layouts
touch src/layouts/Container.jsx
touch src/layouts/Dropdown.jsx
touch src/layouts/Header.jsx
touch src/layouts/Menu.jsx
touch src/layouts/MenuItem.jsx
mkdir src/pages
touch src/pages/FriendPage.jsx
touch src/pages/HomePage.jsx
touch src/pages/LoginPage.jsx
touch src/pages/ProfilePage.jsx
mkdir src/route
touch src/route/Router.jsx
mkdir src/store
touch src/store/index.js
mkdir src/utils
touch src/utils/localstorage.js
touch src/utils/create-classes.js  
touch src/utils/timeago.js
```

## Frontend-api Folder and file Structure 


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