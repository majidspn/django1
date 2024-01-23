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
