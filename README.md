
# ProvinceCity-Iran

This repository contains a simple HTML, CSS, and JavaScript project that allows users to select an Iranian province from a dropdown list and view the corresponding cities in that province.
- The important part of this repository is the JS.

## Project Overview

The project provides a simple user-friendly interface to select a province and dynamically displays the list of cities within that province. The project is built using HTML, CSS, and JavaScript and includes a custom script to manage the province-city relationships.

## Features

- Dropdown list of Iranian provinces.
- Dynamic population of cities based on the selected province.

## Getting Started

### Prerequisites

To run this project, you need a web browser that supports modern web standards.

### Installation

1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/Bardia-AA/ProvinceCity-Iran.git
   ```
2. Navigate to the project directory:
   ```bash
   cd ProvinceCity-Iran
   ```
3. Open the `index.html` file in your web browser to view the project.

## Usage

1. Open the `index.html` file in your web browser.
2. Select a province from the dropdown list.
3. The cities dropdown will be populated based on the selected province.
4. Submit the form to see the selected values.
5. Now you can use the JS for your own projects.

## Project Structure

```
ProvinceCity-Iran/
├── css/
│   ├── style/
│   │   ├── style.css
│   │   └── form.css
├── js/
│   ├── bootstrap/
│   │   └── bootstrap_5.3.0_dist.js
│   ├── CustomJS/
│   │   └── StateCity.js
├── font/
│   └── IRANSansWeb.ttf
├── index.html
└── README.md
```

---

## Database Setup

This section provides the complete SQL script to create the `States` and `Cities` tables and insert all the states and cities as per my JavaScript object. 

## Create Tables
```sql
-- Create States table
CREATE TABLE States (
    StateID INT IDENTITY(1,1) PRIMARY KEY,
    StateName NVARCHAR(255) NOT NULL
);

-- Create Cities table
CREATE TABLE Cities (
    CityID INT IDENTITY(1,1) PRIMARY KEY,
    CityName NVARCHAR(255) NOT NULL,
    StateID INT,
    FOREIGN KEY (StateID) REFERENCES States(StateID)
);
```

# Insert States
```sql
-- Inserting states into the States table
INSERT INTO States (StateName)
VALUES 
(N'تهران'), (N'اصفهان'), (N'آذربایجان شرقی'), (N'آذربایجان غربی'), (N'اردبیل'), 
(N'ایلام'), (N'بوشهر'), (N'چهارمحال و بختیاری'), (N'خراسان جنوبی'), (N'خراسان رضوی'), 
(N'خراسان شمالی'), (N'خوزستان'), (N'زنجان'), (N'سمنان'), (N'سیستان و بلوچستان'), 
(N'فارس'), (N'قزوین'), (N'قم'), (N'کردستان'), (N'کرمان'), 
(N'کرمانشاه'), (N'کهگیلویه و بویراحمد'), (N'گلستان'), (N'گیلان'), (N'لرستان'), 
(N'مازندران'), (N'مرکزی'), (N'هرمزگان'), (N'همدان'), (N'یزد'), 
(N'البرز');
```
# Insert Cities
```sql
-- Inserting cities into the Cities table
DECLARE @StateID INT;

-- Insert cities for state تهران
SELECT @StateID = StateID FROM States WHERE StateName = N'تهران';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'تهران', @StateID), (N'شهریار', @StateID), (N'ورامین', @StateID), (N'اسلامشهر', @StateID), 
(N'پردیس', @StateID), (N'پیشوا', @StateID), (N'تجریش', @StateID), (N'دماوند', @StateID), 
(N'رباط‌کریم', @StateID), (N'شمیرانات', @StateID), (N'فیروزکوه', @StateID), (N'قرچک', @StateID), 
(N'گلستان', @StateID), (N'ملارد', @StateID), (N'وحیدیه', @StateID), (N'بومهن', @StateID), 
(N'پاکدشت', @StateID), (N'فشم', @StateID), (N'شاهدشهر', @StateID), (N'قدس', @StateID), 
(N'رودهن', @StateID), (N'شهریار', @StateID), (N'ری', @StateID), (N'اسلامآباد', @StateID), 
(N'باغستان', @StateID), (N'فردوسیه', @StateID), (N'فرونآباد', @StateID), (N'آبعلی', @StateID), 
(N'احمدآبادمستوفی', @StateID), (N'ادران', @StateID), (N'ارجمند', @StateID), (N'اشتهارد', @StateID), 
(N'افسریه', @StateID), (N'الهیه', @StateID), (N'اندیشه', @StateID), (N'ایوانک', @StateID), 
(N'آبسرد', @StateID), (N'آبشناسان', @StateID), (N'باغستان', @StateID), (N'باغ‌فیض', @StateID), 
(N'برغان', @StateID), (N'بومهن', @StateID), (N'بی‌بی‌شهربانو', @StateID), (N'پرند', @StateID), 
(N'پرندک', @StateID), (N'پسقلعه', @StateID), (N'پیشوا', @StateID), (N'تاکستان', @StateID), 
(N'تهرانپارس', @StateID), (N'توپچی', @StateID), (N'جاجرود', @StateID), (N'جمشیدآباد', @StateID), 
(N'جوادآباد', @StateID), (N'چرمشهر', @StateID), (N'چترود', @StateID), (N'چهاردانگه', @StateID), 
(N'حسن‌آباد', @StateID), (N'حسین‌آباد', @StateID), (N'حصارک', @StateID), (N'حکیمیه', @StateID), 
(N'خاکعلی', @StateID), (N'خرمدشت', @StateID), (N'خلجستان', @StateID), (N'خورین', @StateID), 
(N'دربندسر', @StateID), (N'درکه', @StateID), (N'دلیجان', @StateID), (N'دهگلان', @StateID), 
(N'دودهک', @StateID), (N'دولت‌آباد', @StateID), (N'راهدارآباد', @StateID), (N'رحمت‌آباد', @StateID), 
(N'رزکان', @StateID), (N'رودهن', @StateID), (N'زایندهرود', @StateID), (N'زرندیه', @StateID), 
(N'سعیدآباد', @StateID), (N'سولقان', @StateID), (N'سیلوند', @StateID), (N'شاهین‌شهر', @StateID), 
(N'شریف‌آباد', @StateID), (N'شمشک', @StateID), (N'شهرزیبا', @StateID), (N'شهرستانک', @StateID), 
(N'شهرکاکی', @StateID), (N'شهرکرد', @StateID), (N'شهریار', @StateID), (N'صالح‌آباد', @StateID), 
(N'صباشهر', @StateID), (N'طالقان', @StateID), (N'علی‌آباد', @StateID), (N'فامنین', @StateID), 
(N'فراک', @StateID), (N'فردوسیه', @StateID), (N'فرون‌آباد', @StateID), (N'فشم', @StateID), 
(N'فیروزآباد', @StateID), (N'فیروزبهرام', @StateID), (N'قائم‌شهر', @StateID), (N'قرهک', @StateID), 
(N'قصران', @StateID), (N'قلعهنو', @StateID), (N'کهریزک', @StateID), (N'کیلان', @StateID), 
(N'گرم‌دره', @StateID), (N'گل‌بهار', @StateID), (N'گلستان', @StateID), (N'گیلاوند', @StateID), 
(N'لواسان', @StateID), (N'لواسان‌کبیر', @StateID), (N'لوسان', @StateID), (N'لولاک', @StateID), 
(N'ماه دشت', @StateID), (N'محمدآباد', @StateID), (N'مرزداران', @StateID), (N'مشکین‌دشت', @StateID), 
(N'ملارد', @StateID), (N'مهرآباد', @StateID), (N'میگون', @StateID), (N'نسیم شهر', @StateID), 
(N'نصیرآباد', @StateID), (N'نقده', @StateID), (N'نمک آبرود', @StateID), (N'نیاوران', @StateID), 
(N'واوان', @StateID), (N'ورامین', @StateID), (N'وشمگیر', @StateID), (N'وهن‌آباد', @StateID), 
(N'پارچین', @StateID), (N'پیشوا', @StateID), (N'کاج‌آباد', @StateID), (N'کن', @StateID), 
(N'چرمشهر', @StateID), (N'جاجرود', @StateID), (N'گلستان', @StateID), (N'لواسانات', @StateID), 
(N'فیروزکوه', @StateID), (N'دماوند', @StateID), (N'آبعلی', @StateID), (N'رودهن', @StateID), 
(N'طالقان', @StateID), (N'شمشک', @StateID), (N'ورامین', @StateID);

-- Insert cities for state اصفهان
SELECT @StateID = StateID FROM States WHERE StateName = N'اصفهان';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'ابريشم', @StateID), (N'ابوزيد آباد', @StateID), (N'اردستان', @StateID), 
(N'اريسمان', @StateID), (N'اژيه', @StateID), (N'اسفرجان', @StateID), 
(N'اسلام آباد', @StateID), (N'اشن', @StateID), (N'اصغر آباد', @StateID), 
(N'اصفهان', @StateID), (N'امين آباد', @StateID), (N'ايمان شهر', @StateID), 
(N'آران و بيدگل', @StateID), (N'بادرود', @StateID), (N'باغ بهادران', @StateID), 
(N'بهارستان', @StateID), (N'بوئين و مياندشت', @StateID), (N'پيربكران', @StateID), 
(N'تودشک', @StateID), (N'تيران', @StateID), (N'جعفرآباد', @StateID), 
(N'جندق', @StateID), (N'جوجيل', @StateID), (N'چادگان', @StateID), 
(N'چرمهين', @StateID), (N'چمگردان', @StateID), (N'حسن آباد', @StateID), 
(N'خالد آباد', @StateID), (N'خمينی شهر', @StateID), (N'خوانسار', @StateID), 
(N'خوانسارک', @StateID), (N'خور', @StateID), (N'خوراسگان', @StateID), 
(N'خورزوق', @StateID), (N'داران ـ فريدن', @StateID), (N'درچه پياز', @StateID), 
(N'دستگرد و برخوار', @StateID), (N'دهاقان', @StateID), (N'دهق', @StateID), 
(N'دولت آباد', @StateID), (N'ديزيچه', @StateID), (N'رزوه', @StateID), 
(N'رضوان شهر', @StateID), (N'رهنان', @StateID), (N'زاينده رود', @StateID), 
(N'زرين شهر ـ لنجان', @StateID), (N'زواره', @StateID), (N'زيار', @StateID), 
(N'زيبا شهر', @StateID), (N'سپاهان شهر', @StateID), (N'سده لنجان', @StateID), 
(N'سميرم', @StateID), (N'شاهين شهر', @StateID), (N'شهرضا', @StateID), 
(N'شهرک صنعتی مورچ', @StateID), (N'شهرک مجلسی', @StateID), 
(N'شهرک صنعتی محمودآباد', @StateID), (N'طالخونچه', @StateID), 
(N'عسگران', @StateID), (N'علويچه', @StateID), (N'غرغن', @StateID), 
(N'فرخی', @StateID), (N'فريدون شهر', @StateID), (N'فلاورجان', @StateID), 
(N'فولادشهر', @StateID), (N'فولاد مباركه', @StateID), (N'قهدريجان', @StateID), 
(N'كاشان', @StateID), (N'كليشاد و سودرجان', @StateID), (N'كمشچه', @StateID), 
(N'كوهپايه', @StateID), (N'گز', @StateID), (N'گلپايگان', @StateID), 
(N'گلدشت', @StateID), (N'گلشهر', @StateID), (N'گوگد', @StateID), 
(N'مباركه', @StateID), (N'مهاباد', @StateID), (N'مورچه خورت', @StateID), 
(N'ميمه', @StateID), (N'نائين', @StateID), (N'نجف آباد', @StateID), 
(N'نصر آباد', @StateID), (N'نطنز', @StateID), (N'نيک آباد', @StateID), 
(N'بهارستان', @StateID), (N'هرند', @StateID), (N'ورزنه', @StateID), 
(N'ورنامخواست', @StateID), (N'ویلاشهر', @StateID);

-- Insert cities for state آذربایجان شرقی
SELECT @StateID = StateID FROM States WHERE StateName = N'آذربایجان شرقی';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'تبریز', @StateID), (N'آذرشهر', @StateID), (N'بناب', @StateID), 
(N'بستان‌آباد', @StateID), (N'سراب', @StateID), (N'مرند', @StateID), 
(N'خداآفرین', @StateID), (N'جلفا', @StateID), (N'اهر', @StateID), 
(N'مراغه', @StateID), (N'میانه', @StateID), (N'شبستر', @StateID), 
(N'عجب‌شیر', @StateID), (N'اسکو', @StateID), (N'خلخال', @StateID), 
(N'کلیبر', @StateID), (N'بناب‌جدید', @StateID), (N'سراب', @StateID), 
(N'هریس', @StateID), (N'هشترود', @StateID), (N'ورزقان', @StateID), 
(N'ملکان', @StateID), (N'خسروشهر', @StateID), (N'باسمنج', @StateID), 
(N'کندوان', @StateID), (N'اذغان', @StateID), (N'سیس', @StateID), 
(N'تسوج', @StateID), (N'شرفخانه', @StateID), (N'خاروانا', @StateID), 
(N'یامچی', @StateID), (N'بخشایش', @StateID), (N'چاراویماق', @StateID), 
(N'هوراند', @StateID), (N'ایلخچی', @StateID), (N'قره‌بابا', @StateID), 
(N'خضرلو', @StateID), (N'سردرود', @StateID), (N'شربیان', @StateID), 
(N'کردکندی', @StateID), (N'گوگان', @StateID), (N'قره‌آغاج', @StateID), 
(N'صوفیان', @StateID), (N'ممقان', @StateID), (N'خامنه', @StateID), 
(N'اقمنار', @StateID), (N'ابش‌احمد', @StateID), (N'القو', @StateID), 
(N'آذرشهر', @StateID), (N'اسکو', @StateID), (N'اهر', @StateID), 
(N'بناب', @StateID), (N'تبریز', @StateID), (N'جلفا', @StateID), 
(N'خداآفرین', @StateID), (N'سراب', @StateID), (N'مراغه', @StateID), 
(N'مرند', @StateID), (N'میانه', @StateID), (N'ملکان', @StateID), 
(N'هریس', @StateID), (N'هشترود', @StateID);

-- Insert cities for state آذربایجان غربی
SELECT @StateID = StateID FROM States WHERE StateName = N'آذربایجان غربی';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'اروميه', @StateID), (N'اشنويه', @StateID), (N'ايواوغلی', @StateID), 
(N'بازرگان', @StateID), (N'بوكان', @StateID), (N'پسوه', @StateID), 
(N'پلدشت', @StateID), (N'پيرانشهر', @StateID), (N'تازه شهر', @StateID), 
(N'تكاب', @StateID), (N'چهاربرج قديم', @StateID), (N'خوی', @StateID), 
(N'ديزج', @StateID), (N'ديزجديز', @StateID), (N'ربط', @StateID), 
(N'زيوه', @StateID), (N'سردشت', @StateID), (N'سلماس', @StateID), 
(N'سيلوانا', @StateID), (N'سيلوه', @StateID), (N'سيه چشمه ـ چالدران', @StateID), 
(N'شاهين دژ', @StateID), (N'شوط', @StateID), (N'قره ضياء الدين ـ چايپاره', @StateID), 
(N'قوشچی', @StateID), (N'كشاورز (اقبال)', @StateID), (N'ماكو', @StateID), 
(N'محمد يار', @StateID), (N'محمودآباد', @StateID), (N'مهاباد', @StateID), 
(N'مياندوآب', @StateID), (N'مياوق', @StateID), (N'ميرآباد', @StateID), 
(N'نقده', @StateID), (N'نوشين شهر', @StateID);

-- Insert cities for state اردبیل
SELECT @StateID = StateID FROM States WHERE StateName = N'اردبیل';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'ابی بيگلو', @StateID), (N'اردبيل', @StateID), (N'اصلاندوز', @StateID), 
(N'بيله سوار', @StateID), (N'پارس آباد', @StateID), (N'تازه كند انگوت', @StateID), 
(N'جعفرآباد', @StateID), (N'خلخال', @StateID), (N'سرعين', @StateID), 
(N'شهرک شهيد غفاری', @StateID), (N'كلور', @StateID), (N'كوارئيم', @StateID), 
(N'گرمی', @StateID), (N'گيوی ـ كوثر', @StateID), (N'لاهرود', @StateID), 
(N'مشگين شهر', @StateID), (N'نمين', @StateID), (N'نير', @StateID), 
(N'هشتجين', @StateID);

-- Insert cities for state ایلام
SELECT @StateID = StateID FROM States WHERE StateName = N'ایلام';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'اركواز', @StateID), (N'ارمو', @StateID), (N'ايلام', @StateID), 
(N'ايوان', @StateID), (N'آبدانان', @StateID), (N'آسمان آباد', @StateID), 
(N'بدره', @StateID), (N'توحيد', @StateID), (N'چشمه شيرين', @StateID), 
(N'چوار', @StateID), (N'دره شهر', @StateID), (N'دهلران', @StateID), 
(N'سرابله ـ شيروان و چرداو', @StateID), (N'شباب', @StateID), 
(N'شهرک اسلاميه', @StateID), (N'لومار', @StateID), (N'مهران', @StateID), 
(N'موسيان', @StateID), (N'ميمه', @StateID);

-- Insert cities for state بوشهر
SELECT @StateID = StateID FROM States WHERE StateName = N'بوشهر';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'ابدان', @StateID), (N'اهرم ـ تنگستان', @StateID), (N'آباد', @StateID), 
(N'آبپخش', @StateID), (N'بادوله', @StateID), (N'برازجان ـ دشتستان', @StateID), 
(N'بردخون', @StateID), (N'بندردير', @StateID), (N'بندرديلم', @StateID), 
(N'بندرريگ', @StateID), (N'بندركنگان', @StateID), (N'بندرگناوه', @StateID), 
(N'بوشهر', @StateID), (N'تنگ ارم', @StateID), (N'جزيره خاک', @StateID), 
(N'جم', @StateID), (N'چغارک', @StateID), (N'خورموج ـ دشتی', @StateID), 
(N'دلوار', @StateID), (N'ريز', @StateID), (N'سعدآباد', @StateID), 
(N'شبانكاره', @StateID), (N'شنبه', @StateID), (N'شول', @StateID), 
(N'عالی شهر', @StateID), (N'عسلويه', @StateID), (N'كاكی', @StateID), 
(N'كلمه', @StateID), (N'نخل تقی', @StateID), (N'وحدتيه', @StateID);

-- Insert cities for state چهارمحال و بختیاری
SELECT @StateID = StateID FROM States WHERE StateName = N'چهارمحال و بختیاری';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'اردل', @StateID), (N'آلونی', @StateID), (N'باباحيدر', @StateID), 
(N'بروجن', @StateID), (N'بلداجی', @StateID), (N'بن', @StateID), 
(N'جونقان', @StateID), (N'چالشتر', @StateID), (N'چلگرد ـ كوهرنگ', @StateID), 
(N'دزک', @StateID), (N'دستنای', @StateID), (N'دشتک', @StateID), 
(N'سامان', @StateID), (N'سودجان', @StateID), (N'سورشجان', @StateID), 
(N'شلمزار ـ كيار', @StateID), (N'شهركرد', @StateID), (N'فارسان', @StateID), 
(N'فرادنبه', @StateID), (N'فرخ شهر', @StateID), (N'كیان', @StateID), 
(N'گندمان', @StateID), (N'گهرو', @StateID), (N'لردگان', @StateID), 
(N'مال خليفه', @StateID), (N'ناغان', @StateID), (N'هارونی', @StateID), 
(N'هفشجان', @StateID), (N'وردنجان', @StateID);

-- Insert cities for state خراسان جنوبی
SELECT @StateID = StateID FROM States WHERE StateName = N'خراسان جنوبی';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'ارسک', @StateID), (N'اسديه ـ درميان', @StateID), (N'آرين شهر', @StateID), 
(N'آيسک', @StateID), (N'بشرويه', @StateID), (N'بیرجند', @StateID), 
(N'حاجی آباد', @StateID), (N'خضری دشت بياض', @StateID), (N'خوسف', @StateID), 
(N'زهان', @StateID), (N'سر بیشه', @StateID), (N'سرايان', @StateID), 
(N'سه قلعه', @StateID), (N'فردوس', @StateID), (N'قائن ـ قائنات', @StateID), 
(N'گزيک', @StateID), (N'مود', @StateID), (N'نهبندان', @StateID), 
(N'نیمبلوک', @StateID);

-- Insert cities for state خراسان رضوی
SELECT @StateID = StateID FROM States WHERE StateName = N'خراسان رضوی';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'ابدال آباد', @StateID), (N'ازادوار', @StateID), (N'باجگيران', @StateID), 
(N'باخرز', @StateID), (N'باسفر', @StateID), (N'بجستان', @StateID), 
(N'بردسكن', @StateID), (N'برون', @StateID), (N'بزنگان', @StateID), 
(N'بند قرای', @StateID), (N'بيدخت', @StateID), (N'تايباد', @StateID), 
(N'تربت جام', @StateID), (N'تربت حيدريه', @StateID), (N'جغتای', @StateID), 
(N'جنگل', @StateID), (N'چمن آباد', @StateID), (N'چناران', @StateID), 
(N'خليل آباد', @StateID), (N'خواف', @StateID), (N'داورزن', @StateID), 
(N'درگز', @StateID), (N'دولت آباد ـ زاوه', @StateID), (N'رادكان', @StateID), 
(N'رشتخوار', @StateID), (N'رضويه', @StateID), (N'ريوش (كوهسرخ)', @StateID), 
(N'سبزوار', @StateID), (N'سرخس', @StateID), (N'سلطان آباد', @StateID), 
(N'سنگان', @StateID), (N'شانديز', @StateID), (N'صالح آباد', @StateID), 
(N'طرقبه ـ بينالود', @StateID), (N'طوس سفلی', @StateID), (N'فريمان', @StateID), 
(N'فيروزه ـ تخت جلگه', @StateID), (N'فيض آباد ـ مه ولات', @StateID), 
(N'قاسم آباد', @StateID), (N'قدمگاه', @StateID), (N'قوچان', @StateID), 
(N'كاخک', @StateID), (N'كاشمر', @StateID), (N'كلات', @StateID), 
(N'گلبهار', @StateID), (N'گناباد', @StateID), (N'لطف آباد', @StateID), 
(N'مشهد', @StateID), (N'مشهد ريزه', @StateID), (N'مصعبی', @StateID), 
(N'نشتيفان', @StateID), (N'نقاب ـ جوين', @StateID), (N'نيشابور', @StateID), 
(N'نيل شهر', @StateID);

-- Insert cities for state خراسان شمالی
SELECT @StateID = StateID FROM States WHERE StateName = N'خراسان شمالی';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'اسفراين', @StateID), (N'ايور', @StateID), (N'آشخانه ـ مانه و سلمقان', @StateID), 
(N'بجنورد', @StateID), (N'جاجرم', @StateID), (N'درق', @StateID), 
(N'راز', @StateID), (N'شوقان', @StateID), (N'شيروان', @StateID), 
(N'فاروج', @StateID), (N'گرمه', @StateID);

-- Insert cities for state خوزستان
SELECT @StateID = StateID FROM States WHERE StateName = N'خوزستان';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'اهواز', @StateID), (N'آبادان', @StateID), (N'امیدیه', @StateID), 
(N'اندیمشک', @StateID), (N'بهبهان', @StateID), (N'خرمشهر', @StateID), 
(N'دزفول', @StateID), (N'سربندر', @StateID), (N'شادگان', @StateID), 
(N'شوش', @StateID), (N'شوشتر', @StateID), (N'مسجدسلیمان', @StateID), 
(N'هفتگل', @StateID), (N'رامهرمز', @StateID), (N'اندیکا', @StateID), 
(N'باغملک', @StateID), (N'بندرامام', @StateID), (N'پیروزی', @StateID), 
(N'تشان', @StateID), (N'جایزان', @StateID), (N'حمیدیه', @StateID), 
(N'خانلر', @StateID), (N'درویشان', @StateID), (N'رامشیر', @StateID), 
(N'زرگان', @StateID), (N'سردشت', @StateID), (N'سماله', @StateID), 
(N'سوسنگرد', @StateID), (N'شاوور', @StateID), (N'شیبان', @StateID), 
(N'قلعه‌تل', @StateID), (N'گتوند', @StateID), (N'لالی', @StateID), 
(N'ماهشهر', @StateID), (N'مسجدسلیمان', @StateID), (N'هفتگل', @StateID), 
(N'هندیجان', @StateID), (N'ارکوازی', @StateID), (N'ایذه', @StateID), 
(N'باباهاشم', @StateID), (N'بهبهان', @StateID), (N'حمزه', @StateID), 
(N'خفاجه', @StateID), (N'دهدز', @StateID), (N'رامهرمز', @StateID), 
(N'سردشت', @StateID), (N'شویدا', @StateID), (N'صالح‌شهر', @StateID), 
(N'قصرشیرین', @StateID), (N'میداود', @StateID), (N'مینوبار', @StateID), 
(N'ویس', @StateID), (N'هفتکل', @StateID), (N'امانیه', @StateID), 
(N'بندق', @StateID), (N'پیتاوه', @StateID), (N'تنگ‌سرخ', @StateID), 
(N'جناح', @StateID), (N'چمران', @StateID), (N'خصیب', @StateID), 
(N'دوراهک', @StateID), (N'رودزرد', @StateID), (N'سلطان‌آباد', @StateID), 
(N'صیدون', @StateID), (N'قلعه‌تل', @StateID), (N'لیکک', @StateID), 
(N'ملاثانی', @StateID), (N'ویان', @StateID);

-- Insert cities for state زنجان
SELECT @StateID = StateID FROM States WHERE StateName = N'زنجان';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'آب‌بر ـ طارم', @StateID), (N'ابهر', @StateID), (N'اسفجين', @StateID), 
(N'پری', @StateID), (N'حلب', @StateID), (N'خرمدره', @StateID), 
(N'دستجرده', @StateID), (N'دندی', @StateID), (N'زرين‌آباد ـ ايجرود', @StateID), 
(N'زرين رود', @StateID), (N'زنجان', @StateID), (N'سلطانيه', @StateID), 
(N'صائين قلعه', @StateID), (N'قيدار', @StateID), (N'گرماب', @StateID), 
(N'گيلوان', @StateID), (N'ماهنشان', @StateID), (N'همايون', @StateID), 
(N'هيدج', @StateID);

-- Insert cities for state سمنان
SELECT @StateID = StateID FROM States WHERE StateName = N'سمنان';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'ارادان', @StateID), (N'اميريه', @StateID), (N'ايوانكی', @StateID), 
(N'بسطام', @StateID), (N'بيارجمند', @StateID), (N'خيرآباد', @StateID), 
(N'دامغان', @StateID), (N'درجزين', @StateID), (N'سرخه', @StateID), 
(N'سمنان', @StateID), (N'شاهرود', @StateID), (N'شهميرزاد', @StateID), 
(N'گرمسار', @StateID), (N'مجن', @StateID), (N'مهدی شهر', @StateID), 
(N'ميامی', @StateID), (N'ميغان', @StateID);

-- Insert cities for state سیستان و بلوچستان
SELECT @StateID = StateID FROM States WHERE StateName = N'سیستان و بلوچستان';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'اسپكه', @StateID), (N'ايرانشهر', @StateID), (N'بزمان', @StateID), 
(N'بمپور', @StateID), (N'بنت', @StateID), (N'بنجار', @StateID), 
(N'پسكو', @StateID), (N'تيمور آباد', @StateID), (N'جالق', @StateID), 
(N'چابهار', @StateID), (N'خاش', @StateID), (N'دوست محمد ـ هيرمند', @StateID), 
(N'راسک', @StateID), (N'زابل', @StateID), (N'زابلی', @StateID), 
(N'زاهدان', @StateID), (N'زهک', @StateID), (N'ساربوک', @StateID), 
(N'سراوان', @StateID), (N'سرباز', @StateID), (N'سنگان', @StateID), 
(N'سوران ـ سيب سوران', @StateID), (N'سيركان', @StateID), (N'فنوج', @StateID), 
(N'قصرقند', @StateID), (N'كنارک', @StateID), (N'كيتج', @StateID), 
(N'گلمورتی ـ دلگان', @StateID), (N'گوهركوه', @StateID), (N'محمدآباد', @StateID), 
(N'ميرجاوه', @StateID), (N'نصرت آباد', @StateID), (N'نگور', @StateID), 
(N'نيک شهر', @StateID), (N'هيدوچ', @StateID);

-- Insert cities for state فارس
SELECT @StateID = StateID FROM States WHERE StateName = N'فارس';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'شیراز', @StateID), (N'آباده', @StateID), (N'ارسنجان', @StateID), 
(N'استهبان', @StateID), (N'اقلید', @StateID), (N'بوانات', @StateID), 
(N'جهرم', @StateID), (N'خرامه', @StateID), (N'داراب', @StateID), 
(N'فسا', @StateID), (N'فیروزآباد', @StateID), (N'کازرون', @StateID), 
(N'لار', @StateID), (N'لامرد', @StateID), (N'مرودشت', @StateID), 
(N'ممسنی', @StateID), (N'مهر', @StateID), (N'نیریز', @StateID), 
(N'اردکان', @StateID), (N'اشکنان', @StateID), (N'اوز', @StateID), 
(N'ایزدخواست', @StateID), (N'بالاده', @StateID), (N'بنارویه', @StateID), 
(N'بوانات', @StateID), (N'جویم', @StateID), (N'حسن‌آباد', @StateID), 
(N'خنج', @StateID), (N'داریان', @StateID), (N'رونیز', @StateID), 
(N'زرقان', @StateID), (N'سپیدان', @StateID), (N'سروستان', @StateID), 
(N'سیدان', @StateID), (N'ششده', @StateID), (N'صغاد', @StateID), 
(N'طسوج', @StateID), (N'فدامی', @StateID), (N'فسا', @StateID), 
(N'فیروزآباد', @StateID), (N'فیشور', @StateID), (N'قادرآباد', @StateID), 
(N'قائمیه', @StateID), (N'قطب‌آباد', @StateID), (N'قطرویه', @StateID), 
(N'قیر', @StateID), (N'کامفیروز', @StateID), (N'کارزین', @StateID), 
(N'کلانی', @StateID), (N'کوار', @StateID), (N'گراش', @StateID), 
(N'گویم', @StateID), (N'مبارک‌آباد', @StateID), (N'مشکان', @StateID), 
(N'مظفری', @StateID), (N'میمند', @StateID), (N'نورآباد', @StateID), 
(N'هرگان', @StateID), (N'وراوی', @StateID), (N'جهرم', @StateID), 
(N'فیروزآباد', @StateID), (N'لارستان', @StateID), (N'آباده', @StateID), 
(N'ارسنجان', @StateID), (N'استهبان', @StateID), (N'اقلید', @StateID), 
(N'بوانات', @StateID), (N'پاسارگاد', @StateID), (N'جهرم', @StateID), 
(N'خرامه', @StateID), (N'خرم‌بید', @StateID), (N'داراب', @StateID), 
(N'زرین‌دشت', @StateID), (N'سروستان', @StateID), (N'سپیدان', @StateID), 
(N'سیدان', @StateID), (N'شیراز', @StateID), (N'فسا', @StateID), 
(N'فیروزآباد', @StateID), (N'فیشور', @StateID), (N'قیر', @StateID), 
(N'کازرون', @StateID), (N'لارستان', @StateID), (N'لامرد', @StateID), 
(N'مرودشت', @StateID), (N'ممسنی', @StateID), (N'مهر', @StateID), 
(N'نی‌ریز', @StateID), (N'هرگان', @StateID);

-- Insert cities for state قزوین
SELECT @StateID = StateID FROM States WHERE StateName = N'قزوین';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'آوج', @StateID), (N'ارداق', @StateID), (N'اسفرورين', @StateID), 
(N'اقباليه', @StateID), (N'الوند', @StateID), (N'آبگرم', @StateID), 
(N'آبيک', @StateID), (N'آقابابا', @StateID), (N'بوئين زهرا', @StateID), 
(N'بیدستان', @StateID), (N'تاكستان', @StateID), (N'حصار', @StateID), 
(N'خاكعلی', @StateID), (N'خرم دشت', @StateID), (N'دانسفهان', @StateID), 
(N'سيردان', @StateID), (N'شال', @StateID), (N'شهر صنعتی البرز', @StateID), 
(N'ضياآباد', @StateID), (N'قزوين', @StateID), (N'ليا', @StateID), 
(N'محمديه', @StateID), (N'محمود آباد نمونه', @StateID), (N'معلم كلايه', @StateID), 
(N'نرجه', @StateID);

-- Insert cities for state قم
SELECT @StateID = StateID FROM States WHERE StateName = N'قم';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'دستجرد', @StateID), (N'سلفچگان', @StateID), (N'شهر جعفریه', @StateID), 
(N'قم', @StateID), (N'قنوات', @StateID), (N'كهک', @StateID);

-- Insert cities for state کردستان
SELECT @StateID = StateID FROM States WHERE StateName = N'کردستان';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'اورامانتخت', @StateID), (N'بانه', @StateID), (N'بلبان آباد', @StateID), 
(N'بيجار', @StateID), (N'دلبران', @StateID), (N'دهگلان', @StateID), 
(N'ديواندره', @StateID), (N'سروآباد', @StateID), (N'سريش آباد', @StateID), 
(N'سقز', @StateID), (N'سنندج', @StateID), (N'قروه', @StateID), 
(N'كامياران', @StateID), (N'مريوان', @StateID), (N'موچش', @StateID);

-- Insert cities for state کرمان
SELECT @StateID = StateID FROM States WHERE StateName = N'کرمان';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'اختيارآباد', @StateID), (N'ارزوئیه', @StateID), (N'امين شهر', @StateID), 
(N'انار', @StateID), (N'باغين', @StateID), (N'بافت', @StateID), 
(N'بردسير', @StateID), (N'بلوک', @StateID), (N'بم', @StateID), 
(N'بهرمان', @StateID), (N'پاريز', @StateID), (N'جواديه فلاح', @StateID), 
(N'جوشان', @StateID), (N'جيرفت', @StateID), (N'چترود', @StateID), 
(N'خانوک', @StateID), (N'دوساری', @StateID), (N'رابر', @StateID), 
(N'راور', @StateID), (N'راين', @StateID), (N'رفسنجان', @StateID), 
(N'رودبار', @StateID), (N'ريگان', @StateID), (N'زرند', @StateID), 
(N'زنگی آباد', @StateID), (N'سرچشمه', @StateID), (N'سريز', @StateID), 
(N'سيرجان', @StateID), (N'شهربابک', @StateID), (N'صفائيه', @StateID), 
(N'عنبرآباد', @StateID), (N'فارياب', @StateID), (N'فهرج', @StateID), 
(N'قلعه گنج', @StateID), (N'كاظم آباد', @StateID), (N'كرمان', @StateID), 
(N'كهنوج', @StateID), (N'كهنوج (مغزآباد)', @StateID), (N'كوهبنان', @StateID), 
(N'كيان شهر', @StateID), (N'گلباف', @StateID), (N'ماهان', @StateID), 
(N'محمدآباد ـ ريگان', @StateID), (N'محی آباد', @StateID), (N'منوجان', @StateID), 
(N'نجف شهر', @StateID), (N'نگار', @StateID);

-- Insert cities for state کرمانشاه
SELECT @StateID = StateID FROM States WHERE StateName = N'کرمانشاه';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'اسلام آباد غرب', @StateID), (N'باينگان', @StateID), (N'بيستون', @StateID), 
(N'پاوه', @StateID), (N'تازه آباد ـ ثلاث باباجانی', @StateID), (N'جوانرود', @StateID), 
(N'روانسر', @StateID), (N'ريجاب', @StateID), (N'سراب ذهاب', @StateID), 
(N'سرپل ذهاب', @StateID), (N'سنقر', @StateID), (N'صحنه', @StateID), 
(N'فرامان', @StateID), (N'فش', @StateID), (N'قصرشيرين', @StateID), 
(N'كرمانشاه', @StateID), (N'كنگاور', @StateID), (N'گيلانغرب', @StateID), 
(N'نودشه', @StateID), (N'هرسين', @StateID), (N'هلشی', @StateID);

-- Insert cities for state کهگیلویه و بویراحمد
SELECT @StateID = StateID FROM States WHERE StateName = N'کهگیلویه و بویراحمد';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'باشت', @StateID), (N'پاتاوه', @StateID), (N'چرام', @StateID), 
(N'دهدشت ـ كهگيلويه', @StateID), (N'دوگنبدان ـ گچساران', @StateID), 
(N'ديشموک', @StateID), (N'سپيدار', @StateID), (N'سوق', @StateID), 
(N'سي سخت ـ دنا', @StateID), (N'قلعه رئيسی', @StateID), (N'لنده', @StateID), 
(N'ليكک', @StateID), (N'مادوان', @StateID), (N'ياسوج', @StateID);

-- Insert cities for state گلستان
SELECT @StateID = StateID FROM States WHERE StateName = N'گلستان';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'انبار آلوم', @StateID), (N'اينچه برون', @StateID), (N'آزادشهر', @StateID), 
(N'آق قلا', @StateID), (N'بندر گز', @StateID), (N'بندر تركمن', @StateID), 
(N'جلين', @StateID), (N'خان ببين', @StateID), (N'راميان', @StateID), 
(N'سيمين شهر', @StateID), (N'علی آباد', @StateID), (N'فاضل آباد', @StateID), 
(N'كردكوی', @StateID), (N'كلاله', @StateID), (N'گاليكش', @StateID), 
(N'گرگان', @StateID), (N'گميش تپه', @StateID), (N'گنبد كاوس', @StateID), 
(N'مراوه تپه', @StateID), (N'مينودشت', @StateID);

-- Insert cities for state گیلان
SELECT @StateID = StateID FROM States WHERE StateName = N'گیلان';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'رشت', @StateID), (N'آستارا', @StateID), (N'آستانهاشرفیه', @StateID), 
(N'املش', @StateID), (N'بندرانزلی', @StateID), (N'تالش', @StateID), 
(N'رضوانشهر', @StateID), (N'رودبار', @StateID), (N'رودسر', @StateID), 
(N'سیاهکل', @StateID), (N'شفت', @StateID), (N'طوالش', @StateID), 
(N'فومن', @StateID), (N'لاهیجان', @StateID), (N'لنگرود', @StateID), 
(N'ماسال', @StateID), (N'انزلی', @StateID), (N'رودبنه', @StateID), 
(N'صومعهسرا', @StateID), (N'شاندرمن', @StateID), (N'سنگر', @StateID), 
(N'چابکسر', @StateID), (N'چمخاله', @StateID), (N'دیلمان', @StateID), 
(N'کلاچای', @StateID), (N'ماسوله', @StateID), (N'هشتپر', @StateID), 
(N'گیلدخت', @StateID), (N'لوشان', @StateID), (N'لومار', @StateID), 
(N'چاتم', @StateID), (N'چوبر', @StateID), (N'کومله', @StateID), 
(N'بیبالان', @StateID), (N'کیاشهر', @StateID), (N'توتکابن', @StateID), 
(N'رانکوه', @StateID), (N'لوندویل', @StateID), (N'صومعهسرا', @StateID), 
(N'فیروزجاه', @StateID), (N'دیناچال', @StateID), (N'لیسار', @StateID), 
(N'گورابزرمی', @StateID), (N'سیاهرود', @StateID), (N'شلمان', @StateID), 
(N'رحیمآباد', @StateID), (N'بلسبنه', @StateID), (N'خشکبیجار', @StateID), 
(N'خمام', @StateID), (N'کپورچال', @StateID), (N'لولمان', @StateID), 
(N'لشتنشاء', @StateID), (N'منجیل', @StateID), (N'سرخرود', @StateID), 
(N'سنگر', @StateID), (N'شیخمحله', @StateID), (N'فرحآباد', @StateID), 
(N'قاسمآباد', @StateID), (N'گفشه', @StateID), (N'لاکان', @StateID), 
(N'بازارِ جمعه', @StateID), (N'خرمآباد', @StateID), (N'رضوانشهر', @StateID), 
(N'برهسر', @StateID), (N'حویق', @StateID), (N'رستمآباد', @StateID), 
(N'رحیمآباد', @StateID), (N'رشت', @StateID), (N'خمام', @StateID), 
(N'لنگرود', @StateID), (N'لاهیجان', @StateID), (N'آستانه اشرفیه', @StateID), 
(N'آستارا', @StateID), (N'املش', @StateID), (N'تالش', @StateID), 
(N'سیاهکل', @StateID), (N'طالقان', @StateID), (N'چابکسر', @StateID), 
(N'رودسر', @StateID), (N'شفت', @StateID), (N'فومن', @StateID), 
(N'انزلی', @StateID), (N'پره سر', @StateID), (N'ماسال', @StateID), 
(N'رضوانشهر', @StateID), (N'هشتپر', @StateID), (N'کلاچای', @StateID), 
(N'رودبار', @StateID), (N'لوشان', @StateID), (N'چابکسر', @StateID), 
(N'رودبنه', @StateID), (N'صومعه سرا', @StateID), (N'چمخاله', @StateID), 
(N'شاندرمن', @StateID), (N'سنگر', @StateID), (N'دیلمان', @StateID), 
(N'ماسوله', @StateID), (N'کومله', @StateID), (N'لشت نشا', @StateID);

-- Insert cities for state لرستان
SELECT @StateID = StateID FROM States WHERE StateName = N'لرستان';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'ازنا', @StateID), (N'الشتر ـ سلسله', @StateID), (N'اليگودرز', @StateID), 
(N'برخوردار', @StateID), (N'بروجرد', @StateID), (N'پل دختر', @StateID), 
(N'تقی آباد', @StateID), (N'چغلوندی', @StateID), (N'چقابل', @StateID), 
(N'خرم آباد', @StateID), (N'دورود', @StateID), (N'زاغه', @StateID), 
(N'سپيددشت', @StateID), (N'شول آباد', @StateID), (N'كونانی', @StateID), 
(N'كوهدشت', @StateID), (N'معمولان', @StateID), (N'نورآباد ـ دلفان', @StateID), 
(N'واشيان نصيرتپه', @StateID);

-- Insert cities for state مازندران
SELECT @StateID = StateID FROM States WHERE StateName = N'مازندران';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'اسلام آباد', @StateID), (N'اميركلا', @StateID), (N'ايزدشهر', @StateID), 
(N'آمل', @StateID), (N'آهنگركلا', @StateID), (N'بابل', @StateID), 
(N'بابلسر', @StateID), (N'بلده', @StateID), (N'بهشهر', @StateID), 
(N'بهنمير', @StateID), (N'پل سفيد ـ سوادكوه', @StateID), (N'تنكابن', @StateID), 
(N'جويبار', @StateID), (N'چالوس', @StateID), (N'چمستان', @StateID), 
(N'خرم آباد', @StateID), (N'خوشرودپی', @StateID), (N'رامسر', @StateID), 
(N'رستم كلا', @StateID), (N'رويانشهر', @StateID), (N'زاغمرز', @StateID), 
(N'زرگر محله', @StateID), (N'زيرآب', @StateID), (N'سادات محله', @StateID), 
(N'ساری', @StateID), (N'سرخرود', @StateID), (N'سلمانشهر', @StateID), 
(N'سنگده', @StateID), (N'سوا', @StateID), (N'سورک', @StateID), 
(N'شيرگاه', @StateID), (N'شيرود', @StateID), (N'عباس آباد', @StateID), 
(N'فريدون كنار', @StateID), (N'قائم شهر', @StateID), (N'كلارآباد', @StateID), 
(N'كلاردشت', @StateID), (N'كيا كلا', @StateID), (N'كياسر', @StateID), 
(N'گزنک', @StateID), (N'گلوگاه', @StateID), (N'گهرباران', @StateID), 
(N'محمود آباد', @StateID), (N'مرزن آباد', @StateID), (N'مرزی كلا', @StateID), 
(N'نشتارود', @StateID), (N'نكاء', @StateID), (N'نور', @StateID), 
(N'نوشهر', @StateID);

-- Insert cities for state مرکزی
SELECT @StateID = StateID FROM States WHERE StateName = N'مرکزی';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'اراک', @StateID), (N'آستانه', @StateID), (N'آشتيان', @StateID), 
(N'تفرش', @StateID), (N'توره', @StateID), (N'جاورسيان', @StateID), 
(N'خسروبيک', @StateID), (N'خشک رود', @StateID), (N'خمين', @StateID), 
(N'خنداب', @StateID), (N'دليجان', @StateID), (N'ريحان عليا', @StateID), 
(N'زاويه', @StateID), (N'ساوه', @StateID), (N'شازند', @StateID), 
(N'شهراب', @StateID), (N'شهرک مهاجران', @StateID), (N'فرمهين', @StateID), 
(N'كميجان', @StateID), (N'مامونيه ـ زرنديه', @StateID), (N'محلات', @StateID), 
(N'ميلاجرد', @StateID), (N'هندودر', @StateID);

-- Insert cities for state هرمزگان
SELECT @StateID = StateID FROM States WHERE StateName = N'هرمزگان';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'ابوموسی', @StateID), (N'ايسين', @StateID), (N'بستک', @StateID), 
(N'بندر خمير', @StateID), (N'بندر عباس', @StateID), (N'بندر لنگه', @StateID), 
(N'بندزک كهنه', @StateID), (N'پارسيان', @StateID), (N'پدل', @StateID), 
(N'پل شرقی', @StateID), (N'تياب', @StateID), (N'جاسک', @StateID), 
(N'جزيره سيری', @StateID), (N'جزيره لاوان', @StateID), (N'جزيره هنگام', @StateID), 
(N'جزيرهلارک', @StateID), (N'جناح', @StateID), (N'چارک', @StateID), 
(N'حاجی آباد', @StateID), (N'درگهان', @StateID), (N'دشتی', @StateID), 
(N'دهبارز ـ رودان', @StateID), (N'رويدر', @StateID), (N'زيارت علی', @StateID), 
(N'سردشت ـ بشاگرد', @StateID), (N'سندرک', @StateID), (N'سيريک', @StateID), 
(N'فارغان', @StateID), (N'فين', @StateID), (N'قشم', @StateID), 
(N'كنگ', @StateID), (N'كيش', @StateID), (N'ميناب', @StateID);

-- Insert cities for state همدان
SELECT @StateID = StateID FROM States WHERE StateName = N'همدان';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'ازندريان', @StateID), (N'اسدآباد', @StateID), (N'اسلام آباد', @StateID), 
(N'بهار', @StateID), (N'پايگاه نوژه', @StateID), (N'تويسركان', @StateID), 
(N'دمق', @StateID), (N'رزن', @StateID), (N'سامن', @StateID), 
(N'سركان', @StateID), (N'شيرين سو', @StateID), (N'صالح آباد', @StateID), 
(N'فامنين', @StateID), (N'قروه درجزين', @StateID), (N'قهاوند', @StateID), 
(N'كبودرآهنگ', @StateID), (N'گيان', @StateID), (N'لالجين', @StateID), 
(N'ملاير', @StateID), (N'نهاوند', @StateID), (N'همدان', @StateID);

-- Insert cities for state یزد
SELECT @StateID = StateID FROM States WHERE StateName = N'یزد';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'ابركوه', @StateID), (N'احمدآباد', @StateID), (N'اردكان', @StateID), 
(N'بافق', @StateID), (N'بفروئيه', @StateID), (N'بهاباد', @StateID), 
(N'تفت', @StateID), (N'حميديا', @StateID), (N'زارچ', @StateID), 
(N'شاهديه', @StateID), (N'صدوق', @StateID), (N'طبس', @StateID), 
(N'عشق آباد', @StateID), (N'فراغه', @StateID), (N'مروست', @StateID), 
(N'مهريز', @StateID), (N'ميبد', @StateID), (N'نير', @StateID), 
(N'هرات ـ خاتم', @StateID), (N'يزد', @StateID);

-- Insert cities for state البرز
SELECT @StateID = StateID FROM States WHERE StateName = N'البرز';
INSERT INTO Cities (CityName, StateID) VALUES 
(N'اشتهارد', @StateID), (N'آسارا', @StateID), (N'چهارباغ', @StateID), 
(N'سيف آباد', @StateID), (N'شهرجديد هشتگرد', @StateID), (N'بالا طالقان', @StateID), 
(N'شهرک طالقان', @StateID), (N'پایین طالقان', @StateID), (N'كرج', @StateID), 
(N'كمال شهر', @StateID), (N'كوهسار ـ چندار', @StateID), (N'گرمدره', @StateID), 
(N'ماهدشت', @StateID), (N'محمدشهر', @StateID), (N'مشکين دشت', @StateID), 
(N'نظرآباد', @StateID), (N'هشتگرد ـ ساوجبلاغ', @StateID);
```

This SQL script will create the `States` and `Cities` tables, then insert all the states and their respective cities into these tables. 

# Insert AreaCodes
To add a new field for the area code to the `States` table and update it with the relevant values, you can follow these steps:

1. **Add the new column** to the `States` table.
2. **Update the new column** with the appropriate area codes.

Here is the SQL script to accomplish this:

```sql
-- Step 1: Add the new column for area codes
ALTER TABLE [States]
ADD [AreaCode] NVARCHAR(10);

-- Step 2: Update the new column with the area codes
UPDATE [States]
SET [AreaCode] = CASE 
    WHEN [StateName] = N'تهران' THEN '021'
    WHEN [StateName] = N'اصفهان' THEN '031'
    WHEN [StateName] = N'آذربایجان شرقی' THEN '041'
    WHEN [StateName] = N'آذربایجان غربی' THEN '044'
    WHEN [StateName] = N'اردبیل' THEN '045'
    WHEN [StateName] = N'ایلام' THEN '084'
    WHEN [StateName] = N'بوشهر' THEN '077'
    WHEN [StateName] = N'چهارمحال و بختیاری' THEN '038'
    WHEN [StateName] = N'خراسان جنوبی' THEN '056'
    WHEN [StateName] = N'خراسان رضوی' THEN '051'
    WHEN [StateName] = N'خراسان شمالی' THEN '058'
    WHEN [StateName] = N'خوزستان' THEN '061'
    WHEN [StateName] = N'زنجان' THEN '024'
    WHEN [StateName] = N'سمنان' THEN '023'
    WHEN [StateName] = N'سیستان و بلوچستان' THEN '054'
    WHEN [StateName] = N'فارس' THEN '071'
    WHEN [StateName] = N'قزوین' THEN '028'
    WHEN [StateName] = N'قم' THEN '025'
    WHEN [StateName] = N'کردستان' THEN '087'
    WHEN [StateName] = N'کرمان' THEN '034'
    WHEN [StateName] = N'کرمانشاه' THEN '083'
    WHEN [StateName] = N'کهگیلویه و بویراحمد' THEN '074'
    WHEN [StateName] = N'گلستان' THEN '017'
    WHEN [StateName] = N'گیلان' THEN '013'
    WHEN [StateName] = N'لرستان' THEN '066'
    WHEN [StateName] = N'مازندران' THEN '011'
    WHEN [StateName] = N'مرکزی' THEN '086'
    WHEN [StateName] = N'هرمزگان' THEN '076'
    WHEN [StateName] = N'همدان' THEN '081'
    WHEN [StateName] = N'یزد' THEN '035'
    WHEN [StateName] = N'البرز' THEN '026'
    ELSE NULL
END;
```

This script first adds a new column called `AreaCode` to the `States` table. Then, it updates this column with the corresponding area codes based on the state names.


- Just copy and paste this script into your SQL Server management tool and run it. ^_^

---

## Data Accuracy

We have identified that the data for some cities might not be entirely accurate. We are committed to ensuring the correctness of our dataset, and we need your help!
How You Can Help

   - Report Issues: If you notice any incorrect city names or associations, please report them by creating an issue in this repository.
   - Contribute Data: If you have verified data, feel free to contribute by submitting a pull request with the correct data.

## Planned Actions

   - Verification: We are in the process of verifying the current data against reliable sources.
   - Updates: We will periodically update the dataset.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
