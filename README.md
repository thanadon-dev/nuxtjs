# วิธีการติดตั้ง Create To Project (Nuxtjs+Laravel)

วิธีการติดตั้งผ่าน cmd สร้างไฟล์ทั้ง frontend และ backend
เปิด Command Prompt ใช้คำสั่งและเปิด vscode ผ่าน cmd

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

## 4.จากนั้นสร้าง Table ที่ Backend ได้เลย
  database/migrations จากนั้นพิมคำสั่ง 
```php
  php artisan migrate
```

## 5.จากนั้นเข้าไปที่โฟเดอร์ Controllers แล้วสร้างโฟลเดอร์ที่ชื่อ Auth ไว้เพื่อทำระบบ Authentication
```python
  php artisan make:controller Auth\\RegisterController
  composer require laravel/ui
  php artisan ui vue --auth
```
