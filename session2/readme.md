<h3>مواردی که در این جلسه آموزش داده می شود</h3>
<ul>
  <li>افزودن اپ books به setting.py در پوشه config</li>
  <li>تصحیح urls.py در پوشه config</li>
  <li>ساخت urls.py در اپ books</li>
  <li>اصلاح فایل views.py</li>
  <li>ساخت یک فایل html ساده برای homepage</li>
</ul>
<h3>افزودن اپ books به setting.py در پوشه config</h3>
<p>در ابتدا باید app ساخته شده را به جنگو بشناسانیم بنابراین وارد پوشه config میشویم و سپس وارد فایل settings.py میشویم و در قسمت INSTALLED_APPS میتوانیم app ساخته شده ی خود را مطابق زیر اضافه نماییم</p>
<p>
  INSTALLED_APPS = [ <br>
    'django.contrib.admin',<br>
    'django.contrib.auth',<br>
    'django.contrib.contenttypes',<br>
    'django.contrib.sessions',<br>
    'django.contrib.messages',<br>
    'django.contrib.staticfiles',<br>
    'books',<br>
    
]
</p>
<h3>تصحیح urls.py در پوشه config</h3>
<p>
حال میخواهیم اولین url سایت خود را بسازیم. برای اینکار باید وارد پوشه config و سپس وارد urls.py شویم. در اینجا include را import میکنیم و در قسمت path مسیر جدید را وارد می کنیم.
این کار را مطابق زیر انجام می دهیم. (url بخش ادمین خودکار در این فایل موجود بوده است)
</p>
<p>
  from django.contrib import admin<br>
from django.urls import path,include<br>

urlpatterns = [<br>
    path('admin/', admin.site.urls),<br>
    path('books',include("books.urls"))<br>
]
</p>
