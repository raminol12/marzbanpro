<p align="center">
  <a href="https://github.com/raminol12/marzbanpro" target="_blank" rel="noopener noreferrer">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://github.com/raminol12/marzbanpro/blob/main/photo_2025-04-11_02-12-22.jpg">
      <img width="680" height="500" src="https://github.com/raminol12/marzbanpro/blob/main/photo_2025-04-11_02-12-22.jpg">
    </picture>
  </a>
</p>
<h1 align="center"/>قالب سابسکریپشن برای پنل  <a href="https://github.com/Gozargah/Marzban">مرزبان</a></h1>

## فهرست مطالب
- [ویژگی‌ ها](#ویژگی-ها)
- [مراحل نصب](#مراحل-نصب)

# مقدمه
یک قالب html ساده برای نمایش بهتر اطلاعات کاربر

# ویژگی ها
- افزودن سریع لینک سابسکریپشن به برنامه های v2rayNG، NekoBox و sing-box
- لینک دانلود اپلیکیشن های مورد نیاز

# مراحل نصب
1. دانلود فایل template
```sh
sudo wget -N -P /var/lib/marzban/templates/subscription/ https://raw.githubusercontent.com/raminol12/marzbanpro/refs/heads/main/index.html
```

2. دستورات زیر رو تو ترمینال سرورتون بزنید:
```sh
echo 'CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"' | sudo tee -a /opt/marzban/.env
echo 'SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"' | sudo tee -a /opt/marzban/.env
```
یا مقادیر زیر رو در فایل `.env` در پوشه `/opt/marzban` قرار بدین
```sh
CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"
SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"
```

3. ری استارت مرزبان
```sh
marzban restart
```

## بروزرسانی
برای بروزرسانی تمپلیت فقط کافیست مرحله 1 را تکرار کنید.


<a href="https://www.coffeebede.com/alexporter"><img class="img-fluid" src="https://coffeebede.ir/DashboardTemplateV2/app-assets/images/banner/default-yellow.svg" /></a>


<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>راهنمای تنظیمات قالب</title>
    <link href="https://cdn.jsdelivr.net/gh/rastikerdar/vazirmatn-font/dist/font-face.css" rel="stylesheet" type="text/css" />
    <style>
        body {
            font-family: Vazirmatn, sans-serif;
            line-height: 1.6;
            max-width: 800px;
            margin: 0 auto;
            padding: 2rem;
            background: #f5f5f5;
            color: #333;
        }

        h1, h2 {
            color: #2c3e50;
            margin-bottom: 1.5rem;
        }

        .code-block {
            background: #2c3e50;
            color: #ecf0f1;
            padding: 1rem;
            border-radius: 0.5rem;
            margin: 1rem 0;
            overflow-x: auto;
            direction: ltr;
        }

        .note {
            background: #fff3cd;
            border-right: 4px solid #ffc107;
            padding: 1rem;
            margin: 1rem 0;
            border-radius: 0.5rem;
        }

        .example {
            background: #d4edda;
            border-right: 4px solid #28a745;
            padding: 1rem;
            margin: 1rem 0;
            border-radius: 0.5rem;
        }

        .step {
            background: white;
            padding: 1.5rem;
            margin: 1rem 0;
            border-radius: 0.5rem;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }

        .step-number {
            background: #3498db;
            color: white;
            width: 30px;
            height: 30px;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            margin-left: 0.5rem;
        }
    </style>
</head>
<body>
    <h1>راهنمای تنظیمات قالب</h1>

    <div class="step">
        <h2><span class="step-number">1</span> تغییر پس‌زمینه</h2>
        <p>برای تغییر پس‌زمینه، کد زیر را در فایل CSS پیدا کرده و آدرس تصویر را تغییر دهید:</p>
        <div class="code-block">
body {
    background: url('https://i.imgur.com/example.jpg') center/cover no-repeat fixed;
}
        </div>
        <div class="note">
            <strong>نکات مهم:</strong>
            <ul>
                <li>آدرس تصویر باید با https:// شروع شود</li>
                <li>تصویر باید با کیفیت بالا باشد</li>
                <li>اندازه پیشنهادی: حداقل 1920x1080 پیکسل</li>
                <li>فرمت‌های پیشنهادی: JPG یا PNG</li>
            </ul>
        </div>
    </div>

    <div class="step">
        <h2><span class="step-number">2</span> تغییر لوگو فروشنده</h2>
        <p>برای تغییر لوگو، کد زیر را در فایل HTML پیدا کرده و آدرس تصویر را تغییر دهید:</p>
        <div class="code-block">
&lt;div class="seller-logo"&gt;
    &lt;img src="https://example.com/seller-logo.png" alt="Seller Logo"&gt;
&lt;/div&gt;
        </div>
        <div class="note">
            <strong>نکات مهم:</strong>
            <ul>
                <li>آدرس تصویر باید با https:// شروع شود</li>
                <li>لوگو باید با پس‌زمینه شفاف باشد</li>
                <li>اندازه پیشنهادی: 200x200 پیکسل</li>
                <li>فرمت‌های پیشنهادی: PNG یا SVG</li>
            </ul>
        </div>
    </div>

    <div class="step">
        <h2><span class="step-number">3</span> تغییر اطلاعات پشتیبانی</h2>
        <p>برای تغییر اطلاعات پشتیبانی، کدهای زیر را در فایل HTML پیدا کرده و مقادیر را تغییر دهید:</p>
        <div class="code-block">
&lt;div class="support-icons"&gt;
    &lt;a href="https://wa.me/your-whatsapp-number" class="support-icon whatsapp" target="_blank"&gt;
        &lt;img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg" alt="WhatsApp"&gt;
        &lt;span class="support-tooltip"&gt;پشتیبانی واتساپ&lt;/span&gt;
    &lt;/a&gt;
    &lt;a href="https://t.me/your-telegram-username" class="support-icon telegram" target="_blank"&gt;
        &lt;img src="https://upload.wikimedia.org/wikipedia/commons/8/82/Telegram_logo.svg" alt="Telegram"&gt;
        &lt;span class="support-tooltip"&gt;پشتیبانی تلگرام&lt;/span&gt;
    &lt;/a&gt;
&lt;/div&gt;
        </div>
        <div class="note">
            <strong>نکات مهم:</strong>
            <ul>
                <li>your-whatsapp-number را با شماره واتساپ خود جایگزین کنید (با کد کشور و بدون +)</li>
                <li>your-telegram-username را با یوزرنیم تلگرام خود جایگزین کنید</li>
                <li>متن تولتیپ‌ها را می‌توانید تغییر دهید</li>
            </ul>
        </div>
    </div>

    <div class="step">
        <h2><span class="step-number">4</span> تغییر اطلاعات شبکه‌های اجتماعی</h2>
        <p>برای تغییر اطلاعات شبکه‌های اجتماعی، کدهای زیر را در فایل HTML پیدا کرده و مقادیر را تغییر دهید:</p>
        <div class="code-block">
&lt;div class="social-icons"&gt;
    &lt;a href="https://instagram.com/your-instagram" class="social-icon instagram" target="_blank"&gt;
        &lt;img src="https://upload.wikimedia.org/wikipedia/commons/e/e7/Instagram_logo_2016.svg" alt="Instagram"&gt;
        &lt;span class="social-tooltip"&gt;صفحه اینستاگرام&lt;/span&gt;
    &lt;/a&gt;
    &lt;a href="https://t.me/your-channel" class="social-icon telegram" target="_blank"&gt;
        &lt;img src="https://upload.wikimedia.org/wikipedia/commons/8/82/Telegram_logo.svg" alt="Telegram"&gt;
        &lt;span class="social-tooltip"&gt;کانال تلگرام&lt;/span&gt;
    &lt;/a&gt;
&lt;/div&gt;
        </div>
        <div class="note">
            <strong>نکات مهم:</strong>
            <ul>
                <li>your-instagram را با نام کاربری اینستاگرام خود جایگزین کنید</li>
                <li>your-channel را با نام کانال تلگرام خود جایگزین کنید</li>
                <li>متن تولتیپ‌ها را می‌توانید تغییر دهید</li>
            </ul>
        </div>
    </div>

    <div class="step">
        <h2><span class="step-number">5</span> نکات مهم</h2>
        <div class="note">
            <ul>
                <li>لینک‌ها باید با https:// شروع شوند</li>
                <li>حتماً target="_blank" را حفظ کنید تا لینک در تب جدید باز شود</li>
                <li>کلاس‌های social-icon، support-icon و instagram/telegram را حذف نکنید</li>
                <li>آیکون‌ها از ویکی‌مدیا لود می‌شوند، می‌توانید آنها را با آیکون‌های خود جایگزین کنید</li>
                <li>برای واتساپ، شماره را با کد کشور و بدون + وارد کنید (مثال: 989123456789)</li>
                <li>برای تلگرام، از یوزرنیم یا آیدی عددی استفاده کنید</li>
            </ul>
        </div>
    </div>
</body>
</html> 

