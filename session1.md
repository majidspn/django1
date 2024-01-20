<html>
<head>
    <script>
    function myFunction(text) {
        navigator.clipboard.writeText(text);
        var tooltip = document.getElementById(text);
        tooltip.innerHTML = `${text} کپی شد.`;
    }
      
    
    function outFunc(text) {
        var tooltip = document.getElementById(text);
        tooltip.innerHTML = "برای کپی کردن کلیک کنید";
    }
    </script>
</head>
<body>
<h3>در این جلسه چه مواردی آموزش داده میشود</h3>
<ol>
    <li>نصب و فعالسازی Django</li>
    <li>بالا آوردن Django روی liveserver</li>
    <li>ساخت نخستین پروژه Django</li>
    <li>بررسی فایل های ساخته شده توسط جنگو در پروژه ساخته شده</li>
    <li>ساخت نخستین app در Django و بررسی فایلهای ساخته شده توسط جنگو برای app ساخته شده</li>
</ol>
<h3>نصب و فعال سازی Django</h3>
<p>برای نصب جنگو با دستور زیر ابتدا باید جنگو را روی سیستم نصب کنیم</p>
<p>دستور زیر را در ترمینال تایپ کنید و enter بزنید</p>
<div class="tooltip">
    <button onclick="myFunction('185.51.200.2')" onmouseout="outFunc('185.51.200.2')">
      <span class="tooltiptext" id="185.51.200.2">برای کپی کردن کلیک کنید</span>
      pip install django
    </button>
</div>
</body>
</html>
