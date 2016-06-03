+++
author = "emzi"
categories = ["لاگ"]
date = "2016-05-29T14:59:45+04:30"
description = "راه‌اندازی وبلاگ"
draft = false
featured = "2016-05-29-hello-world-again-notebook-writing-pencil-start.jpg"
featuredalt = ""
featuredpath = "/img"
linktitle = ""
title = "آغازی دوباره"
type = "post"
+++

هیجان‌زده‌ایم از این‌که اعلام می‌کنیم وبلاگ گروه کاربران گنو/لینوکس کرمان اکنون در دسترس است. این نخستین سامانهٔ انتشار محتوای سایت کرمان‌لاگ نیست، اما از آخرین پست منتشر شده با نرم‌افزار پیشین (وردپرس)، زمان زیادی می‌گذرد. پست‌های آرشیوی آن را - که گزارش فعالیت‌های گذشتهٔ لاگ کرمان است - از [این پیوند](http://web.archive.org/web/20140118203056/klug.ir) می‌توانید مرور کنید. با فاصله‌ای که از آن خاموشی گرفته‌ایم، با سلامی دوباره به دنیا آغاز می‌کنیم.

<!--more-->

پروژهٔ راه‌اندازی دوباره سایت - با هدف در اختیار داشتن امکانی برای اطلاع‌رسانی و بایگانی فعالیت‌های لاگ - از اسفند ۹۴ کلید خورد. برای ساختار تازهٔ آن دو بخش [خانه](/) و وبلاگ (همین‌جا) در نظر گرفته شد. خانه (ایندکس یا همان روت دامنه) از پوستهٔ [marketing](http://purecss.io/layouts/marketing/) فورک شد و اندکی پیش در انبارهٔ [kermanlug.github.io](https://github.com/kermanlug/kermanlug.github.io) قرار گرفت. برای وبلاگ سه گزینهٔ زیر را می‌توانستیم بررسی کنیم:

۱- سرویس‌های وبلاگ‌ساز مانند [blog.ir](http://blog.ir)، [بلاگر](http://blogger.com) و...<br>
۲- سامانه‌های مدیریت محتوا (CMS) مانند وردپرس، [ghost](https://ghost.org/developers) و...<br>
۳- موتورهای سازندهٔ سایت ایستا (SSG)<br>
۴- <گزینه چهارمی هم در کار بوده؟!>

گزینهٔ ۱ بررسی نشد، چون ماهیتش همان گزینهٔ ۲ است با این تفاوت که خرما بر نخیل. گزینهٔ ۲ اگر چه مرسوم است و می‌توانستیم دوباره به سراغ آن برویم، اما این‌بار برای ما مهم بود که ابزارها و سرویس‌هایی به کار گرفته شود که هزینه و بار نگه‌داری Host و تأمین امنیت آن تا جای ممکن از دوش گردانندگان آتی لاگ برداشته شود. از این رو مستقیم سراغ گزینهٔ ۳ را گرفتیم. برون‌دهٔ SSG برگه‌‌های ایستا (HTML+CSS+JS) است و هر جایی که وب‌سروری در کار باشد، می‌توان از آن‌ها میزبانی کرد، مانند:<br>

- Hostهای مرسوم (اشتراکی و VPS)
- برخی فضاهای میزبانی فایل مانند [دراپ‌باکس](https://dropbox.com) و [Amazon S3](http://docs.aws.amazon.com/AmazonS3/latest/dev/WebsiteHosting.html)
- برخی سرویس‌های مدیریت مخزن گیت مانند [گیت‌هاب](https://pages.github.com)، [بیت‌باکت](https://bitbucket.org) (با اتصال به  [Aerobatic](https://www.aerobatic.com/)) و [گیت‌لب](http://docs.gitlab.com/ee/pages/README.html) 
- و...

امتیاز میزبانی رایگان روی گیت‌هاب و رها شدن از نگه‌داری خود نرم‌افزار سایت‌ساز ما را در استفاده از یک نرم‌افزار سازندهٔ سایت ایستا قانع کرد. اگر به سایت [Staticgen.com](http://Staticgen.com) سر بزنید، می‌بینید که چقدر دستتان در انتخاب این نوع نرم‌افزارهای سایت‌ساز باز است، گزینه‌های زیادی که در زبان‌های مختلف و با ویژگی‌ها و رویکردهای خاص خودشان توسعه یافته‌اند.

سرانجام وبلاگ با سایت‌ساز [Hugo](https://gohugo.io) و بر روی پوستهٔ [RTL'ed Future Imperfect](https://github.com/samsam-ahmadi/hugo-future-imperfect-rtl) راه‌اندازی شد و در انبارهٔ [kermanlug/blog](https://github.com/kermanlug/blog) روی گیت‌هاب میزبانی می‌شود. پست‌های وبلاگ، دست‌نوشته‌ها و ترجمه‌های اعضای لاگ است. هم‌چنین گزارشی از هر نشست لاگ به همراه محتوای ارائه‌ها/کارگاه‌ها در اینجا منتشر خواهد شد. اعضای لاگ می‌توانند [راهنمای ارسال پست](https://github.com/kermanlug/blog/blob/master/README.md#posts) را بخوانند.

اگر در کار با بخش‌های مختلف سایت با مشکلی روبرو شدید و یا پیشنهادی دارید، در بخش دیدگاه‌های پایین همین برگه، در اتاق‌های گفتگوی لاگ و یا با فرستادن رایانامه به نشانی <a href="http://www.google.com/recaptcha/mailhide/d?k=01wkQ_C7J0BJnMxcWnOoQq2g==&amp;c=8tn4Mc46pVPYj5iLdAGkww==" onclick="window.open('http://www.google.com/recaptcha/mailhide/d?k\x3d01wkQ_C7J0BJnMxcWnOoQq2g\x3d\x3d\x26c\x3d8tn4Mc46pVPYj5iLdAGkww\x3d\x3d', '', 'toolbar=0,scrollbars=0,location=0,statusbar=0,menubar=0,resizable=0,width=500,height=300'); return false;" title="نمایش این نشانی رایانامه">h...</a><i class="fa fa-at"></i>klug.ir می‌توانید مطرح کنید.