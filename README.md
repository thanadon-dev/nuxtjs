# วิธีการติดตั้ง Create To Project (Nuxtjs+Laravel)

วิธีการติดตั้งผ่าน cmd สร้างไฟล์ทั้ง frontend และ backend
เปิด Command Prompt ใช้คำสั่งและเปิด vscode ผ่าน cmd

1.สร้าง Backend
```java
laravel new backend
```

2.สร้าง Frontend และเปิดหน้า vscode ขึ้นมา
```java
npx create-nuxt-app frontend
cd ที่อยู่ไฟล์
code .
```

3. ลง Sanctum
```java
composer require laravel/sanctum
```

4.จากนั้นสร้าง Table ที่ Backend ได้เลย

