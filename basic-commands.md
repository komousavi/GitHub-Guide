Basic Git Commands | دستورات پایه Git

<div dir="rtl">۱. Git چیست؟

Git یک سیستم کنترل نسخه توزیع‌شده (Distributed Version Control System) است که برای ردیابی تغییرات فایل‌ها و مدیریت پروژه‌های نرم‌افزاری استفاده می‌شود.

Git به توسعه‌دهندگان امکان می‌دهد:

- تغییرات ایجادشده در کد منبع را ردیابی کنند.
- به نسخه‌های قبلی پروژه بازگردند.
- قابلیت‌های مختلف نرم‌افزار را به‌صورت مستقل توسعه دهند.
- با سایر توسعه‌دهندگان همکاری کنند.

۲. نصب Git (Installing Git)

برای شروع کار با Git، ابتدا باید آن را روی کامپیوتر خود نصب کنید.

پس از نصب، محیط Git Bash یا ترمینال را باز کرده و دستور زیر را اجرا کنید:

</div>git --version

<div dir="rtl">این دستور نسخه نصب‌شده Git را نمایش می‌دهد و به شما کمک می‌کند از نصب صحیح آن مطمئن شوید.

۳. پیکربندی Git (Configuring Git)

قبل از استفاده از Git، باید نام و آدرس ایمیل خود را تنظیم کنید. این اطلاعات برای شناسایی نویسنده هر Commit استفاده می‌شوند.

برای تنظیم نام کاربری:

</div>git config --global user.name "Your Name"

<div dir="rtl">برای تنظیم آدرس ایمیل:

</div>git config --global user.email "your@email.com"

<div dir="rtl">برای مشاهده تنظیمات انجام‌شده، دستور زیر را اجرا کنید:

</div>git config --list

<div dir="rtl">۴. ایجاد مخزن (Creating a Repository)

Repository (مخزن) محلی است که Git فایل‌های پروژه و تاریخچه تغییرات آن را ذخیره و مدیریت می‌کند.

برای ایجاد یک مخزن محلی جدید، ابتدا وارد پوشه پروژه شوید و دستور زیر را اجرا کنید:

</div>git init

<div dir="rtl">این دستور یک مخزن محلی Git در پوشه فعلی ایجاد می‌کند.

۵. بررسی وضعیت مخزن (Checking Repository Status)

برای بررسی وضعیت فعلی فایل‌ها و تغییرات پروژه از دستور زیر استفاده می‌شود:

</div>git status

<div dir="rtl">این دستور اطلاعاتی درباره وضعیت فایل‌ها نمایش می‌دهد؛ از جمله:

- فایل‌های جدیدی که هنوز تحت کنترل Git قرار نگرفته‌اند (Untracked Files).
- فایل‌هایی که تغییر کرده‌اند (Modified Files).
- فایل‌هایی که برای Commit آماده شده‌اند (Staged Files).

۶. افزودن فایل‌ها به Staging Area

قبل از ثبت تغییرات در مخزن، باید فایل‌های موردنظر را به Staging Area اضافه کنید.

Staging Area فضایی است که در آن تغییرات موردنظر برای Commit بعدی انتخاب و آماده می‌شوند.

برای افزودن یک فایل مشخص:

</div>git add filename

<div dir="rtl">به‌جای "filename" نام فایل موردنظر را قرار دهید.

برای افزودن تمام فایل‌های جدید و تغییر‌یافته:

</div>git add .

<div dir="rtl">۷. ثبت تغییرات (Committing Changes)

Commit عملیاتی است که طی آن یک تصویر از وضعیت تغییرات آماده‌شده در Staging Area در تاریخچه مخزن ذخیره می‌شود.

برای ثبت تغییرات از دستور زیر استفاده کنید:

</div>git commit -m "Your commit message"

<div dir="rtl">مثال:

</div>git commit -m "Add login page"

<div dir="rtl">پیام Commit باید کوتاه، واضح و مرتبط با تغییرات انجام‌شده باشد تا سایر اعضای تیم بتوانند به‌راحتی متوجه هدف هر تغییر شوند.

۸. مشاهده تاریخچه تغییرات (Viewing Commit History)

برای مشاهده تاریخچه Commitهای ثبت‌شده در پروژه، از دستور زیر استفاده می‌شود:

</div>git log

<div dir="rtl">برای مشاهده تاریخچه به‌صورت خلاصه‌تر:

</div>git log --oneline

<div dir="rtl">۹. دریافت یک مخزن (Cloning a Repository)

Clone به معنای ایجاد یک نسخه محلی از یک مخزن موجود است.

با استفاده از این دستور می‌توانید یک Repository موجود در GitHub را به کامپیوتر خود منتقل کنید.

ساختار دستور:

</div>git clone repository-url

<div dir="rtl">مثال:

</div>git clone https://github.com/username/project.git

<div dir="rtl">این دستور فایل‌ها و تاریخچه مخزن را از مخزن راه دور دریافت کرده و یک نسخه محلی از آن ایجاد می‌کند.

۱۰. اتصال به مخزن راه دور (Connecting to a Remote Repository)

برای اتصال یک مخزن محلی به یک مخزن راه دور (Remote Repository)، از دستور زیر استفاده می‌شود:

</div>git remote add origin repository-url

<div dir="rtl">در این دستور:

- "remote": برای مدیریت مخازن راه دور استفاده می‌شود.
- "add": یک مخزن راه دور جدید اضافه می‌کند.
- "origin": نام پیش‌فرضی است که معمولاً برای مخزن راه دور اصلی استفاده می‌شود.
- "repository-url": آدرس مخزن راه دور است.

برای مشاهده مخازن راه دور متصل‌شده:

</div>git remote -v

<div dir="rtl">۱۱. ارسال تغییرات (Pushing Changes)
Push عملیاتی است که طی آن Commitهای محلی به یک مخزن راه دور مانند GitHub ارسال می‌شوند.

ساختار دستور:

</div>git push origin branch-name

<div dir="rtl">مثال:

</div>git push origin main

<div dir="rtl">برای اولین Push یک Branch جدید، می‌توان از دستور زیر استفاده کرد:

</div>git push -u origin branch-name

<div dir="rtl">گزینه "-u" ارتباط بین Branch محلی و Branch راه دور را تنظیم می‌کند تا در دفعات بعد بتوان از دستور ساده‌تر "git push" استفاده کرد.

۱۲. دریافت و ادغام تغییرات (Pulling Changes)

Pull عملیاتی است که تغییرات موجود در مخزن راه دور را دریافت کرده و با Branch محلی فعلی ادغام می‌کند.

ساختار دستور:

</div>git pull origin branch-name

<div dir="rtl">مثال:

</div>git pull origin main

<div dir="rtl">این دستور برای هماهنگ نگه‌داشتن نسخه محلی پروژه با آخرین تغییرات سایر اعضای تیم بسیار کاربردی است.

۱۳. خلاصه دستورات (Summary)

</div>دستور| کاربرد
"git --version"| نمایش نسخه Git
"git config"| تنظیم پیکربندی Git
"git init"| ایجاد مخزن محلی
"git status"| نمایش وضعیت مخزن
"git add"| افزودن فایل‌ها به Staging Area
"git commit"| ثبت تغییرات در تاریخچه مخزن
"git log"| نمایش تاریخچه Commitها
"git clone"| دریافت یک نسخه محلی از مخزن
"git remote"| مدیریت مخازن راه دور
"git push"| ارسال Commitها به مخزن راه دور
"git pull"| دریافت و ادغام تغییرات مخزن راه دور