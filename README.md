# laravel-dompdf
- install laravel ด้วยคำสั่ง composer create-project laravel/laravel laravel-dompdf
  
  ![image](https://github.com/5735512061/laravel-dompdf/assets/28274931/6b468ebf-247e-4fcd-96b3-a13513133868)

- ใช้คำสั่ง composer require barryvdh/laravel-dompdf ในการ install laravel-dompdf
  
  ![image](https://github.com/5735512061/laravel-dompdf/assets/28274931/9f799659-222f-4412-b9de-0cbe501b5fac)

- เพิ่ม Barryvdh\DomPDF\ServiceProvider::class ส่วนของ providers ในไฟล์ config/app.php
- และเพิ่ม 'PDF' => Barryvdh\DomPDF\Facade::class ส่วนของ aliases ในไฟล์ config/app.php
- ใช้คำสั่ง php artisan make:controller PDFController เพื่อสร้าง controller PDFController
  
  ![image](https://github.com/5735512061/laravel-dompdf/assets/28274931/43160a2f-0839-40fc-b885-ecd19b1bedbd)

  
- เพิ่ม use App\Http\Controllers\PDFController; และ  Route::get('/dom-pdf', [PDFController::class, 'domPDF']); ในส่วนของ routes/web.php
- เขียนในส่วนของฟังก์ชันใน Controller PDFController
  
  ![image](https://github.com/5735512061/laravel-dompdf/assets/28274931/f75c2ab6-56be-4d5a-b364-4f30cebe7c3e)

- แสดงข้อมูลที่ View เข้าไปที่ resources/views สร้างไฟล์สำหรับแสดงข้อมูล dom_pdf.blade.php
