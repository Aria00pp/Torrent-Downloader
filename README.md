# 🌊 Torrent Downloader via GitHub Actions

<div dir="rtl">
<br>

# 🌊 دانلودر تورنت با GitHub Actions

</div>

---

[English](#english) | [فارسی](#fa-نحوه-استفاده)

---

<h2 id="english">🇺🇸 English</h2>

### 🔁 First time? Fork this repo

GitHub Actions run on your own copy of the repository.  
👉 Click the **Fork** button (top‑right) to create your own copy.  
All downloads will be saved inside **your** fork – nothing appears in this original repo.

---

### 📦 Storage Limits (important!)

| Resource | Free Limit | How we handle it |
|----------|------------|------------------|
| **Single file max size** | ~100 MB | We split into **45 MB** parts ✅ |
| **Total repository size** | 1 GB (soft limit) | Use the **🧹 Cleaner** workflow to free space |
| **Artifacts (we don’t use)** | 500 MB | We push files directly to the repo, no artifacts |
| **Workflow run time** | 6 hours (public repo) | Large torrents may need multiple runs |

---

### 🚀 How to Use

1. **Fork** this repository (if you haven’t already).

2. **Go to the Actions tab**  
   Click the **Actions** button at the top of your forked repository.

3. **Select the workflow**  
   In the left sidebar, choose **01 - ⏬ Torrent Downloader & Split-ZIP**.

4. **Run the workflow**  
   Click the **Run workflow** dropdown on the right.  
   - **Magnet links** – paste one or more magnet links, separated by **spaces** or **new lines**.  
   - **Password** (optional) – leave blank for no encryption, or type a password to protect the ZIP files.  
   - Press the green **Run workflow** button.

5. **Wait for completion**  
   The workflow will download all torrents in parallel, split them, and push everything to the `torrents/` folder of your repo.  
   *A typical 1 GiB download takes ~10–15 minutes.*

6. **Find your files**  
   - Open the `torrents/` folder → **📥 Torrent Downloads** (master index) lists every download.  
   - Click on any folder to see its **README.md** with direct download links.

7. **Download the parts**  
   Inside each folder’s README you’ll see a table like:

   | # | File | Link |
   |---|------|------|
   | 1 | `Big Buck Bunny.z01` | [Download](https://...) |
   | 2 | `Big Buck Bunny.z02` | [Download](https://...) |

   Right‑click any link → **Save link as…** (or copy all links into a download manager like IDM).

8. **Reassemble and extract**  
   Put all parts in the same folder, then open the `.zip` file with 7‑Zip, WinRAR, or your system’s archive tool.  
   *If you set a password, you’ll be asked for it during extraction.*

---

### 🧹 How to Clean (delete all downloads)

- Go to **Actions** → **02 - 🧹 Clean Torrent Downloads**  
- Click **Run workflow** – a warning message will appear.  
- Press the green button.  
  **The entire `torrents/` folder will be permanently deleted.** No undo.  
  This frees up storage space for new downloads.

---

<br>
<br>

<h2 id="fa-نحوه-استفاده" dir="rtl">🇮🇷 فارسی</h2>
<div dir="rtl">

### 🔁 اولین بار؟ این مخزن را Fork کنید

برای استفاده از GitHub Actions باید یک نسخه شخصی از مخزن داشته باشید.  
روی دکمه **Fork** (بالا سمت راست) کلیک کنید تا یک کپی در حساب شما ایجاد شود.  
تمام فایل‌های دانلود شده در **همان مخزن Fork شده** ذخیره می‌شوند – نه در مخزن اصلی.

---

### 📦 محدودیت‌های فضای رایگان (مهم!)

| منبع | محدودیت رایگان | راه‌حل ما |
|------|-----------------|-----------|
| **حداکثر حجم هر فایل** | حدود ۱۰۰ مگابایت | فایل‌ها به بخش‌های **۴۵ مگابایتی** تقسیم می‌شوند ✅ |
| **حجم کل مخزن** | ۱ گیگابایت (هشدار دار) | با استفاده از **پاک‌کننده 🧹** فضا را آزاد کنید |
| **آرتیفکت‌ها (استفاده نمی‌کنیم)** | ۵۰۰ مگابایت | فایل‌ها مستقیماً روی مخزن ذخیره می‌شوند |
| **زمان اجرای workflow** | ۶ ساعت (مخزن عمومی) | فایل‌های خیلی بزرگ ممکن است به چند بار اجرا نیاز داشته باشند |

---

### 🚀 نحوه استفاده

1. از این مخزن **Fork** بگیرید (اگر قبلاً نگرفته‌اید).

2. به برگه **Actions** در مخزن Fork شده بروید.

3. از نوار کناری **01 - ⏬ Torrent Downloader & Split-ZIP** را انتخاب کنید.

4. روی **Run workflow** کلیک کنید:
   - در قسمت **Magnet links** یک یا چند لینک مگنت را با **فاصله** یا **خط جدید** وارد کنید.
   - در قسمت **Password** (اختیاری) می‌توانید یک رمز عبور برای فایل‌های ZIP تعیین کنید.
   - دکمه سبز **Run workflow** را بزنید.

5. منتظر بمانید تا دانلود و پردازش تمام شود.  
   *یک فایل ۱ گیگابایتی معمولاً ۱۰ تا ۱۵ دقیقه طول می‌کشد.*

6. به شاخه `torrents/` بروید:
   - فایل **📥 Torrent Downloads** (README اصلی) فهرست همه دانلودها را نشان می‌دهد.
   - روی هر پوشه کلیک کنید تا فایل README اختصاصی آن را با لینک‌های دانلود ببینید.

7. در README هر پوشه لینک‌های مستقیم هر بخش را می‌بینید:
   | # | فایل | لینک |
   |---|------|------|
   | 1 | `Big Buck Bunny.z01` | [Download](https://...) |
   | 2 | `Big Buck Bunny.z02` | [Download](https://...) |

   روی هر لینک راست‌کلیک کرده و **Save link as…** را بزنید (یا همه لینک‌ها را به یک نرم‌افزار مدیریت دانلود بدهید).

8. **باز کردن فایل ZIP چندبخشی:**
   همه بخش‌ها را در یک پوشه قرار دهید، سپس فایل `.zip` را با 7‑Zip, WinRAR یا ابزار مشابه باز کنید.  
   اگر رمز گذاشته‌اید، هنگام استخراج از شما خواسته می‌شود.

---

### 🧹 پاک کردن همه دانلودها

- به **Actions** → **02 - 🧹 Clean Torrent Downloads** بروید.
- روی **Run workflow** کلیک کنید. یک هشدار نمایش داده می‌شود.
- دکمه سبز را بزنید.  
  **کل پوشه `torrents/` برای همیشه حذف می‌شود.** بازگشت ندارد.  
  با این کار فضای مخزن شما آزاد می‌شود.

</div>
