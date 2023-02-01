# xray for PaaS

نکات: برای ایجاد یک مخزن خصوصی بر اساس مخزن اصلی روی "Use this template" کلیک کنید

![image](https://user-images.githubusercontent.com/122191366/212063458-2def0e1a-805a-4451-ae62-324b67abee47.png)

## ویژگی های پروژه
* این پروژه برای استقرار xray در هر ارائه دهنده سرویس ابری PaaS استفاده می شود و راه حل اتخاذ شده Nginx + WebSocket + VMess/Vless/Trojan + TLS است.
* فایل هسته xray و فایل پیکربندی "به صورت ویژه پردازش شده است"، هر پروژه متفاوت است، که خطر مسدود شدن را تا حد زیادی کاهش می دهد.
* مقادیر uuid در vmess و vless یا رمز عبور تروجان و شدوساکس را می توان سفارشی کرد یا از مقادیر پیش فرض استفاده کرد.
* کاوشگر Nezha یکپارچه، می توانید آزادانه انتخاب کنید که آن را نصب کنید.
* پس از تکمیل استقرار، اگر متوجه شدید که نمی توانید به اینترنت دسترسی داشته باشید، لطفاً بررسی کنید که آیا آدرس دامنه مسدود شده است یا خیر. می توانید از Cloudflare CDN یا worker برای حل آن استفاده کنید.

## استقرار

* در یکی از ارائه دهنده خدمات ابری PaaS ثبت نام کنید.
* با توجه به ارائه دهنده خدمات ابری PaaS، حساب github خود را متصل کنید یا از اقدامات ارائه شده توسط پروژه برای تولید یک DockerHub image استفاده کنید. استفاده از کتابخانه کوچک + خصوصی به شدت توصیه می شود.
* متغیرهای موجود در پروژه
  | نام متغیر | لزوم | پیش فرض ها | Remark |
  | ------------ | ------ | ------ | ------ |
  | UUID         | نه | de04add9-5c68-8bab-950c-08cd5320df18 | می توان به صورت آنلاین تولید کرد https://www.uuidgenerator.net/ |
  | VMESS_WSPATH | نه | /vmess | شروع با /|
  | VLESS_WSPATH | نه | /vless | شروع با / |
  | TROJAN_WSPATH | نه | /trojan | شروع با / |
  | SS_WSPATH | نه | /shadowsocks | شروع با / |
  | NEZHA_SERVER | نه |        |سرور IP یا نام دامنه Nezha probe  |
  | NEZHA_PORT   | نه |        | پورت سرور Nezha Probe  |
  | NEZHA_KEY    | نه |        |کلید اختصاصی کلاینت Nezha Probe |

* متغیرهای مورد استفاده توسط GitHub Actions

  | نام متغیر | Remark |
  | ------------- | -------------- |
  |DOCKER_USERNAME|Docker Hub نام کاربری|
  |DOCKER_PASSWORD|Docker Hub کلمه عبور|

![image](https://user-images.githubusercontent.com/116990986/211692321-34df154a-320a-448f-9abe-2efab9c53550.png)

## با تشکر از

پروژه v2ray از ifeng：https://github.com/hiifeng

## سلب مسئولیت

* این برنامه فقط برای یادگیری و درک است. برای اهداف غیرانتفاعی لطفاً ظرف 24 ساعت پس از دانلود آن را حذف کنید. برای هیچ هدف تجاری قابل استفاده نیست. متن، داده ها و تصاویر همگی دارای حق چاپ هستند. در صورت کپی برداری، منبع باید ذکر شود. 
* استفاده از این برنامه منوط به سلب مسئولیت استقرار است. استفاده از این برنامه باید با قوانین و مقررات مکانی که سرور استقرار در آن قرار دارد، کشوری که کاربر در آن قرار دارد و کشوری که کاربر در آن قرار دارد مطابقت داشته باشد. نویسنده برنامه هیچ مسئولیتی در قبال رفتار نادرست کاربر ندارد. 

## حمایت

Misaka：https://afdian.net/a/Misaka-blog

![afdian-MisakaNo の 小破站](https://user-images.githubusercontent.com/122191366/211533469-351009fb-9ae8-4601-992a-abbf54665b68.jpg)