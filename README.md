# React + Vite

* npm i -D concurrently
* npm init -y && npm i json-server
* date-fns-jalali @reduxjs/toolkit react-redux axios
* "start": "json-server --watch db.json -p 9000"
* "dev": "concurrently \" vite --port 3000 \" ",

# نکته ها

- ما نمیتونیم از کلاس ها وتوابع ساختن توی ریداکس استفاده کنیم (همون کلمه کلیدی this)
  اکشن ها و استیت های ریداکس باید حاوی تنها آبجکت معمولی باشند مثل آبجکت ، آرایه و ...
  
* قانون : reducer ها هرگز نباید مقدار تصادفی محاسبه کنند.
* اگر یک اکشن نیاز داشت یک شناسه منحصر به فرد داشته باشد یا یک مقدار تصادفی همیشه این مقدار تصادفی ساخته میشه و بعد درون اکشن قرار داده میشه.

* تابع preparecallback : راهکاری برای سفارشی سازی action payload هست این تابع میتونه آرگمان های ورودی دریافت کنه و مقادیر تصادفی از جمله شناسه منحصر به فرد تولید کنه  و همچنین منطق همزمانی sync برای اینکه تصمیم گرفته شود چه مقادیری درون آبجکت action باشد درونش میتونیم بنویسیم و همچنین باید آبجکتی برگشت بده به همراه فیلد payload درونش و آبجکت برگشت داده شده میتونه حاوی فیلد meta باشد و از meta برای نوشتن مقادیر توصیفی استفاده میکنیم و همچنین میتونه حاوی فیلد ارور هم باشد.
