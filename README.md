# วิธีการติดตั้ง Create To Project (Nuxtjs+Laravel)

* [เริ่มต้นการติดตั้ง](#Setup)

* [เริ่มทำระบบ Authentication](#Authentication)


วิธีการติดตั้งผ่าน cmd สร้างไฟล์ทั้ง frontend และ backend
เปิด Command Prompt ใช้คำสั่งและเปิด vscode ผ่าน cmd

# Setup (เริ่มต้นการติดตั้ง)
## 1.สร้าง Backend
```php
laravel new backend
```

## 2.สร้าง Frontend และเปิดหน้า vscode ขึ้นมา
```php
npx create-nuxt-app frontend
cd ที่อยู่ไฟล์
code .
```

## 3. ลง Sanctum
```php
composer require laravel/sanctum
```

## 6.สร้าง Database แก้ไขไฟล์ที่ชื่อว่า .env เช่น
```php
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=thanadon
DB_USERNAME=root
DB_PASSWORD=
```

## 5.จากนั้นสร้าง Table ที่ Backend ได้เลย
  database/migrations จากนั้นพิมคำสั่ง 
```php
  php artisan migrate
```

## 6.จากนั้นเข้าไปที่โฟเดอร์ Controllers แล้วสร้างโฟลเดอร์ที่ชื่อ Auth ไว้เพื่อทำระบบ Authentication
```python
  php artisan make:controller Auth\\RegisterController
  composer require laravel/ui
  php artisan ui vue --auth
```


# Authentication (เริ่มทำระบบ สมัครสมาชิก และ เข้าสู่ระบบ)
## 1. เริ่มต้นติดตั้ง Nuxt Auth ที่บน Frontend
```vue
npm i @nuxtjs/auth-next


 modules: [
    '@nuxtjs/auth-next',
  ],

 axios: {
    baseURL:'http://localhost:8000/',
    credentials: true
  },
  
```

## 2. เข้า cd backend แล้วพิมเพื่อสร้างmodelเพิ่ม
```php
php artisan make:model Course --migration
```



