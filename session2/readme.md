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
<p>در اینجا ما بعد از اجرای برنامه روی liveserver مثلا روی پورت 8000 url ثابت 127.0.0.1:8000 را داریم که حال اگر یک /books به آن اضافه کنیم باید به سراغ books برود و urls موجود در اپ book را چک کند. بنابر این نیاز است تا در اپ books یک urls.py بسازیم</p>
<h3>ساخت urls.py در اپ books</h3>
<p>یک فایل urls.py در این پوشه ایجاد میکنیم. در اینجا ما فایل views.py را نیاز است که از همین پوشه ی books در برنامه import کنیم تا بتوانیم تابعی داشته باشیم که در آن برای اکشن خاصی در این url برنامه نویسی کنیم. بنابر این فایل urls.py در پوشه books تا به اینجای کار مطابق زیر خواهد بود</p>
<p>
  from django.contrib import admin<br>
from django.urls import path<br>
from . import views<br>

urlpatterns = [<br>
    path('',views.homepage,name="homepage")<br>
]

</p>
<p>
  در بالا اگر books را بعد از 127.0.0.1:8000 وارد کرده باشیم و دیگر چیز دیگری وارد نکنیم خود به خود ما را به تابع homepage در فایل views پاس میدهد. بنابر این نیاز است تا در views.py در همین پوشه books تابع homepage را بسازیم
</p>
<h3>اصلاح فایل views.py</h3>
<p>وارد views.py می شویم و تابع homepage را مطابق زیر می سازیم. نکته اینکه در اینجا نیاز است تا render را import کرده باشیم</p>
<p>
  from django.shortcuts import render <br>
def homepage(request):<br>
    return render(request,"home.html")<br>
</p>
