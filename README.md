
# ProvinceCity-Iran

This repository contains a simple HTML, CSS, and JavaScript project that allows users to select an Iranian province from a dropdown list and view the corresponding cities in that province.

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

This section provides the complete SQL script to create the `Provinces` and `Cities` tables and insert all the provinces and cities. 

```sql
GO
SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE [Cities](
	[ID] [bigint] IDENTITY(1,1) NOT NULL,
	[ProvinceID] [bigint] NOT NULL,
	[Title] [nvarchar](200) NOT NULL,
	[LatinTitle] [nvarchar](200) NOT NULL,
 CONSTRAINT [PK_City] PRIMARY KEY CLUSTERED 
(
	[ID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON, OPTIMIZE_FOR_SEQUENTIAL_KEY = OFF) ON [PRIMARY]
) ON [PRIMARY]
GO
SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE [Provinces](
	[ID] [bigint] IDENTITY(1,1) NOT NULL,
	[Title] [nvarchar](max) NULL,
	[LatinTitle] [nvarchar](200) NOT NULL,
	[AreaCode] [nvarchar](10) NULL,
 CONSTRAINT [PK_Provinces] PRIMARY KEY CLUSTERED 
(
	[ID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON, OPTIMIZE_FOR_SEQUENTIAL_KEY = OFF) ON [PRIMARY]
) ON [PRIMARY] TEXTIMAGE_ON [PRIMARY]
GO
SET IDENTITY_INSERT [Cities] ON 
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1, 1, N'اهر', N'Ahar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (2, 1, N'تبریز', N'Tabriz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (3, 1, N'سردرود', N'Sardrud')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (4, 1, N'خسروشاه', N'Khosrowshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (5, 1, N'باسمنج', N'Basmenj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (6, 1, N'سراب', N'Sarab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (7, 1, N'مهربان', N'Mehraban')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (8, 1, N'شربیان', N'Sharabian')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (9, 1, N'دوزدوزان', N'Dozdozan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (10, 1, N'مراغه', N'Maragheh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (11, 1, N'خراجو', N'Kharaju')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (12, 1, N'زنوز', N'Zonouz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (13, 1, N'مرند', N'Marand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (14, 1, N'بناب مرند', N'Bonab Marand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (15, 1, N'یامچی', N'Yamchi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (16, 1, N'دیزج حسین بیگ', N'Dizaj Hoseyn Beyg')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (17, 1, N'کشکسرای', N'Kashk-e Saray')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (18, 1, N'ترکمانچای', N'Torkamanchay')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (19, 1, N'آقکند', N'Aqqand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (20, 1, N'ترک', N'Tork')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (21, 1, N'میانه', N'Miyaneh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (22, 1, N'آچاچی', N'Achachi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (23, 1, N'هشترود', N'Hashtrood')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (24, 1, N'نظرکهریزی', N'Nazar Kahrizi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (25, 1, N'بناب', N'Bonab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (26, 1, N'خوشه مهر', N'Khoshmehr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (27, 1, N'تیکمه داش', N'Tikmeh Dash')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (28, 1, N'کردکندی', N'Kordkandi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (29, 1, N'بستان‌آباد', N'Bostanabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (30, 1, N'صوفیان', N'Sufian')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (31, 1, N'خامنه', N'Khameneh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (32, 1, N'شبستر', N'Shabestar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (33, 1, N'شرفخانه', N'Sharafkhaneh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (34, 1, N'شندآباد', N'Shendabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (35, 1, N'سیس', N'Sis')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (36, 1, N'وایقان', N'Vaighan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (37, 1, N'کوزه کنان', N'Kouzeh Konan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (38, 1, N'داریان', N'Darian')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (39, 1, N'علیشاه', N'Ali Shah')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (40, 1, N'تسوج', N'Tasuj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (41, 1, N'کلیبر', N'Kaleybar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (42, 1, N'آبش احمد', N'Abish Ahmad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (43, 1, N'خواجه', N'Khaje')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (44, 1, N'اربطان', N'Arbatagh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (45, 1, N'هریس', N'Heris')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (46, 1, N'زرنق', N'Zarnaq')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (47, 1, N'بخشایش', N'Bakhshayesh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (48, 1, N'کلوانق', N'Kalvanagh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (49, 1, N'سیه‌رود', N'Siyah Rud')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (50, 1, N'جلفا', N'Jolfa')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (51, 1, N'هادیشهر', N'Hadishahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (52, 1, N'لیلان', N'Lilan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (53, 1, N'ملکان', N'Malekan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (54, 1, N'مبارک‌شهر', N'Mobarak Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (55, 1, N'گوگان', N'Gogan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (56, 1, N'تیمورلو', N'Teymurlu')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (57, 1, N'ممقان', N'Mamqan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (58, 1, N'آذرشهر', N'Azarshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (59, 1, N'ایلخچی', N'Ilkhchi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (60, 1, N'اسکو', N'Osku')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (61, 1, N'سهند', N'Sahand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (62, 1, N'قره‌آغاج', N'Qaraghaj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (63, 1, N'خاروانا', N'Kharvana')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (64, 1, N'ورزقان', N'Varzeqan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (65, 1, N'جوان‌قلعه', N'Javan Qaleh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (66, 1, N'عجب‌شیر', N'Ajab Shir')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (67, 1, N'خمارلو', N'Khomarlu')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (68, 1, N'لاریجان', N'Larijan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (69, 1, N'عاشقلو', N'Ashaglu')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (70, 1, N'هوراند', N'Horand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (71, 2, N'قوشچی', N'Qushchi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (72, 2, N'سیلوانه', N'Silvaneh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (73, 2, N'سرو', N'Sero')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (74, 2, N'ارومیه', N'Urmia')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (75, 2, N'نوشین', N'Nushin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (76, 2, N'پیرانشهر', N'Piranshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (77, 2, N'لاجان', N'Lajan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (78, 2, N'خوی', N'Khoy')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (79, 2, N'دیزج دیز', N'Dizaj Diz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (80, 2, N'زرآباد', N'Zarrabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (81, 2, N'ایواوغلی', N'Ivughli')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (82, 2, N'قطور', N'Qatur')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (83, 2, N'فیرورق', N'Firouragh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (84, 2, N'سردشت', N'Sardasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (85, 2, N'ربط', N'Rabat')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (86, 2, N'نلاس', N'Nalash')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (87, 2, N'تازه شهر', N'Tazeh Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (88, 2, N'سلماس', N'Salmas')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (89, 2, N'ماكو', N'Maku')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (90, 2, N'بازرگان', N'Bazargan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (91, 2, N'خلیفان', N'Khalifan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (92, 2, N'مهاباد', N'Mahabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (93, 2, N'گوگ تپه', N'Guk Tepe')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (94, 2, N'میاندوآب', N'Miandoab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (95, 2, N'بکتاش', N'Baktash')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (96, 2, N'نقده', N'Naqadeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (97, 2, N'محمدیار', N'Mohammadyar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (98, 2, N'سیمینه', N'Simineh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (99, 2, N'بوكان', N'Bukan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (100, 2, N'شاهین دژ', N'Shahin Dezh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (101, 2, N'محمودآباد', N'Mahmoodabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (102, 2, N'كشاورز', N'Keshavarz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (103, 2, N'تكاب', N'Takab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (104, 2, N'تازه کندنصرت آباد', N'Tazeh Kand Nosratabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (105, 2, N'اشنویه', N'Oshnavieh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (106, 2, N'نالوس', N'Nalous')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (107, 2, N'آواجیق', N'Avajiq')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (108, 2, N'سیه چشمه', N'Siyah Cheshmeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (109, 2, N'نازك علیا', N'Nazak Aliya')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (110, 2, N'پلدشت', N'Poldasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (111, 2, N'حاجیلار', N'Hajilar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (112, 2, N'قره ضیاءالدین', N'Qaraziya Eddin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (113, 2, N'مرگنلر', N'Marganlar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (114, 2, N'شوط', N'Showt')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (115, 2, N'یولاگلدی', N'Yulageldi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (116, 2, N'چهاربرج', N'Chaharborj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (117, 2, N'باروق', N'Baruq')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (118, 2, N'میرآباد', N'Mirabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (119, 3, N'اردبیل', N'Ardabil')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (120, 3, N'هیر', N'Hir')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (121, 3, N'آراللو', N'Arallu')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (122, 3, N'ثمرین', N'Samarin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (123, 3, N'بیله سوار', N'Bilesavar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (124, 3, N'جعفرآباد', N'Jafarabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (125, 3, N'هشتجین', N'Hashjin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (126, 3, N'كلور', N'Kolver')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (127, 3, N'خلخال', N'Khalkhal')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (128, 3, N'رضی', N'Razi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (129, 3, N'مشگین شهر', N'Meshginshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (130, 3, N'النی', N'Alni')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (131, 3, N'لاهرود', N'Lahrud')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (132, 3, N'فخراباد', N'Fakhrabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (133, 3, N'مرادلو', N'Moradlu')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (134, 3, N'قصابه', N'Qasabeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (135, 3, N'گرمی', N'Germi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (136, 3, N'زهرا', N'Zahra')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (137, 3, N'اولتان', N'Oltan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (138, 3, N'پارس آباد', N'Parsabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (139, 3, N'مغان سر', N'Moghan Sar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (140, 3, N'اسلام اباد', N'Eslamabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (141, 3, N'گیوی', N'Givi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (142, 3, N'آبی بیگلو', N'Abey Beyglu')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (143, 3, N'نمین', N'Namin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (144, 3, N'عنبران', N'Anbaran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (145, 3, N'نیر', N'Nir')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (146, 3, N'كوراییم', N'Kuraim')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (147, 3, N'سرعین', N'Sareyn')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (148, 3, N'اردیموسی', N'Ardeymousi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (149, 3, N'اصلاندوز', N'Aslandooz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (150, 3, N'تازه کند انگوت', N'Tazeh Kand Angut')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (151, 4, N'اردستان', N'Ardestan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (152, 4, N'زواره', N'Zavareh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (153, 4, N'مهاباد', N'Mahabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (154, 4, N'اصفهان', N'Isfahan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (155, 4, N'قهجاورستان', N'Qahjavarestan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (156, 4, N'بهارستان', N'Baharestan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (157, 4, N'زیار', N'Ziyar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (158, 4, N'خمینی شهر', N'Khomeini Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (159, 4, N'درچه', N'Dorcheh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (160, 4, N'کوشک', N'Koushk')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (161, 4, N'اصغرآباد', N'Asgharabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (162, 4, N'ویست', N'Veyset')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (163, 4, N'خوانسار', N'Khansar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (164, 4, N'کمه', N'Komeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (165, 4, N'سمیرم', N'Semirom')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (166, 4, N'حنا', N'Hana')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (167, 4, N'ونک', N'Vanak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (168, 4, N'بیده', N'Bideh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (169, 4, N'فتح آباد', N'Fathabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (170, 4, N'داران', N'Daran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (171, 4, N'دامنه', N'Damaneh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (172, 4, N'فریدونشهر', N'Fereydunshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (173, 4, N'برف انبار', N'Barf Anbar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (174, 4, N'طاد', N'Tad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (175, 4, N'پیربکران', N'Pir Bakran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (176, 4, N'بهاران شهر', N'Baharan Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (177, 4, N'بوستان زر', N'Boostan-e Zar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (178, 4, N'فلاورجان', N'Falavarjan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (179, 4, N'کلیشادوسودرجان', N'Kelishad-o-Sudarjan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (180, 4, N'ابریشم', N'Abrisham')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (181, 4, N'اشترجان', N'Oshtorjan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (182, 4, N'مینادشت', N'Minadasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (183, 4, N'قهدریجان', N'Qahderijan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (184, 4, N'زازران', N'Zazeran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (185, 4, N'شهرضا', N'Shahreza')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (186, 4, N'منظریه', N'Manzariyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (187, 4, N'قمصر', N'Ghamsar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (188, 4, N'جوشقان قالی', N'Josheghan-e Qali')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (189, 4, N'کامو و چوگان', N'Kamu va Chugan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (190, 4, N'کاشان', N'Kashan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (191, 4, N'مشکات', N'Meshkat')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (192, 4, N'نیاسر', N'Niasar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (193, 4, N'برزک', N'Barzok')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (194, 4, N'گلپایگان', N'Golpayegan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (195, 4, N'گوگد', N'Guged')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (196, 4, N'گلشهر', N'Golshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (197, 4, N'باغ بهادران', N'Bagh-e Bahadoran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (198, 4, N'چرمهین', N'Charmahin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (199, 4, N'چمگردان', N'Chamgordan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (200, 4, N'زرین شهر', N'Zarrin Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (201, 4, N'سده لنجان', N'Sedeh Lenjan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (202, 4, N'ورنامخواست', N'Varnamkhast')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (203, 4, N'فولادشهر', N'Fooladshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (204, 4, N'زاینده رود', N'Zayandeh Rud')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (205, 4, N'باغشاد', N'Baghsad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (206, 4, N'انارک', N'Anarak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (207, 4, N'نایین', N'Naeen')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (208, 4, N'بافران', N'Bafran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (209, 4, N'نجف آباد', N'Najafabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (210, 4, N'جوزدان', N'Jowzdan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (211, 4, N'گلدشت', N'Goldasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (212, 4, N'کهریزسنگ', N'Kahriz Sang')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (213, 4, N'دهق', N'Dehagh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (214, 4, N'علویجه', N'Alavijeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (215, 4, N'نطنز', N'Natanz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (216, 4, N'طرق رود', N'Taregh Rud')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (217, 4, N'بادرود', N'Badroud')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (218, 4, N'خالدآباد', N'Khaledabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (219, 4, N'میمه', N'Meymeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (220, 4, N'وزوان', N'Vazvan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (221, 4, N'لای بید', N'Lay Bid')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (222, 4, N'شاهین شهر', N'Shahin Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (223, 4, N'گزبرخوار', N'Gazborkhar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (224, 4, N'گرگاب', N'Gorgab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (225, 4, N'مبارکه', N'Mobarakeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (226, 4, N'مجلسی', N'Majlesi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (227, 4, N'دیزیچه', N'Dizicheh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (228, 4, N'طالخونچه', N'Talkhooncheh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (229, 4, N'کرکوند', N'Karkevand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (230, 4, N'زیباشهر', N'Zibashahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (231, 4, N'ده سرخ', N'Deh Sorkh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (232, 4, N'ابوزیدآباد', N'Abuzeydabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (233, 4, N'آران وبیدگل', N'Aran va Bidgol')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (234, 4, N'نوش آباد', N'Nushabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (235, 4, N'سفیدشهر', N'Safidshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (236, 4, N'عسگران', N'Asgaran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (237, 4, N'تیران', N'Tiran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (238, 4, N'رضوانشهر', N'Rezvanshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (239, 4, N'چادگان', N'Chadegan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (240, 4, N'رزوه', N'Razaveh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (241, 4, N'دهاقان', N'Dehaghan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (242, 4, N'گلشن', N'Golshan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (243, 4, N'حبیب آباد', N'Habibabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (244, 4, N'شاپورآباد', N'Shapourabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (245, 4, N'کمشچه', N'Komeshcheh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (246, 4, N'خورزوق', N'Khorzug')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (247, 4, N'دستگرد', N'Dastgerd')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (248, 4, N'دولت آباد', N'Dolatabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (249, 4, N'سین', N'Sin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (250, 4, N'خور', N'Khur')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (251, 4, N'فرخی', N'Farrokhi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (252, 4, N'جندق', N'Jandagh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (253, 4, N'بویین ومیاندشت', N'Buin va Miandasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (254, 4, N'افوس', N'Afus')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (255, 4, N'کوهپایه', N'Kuhpayeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (256, 4, N'تودشک', N'Tudeshk')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (257, 4, N'سجزی', N'Sejzi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (258, 4, N'نیک آباد', N'Nikabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (259, 4, N'محمدآباد', N'Mohammadabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (260, 4, N'نصرآباد', N'Nasrabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (261, 4, N'حسن اباد', N'Hasanabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (262, 4, N'ورزنه', N'Varzaneh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (263, 4, N'هرند', N'Harand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (264, 4, N'اژیه', N'Ezhiyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (265, 5, N'کرج', N'Karaj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (266, 5, N'ماهدشت', N'Mahdasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (267, 5, N'کمال شهر', N'Kamalshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (268, 5, N'محمدشهر', N'Mohammadshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (269, 5, N'گرمدره', N'Garmdareh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (270, 5, N'آسارا', N'Asara')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (271, 5, N'هشتگرد', N'Hashtgerd')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (272, 5, N'گلسار', N'Golsar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (273, 5, N'مهستان', N'Mahestan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (274, 5, N'کوهسار', N'Kuhsar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (275, 5, N'نظرآباد', N'Nazarabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (276, 5, N'تنکمان', N'Tankaman')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (277, 5, N'طالقان', N'Taleqan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (278, 5, N'اشتهارد', N'Eshtehard')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (279, 5, N'پلنگ آباد', N'Palangabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (280, 5, N'فردیس', N'Fardis')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (281, 5, N'مشکین دشت', N'Meshkin Dasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (282, 5, N'چهارباغ', N'Chaharbagh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (283, 6, N'ایلام', N'Ilam')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (284, 6, N'جعفراباد', N'Jafarabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (285, 6, N'دره شهر', N'Darreh Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (286, 6, N'ماژین', N'Majin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (287, 6, N'پهله', N'Pahleh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (288, 6, N'دهلران', N'Dehloran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (289, 6, N'موسیان', N'Musian')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (290, 6, N'میمه', N'Meymeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (291, 6, N'سرابله', N'Sarableh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (292, 6, N'آسمان آباد', N'Asemanabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (293, 6, N'شباب', N'Shabab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (294, 6, N'بلاوه', N'Balaveh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (295, 6, N'صالح آباد', N'Salehabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (296, 6, N'مهران', N'Mehran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (297, 6, N'مورموری', N'Murmuri')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (298, 6, N'آبدانان', N'Abdanan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (299, 6, N'سراب باغ', N'Sarab Bagh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (300, 6, N'زرنه', N'Zarneh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (301, 6, N'ایوان', N'Eyvan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (302, 6, N'اركواز', N'Arkavaz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (303, 6, N'دلگشا', N'Delgosha')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (304, 6, N'مهر', N'Mehr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (305, 6, N'لومار', N'Lumar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (306, 6, N'بدره', N'Bedreh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (307, 6, N'چشمه شیرین', N'Cheshmeh Shirin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (308, 6, N'توحید', N'Tohid')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (309, 6, N'چوار', N'Chovar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (310, 7, N'خارك', N'Khark')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (311, 7, N'بوشهر', N'Bushehr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (312, 7, N'عالی شهر', N'Aali Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (313, 7, N'چغادک', N'Choghadak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (314, 7, N'دلوار', N'Delvar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (315, 7, N'اهرم', N'Ahram')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (316, 7, N'آباد', N'Abad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (317, 7, N'سعد آباد', N'Saadabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (318, 7, N'وحدتیه', N'Vahdatiyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (319, 7, N'شبانكاره', N'Shabankareh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (320, 7, N'برازجان', N'Borazjan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (321, 7, N'دالكی', N'Dalki')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (322, 7, N'تنگ ارم', N'Tang Eram')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (323, 7, N'كلمه', N'Kalameh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (324, 7, N'بوشکان', N'Boshkan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (325, 7, N'آب پخش', N'Aab Pakhsh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (326, 7, N'كاكی', N'Kaki')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (327, 7, N'بادوله', N'Baduleh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (328, 7, N'خورموج', N'Khormuj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (329, 7, N'شنبه', N'Shanbeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (330, 7, N'بردخون', N'Bord Khun')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (331, 7, N'بندردیر', N'Bandar-e Deyr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (332, 7, N'بردستان', N'Bordestan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (333, 7, N'دوراهک', N'Dowrahak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (334, 7, N'آبدان', N'Abdan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (335, 7, N'بندركنگان', N'Bandar-e Kangan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (336, 7, N'بنك', N'Benak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (337, 7, N'سیراف', N'Siraf')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (338, 7, N'بندرریگ', N'Bandar-e Rig')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (339, 7, N'بندرگناوه', N'Bandar-e Genaveh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (340, 7, N'امام حسن', N'Imam Hasan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (341, 7, N'بندردیلم', N'Bandar-e Deylam')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (342, 7, N'انارستان', N'Anarestan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (343, 7, N'ریز', N'Riz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (344, 7, N'جم', N'Jam')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (345, 7, N'بهارستان', N'Baharestan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (346, 7, N'عسلویه', N'Asaluyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (347, 7, N'نخل تقی', N'Nakhl-e Taqi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (348, 7, N'بیدخون', N'Bidkhoon')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (349, 7, N'چاه مبارک', N'Chah Mobarak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (350, 8, N'تهران', N'Tehran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (351, 8, N'دماوند', N'Damavand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (352, 8, N'كیلان', N'Kilan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (353, 8, N'آبسرد', N'Absard')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (354, 8, N'رودهن', N'Roudehen')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (355, 8, N'آبعلی', N'Abali')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (356, 8, N'حسن آباد', N'Hasanabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (357, 8, N'باقرشهر', N'Baqershahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (358, 8, N'كهریزك', N'Kahrizak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (359, 8, N'ری', N'Rey')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (360, 8, N'قیام دشت', N'Ghiamdasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (361, 8, N'قلعه نو', N'Ghaleh No')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (362, 8, N'فشم', N'Fasham')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (363, 8, N'تجریش', N'Tajrish')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (364, 8, N'شمشک', N'Shemshak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (365, 8, N'لواسان', N'Lavasan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (366, 8, N'جوادآباد', N'Javadabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (367, 8, N'ورامین', N'Varamin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (368, 8, N'شهریار', N'Shahriar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (369, 8, N'صباشهر', N'Sabashahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (370, 8, N'شاهدشهر', N'Shahedshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (371, 8, N'باغستان', N'Baghestan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (372, 8, N'اندیشه', N'Andisheh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (373, 8, N'وحیدیه', N'Vahidieh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (374, 8, N'فردوسیه', N'Ferdosiyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (375, 8, N'چهاردانگه', N'Chahar Dangeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (376, 8, N'اسلامشهر', N'Eslamshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (377, 8, N'احمد آباد مستوفی', N'Ahmadabad-e Mostowfi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (378, 8, N'رباط كریم', N'Robat Karim')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (379, 8, N'نصیرشهر', N'Nasirshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (380, 8, N'پرند', N'Parand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (381, 8, N'شریف آباد', N'Sharifabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (382, 8, N'پاكدشت', N'Pakdasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (383, 8, N'فرون آباد', N'Firoonabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (384, 8, N'ارجمند', N'Arjmand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (385, 8, N'فیروزكوه', N'Firouzkouh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (386, 8, N'قدس', N'Qods')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (387, 8, N'ملارد', N'Malard')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (388, 8, N'صفادشت', N'Safadasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (389, 8, N'پیشوا', N'Pishva')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (390, 8, N'جلیل آباد', N'Jalilabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (391, 8, N'گلستان', N'Golestan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (392, 8, N'صالحیه', N'Salehiyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (393, 8, N'نسیم شهر', N'Nasim Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (394, 8, N'بومهن', N'Boumehen')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (395, 8, N'خسروآباد', N'Khosrowabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (396, 8, N'سعیدآباد', N'Saeedabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (397, 8, N'پردیس', N'Pardis')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (398, 8, N'قرچک', N'Qarchak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (399, 9, N'گندمان', N'Gandoman')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (400, 9, N'بروجن', N'Borujen')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (401, 9, N'فرادبنه', N'Faradonbeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (402, 9, N'سفیددشت', N'Sefiddasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (403, 9, N'نقنه', N'Naqneh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (404, 9, N'بلداجی', N'Boldaji')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (405, 9, N'شهرکرد', N'Shahr-e Kord')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (406, 9, N'هفشجان', N'Hafshejan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (407, 9, N'کیان', N'Kian')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (408, 9, N'طاقانک', N'Taqanak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (409, 9, N'نافچ', N'Nafch')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (410, 9, N'سورشجان', N'Sureshjan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (411, 9, N'سودجان', N'Soudjan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (412, 9, N'هارونی', N'Harouni')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (413, 9, N'فرخ شهر', N'Farrokhshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (414, 9, N'فارسان', N'Farsan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (415, 9, N'گوجان', N'Gowjan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (416, 9, N'باباحیدر', N'Baba Heydar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (417, 9, N'فیل آباد', N'Filabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (418, 9, N'جونقان', N'Joneghan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (419, 9, N'پردنجان', N'Pardenjan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (420, 9, N'چلیچه', N'Chelgard')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (421, 9, N'لردگان', N'Lordegan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (422, 9, N'منج', N'Menj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (423, 9, N'سردشت', N'Sardasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (424, 9, N'اردل', N'Ardal')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (425, 9, N'کاج', N'Kaj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (426, 9, N'دشتک', N'Dashtak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (427, 9, N'سرخون', N'Sarkhun')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (428, 9, N'بازفت', N'Bazoft')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (429, 9, N'چلگرد', N'Chelgerd')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (430, 9, N'صمصامی', N'Samsami')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (431, 9, N'شلمزار', N'Shalamzar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (432, 9, N'گهرو', N'Gahru')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (433, 9, N'دستنا', N'Dastena')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (434, 9, N'ناغان', N'Naghan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (435, 9, N'سامان', N'Saman')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (436, 9, N'هوره', N'Hureh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (437, 9, N'بن', N'Ben')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (438, 9, N'وردنجان', N'Vardenjan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (439, 9, N'یان چشمه', N'Yan Cheshmeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (440, 9, N'آلونی', N'Aluni')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (441, 9, N'مال خلیفه', N'Mal-e Khalifeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (442, 10, N'بیرجند', N'Birjand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (443, 10, N'قهستان', N'Ghahestan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (444, 10, N'طبس مسینا', N'Tabas-e Masina')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (445, 10, N'گزیك', N'Gazik')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (446, 10, N'اسدیه', N'Asadieh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (447, 10, N'سربیشه', N'Sarbisheh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (448, 10, N'مود', N'Mood')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (449, 10, N'درح', N'Doroh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (450, 10, N'قاین', N'Qaen')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (451, 10, N'اسفدن', N'Esfeden')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (452, 10, N'خضری دشت بیاض', N'Khezri Dasht-e Bayaz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (453, 10, N'نیمبلوك', N'Nimbeluk')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (454, 10, N'آرین شهر', N'Arian Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (455, 10, N'شوسف', N'Shusef')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (456, 10, N'نهبندان', N'Nehbandan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (457, 10, N'سرایان', N'Sarayan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (458, 10, N'آیسك', N'Ayask')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (459, 10, N'سه قلعه', N'Seh Qaleh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (460, 10, N'باغستان', N'Baghestan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (461, 10, N'اسلامیه', N'Eslamiyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (462, 10, N'فردوس', N'Ferdows')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (463, 10, N'بشرویه', N'Bashravieh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (464, 10, N'ارسك', N'Arsak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (465, 10, N'حاجی آباد', N'Hajiabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (466, 10, N'زهان', N'Zohan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (467, 10, N'آبیز', N'Abiz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (468, 10, N'خوسف', N'Khusf')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (469, 10, N'ماژان', N'Majan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (470, 10, N'عشق آباد', N'Eshqabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (471, 10, N'طبس', N'Tabas')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (472, 10, N'دیهوك', N'Deyhuk')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (473, 11, N'تایباد', N'Taybad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (474, 11, N'كاریز', N'Kariz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (475, 11, N'مشهد ریزه', N'Mashhad Rizeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (476, 11, N'بایك', N'Baiek')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (477, 11, N'كدكن', N'Kadkan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (478, 11, N'تربت حیدریه', N'Torbat-e Heydarieh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (479, 11, N'نسر', N'Nasr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (480, 11, N'رباط سنگ', N'Rabat-e Sang')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (481, 11, N'تربت جام', N'Torbat-e Jam')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (482, 11, N'نصرآباد', N'Nasrabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (483, 11, N'احمدآباد صولت', N'Ahmadabad-e Solt')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (484, 11, N'نیل شهر', N'Nil Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (485, 11, N'سمیع آباد', N'Sami Abad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (486, 11, N'چاپشلو', N'Chapeshlu')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (487, 11, N'لطف آباد', N'Lotfabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (488, 11, N'درگز', N'Dargaz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (489, 11, N'نوخندان', N'Nokhandan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (490, 11, N'روداب', N'Rudab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (491, 11, N'سبزوار', N'Sabzevar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (492, 11, N'باجگیران', N'Bajgiran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (493, 11, N'مزرج', N'Mazraj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (494, 11, N'قوچان', N'Quchan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (495, 11, N'الماجق', N'Almagh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (496, 11, N'شهر کهنه', N'Shahr-e Kohneh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (497, 11, N'كاشمر', N'Kashmar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (498, 11, N'فرگ قلعه', N'Farg Qaleh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (499, 11, N'بیدخت', N'Beydokht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (500, 11, N'گناباد', N'Gonabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (501, 11, N'روشناوند', N'Roshanavand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (502, 11, N'كاخك', N'Kakheh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (503, 11, N'ملك آباد', N'Malekabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (504, 11, N'مشهد', N'Mashhad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (505, 11, N'مشهد ثامن', N'Mashhad Samen')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (506, 11, N'رضویه', N'Rezvaneh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (507, 11, N'چكنه', N'Chakaneh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (508, 11, N'نیشابور', N'Nishapur')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (509, 11, N'بار', N'Bar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (510, 11, N'چناران', N'Chenaran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (511, 11, N'رادكان', N'Radkan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (512, 11, N'سیدآباد', N'Seydabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (513, 11, N'سنگان', N'Sangan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (514, 11, N'خواف', N'Khaf')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (515, 11, N'نشتیفان', N'Nashtifan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (516, 11, N'قاسم آباد', N'Qasemabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (517, 11, N'سده', N'Sedeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (518, 11, N'سلامی', N'Salami')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (519, 11, N'مزدآوند', N'Mozdavan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (520, 11, N'سرخس', N'Sarakhs')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (521, 11, N'قلندر آباد', N'Qalandarabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (522, 11, N'سفید سنگ', N'Sefid Sang')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (523, 11, N'فریمان', N'Fariman')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (524, 11, N'فرهادگرد', N'Farhadgerd')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (525, 11, N'انابد', N'Anabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (526, 11, N'بردسكن', N'Bardaskan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (527, 11, N'شهرآباد', N'Shahrabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (528, 11, N'جنگل', N'Jangal')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (529, 11, N'رشتخوار', N'Rashtkhar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (530, 11, N'چنار', N'Chenar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (531, 11, N'شهرزو', N'Shahr-e Zow')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (532, 11, N'كلات', N'Kalat')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (533, 11, N'حسن آباد', N'Hasanabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (534, 11, N'كندر', N'Kondor')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (535, 11, N'خلیل آباد', N'Khalilabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (536, 11, N'شادمهر', N'Shadmehr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (537, 11, N'فیض آباد', N'Feyzabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (538, 11, N'بجستان', N'Bajestan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (539, 11, N'یونسی', N'Yunesi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (540, 11, N'طرقبه', N'Torghebeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (541, 11, N'شاندیز', N'Shandiz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (542, 11, N'فیروزه', N'Firoozeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (543, 11, N'گرماب', N'Garmab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (544, 11, N'همت آباد', N'Hematabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (545, 11, N'جغتای', N'Joghtay')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (546, 11, N'ریواده', N'Rivad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (547, 11, N'دولت آباد', N'Dowlatabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (548, 11, N'چخماق', N'Chakhmaq')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (549, 11, N'نقاب', N'Neqab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (550, 11, N'حكم آباد', N'Hokmabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (551, 11, N'باخرز', N'Bakharz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (552, 11, N'قلعه نوعلیا', N'Qaleh Now Olya')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (553, 11, N'سلطان آباد', N'Soltanabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (554, 11, N'مشكان', N'Meshkan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (555, 11, N'نوده انقلاب', N'Nowdeh Enghelab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (556, 11, N'داورزن', N'Davarzan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (557, 11, N'ریوند', N'Rivand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (558, 11, N'صالح آباد', N'Salehabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (559, 11, N'جنت آباد', N'Jannatabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (560, 11, N'ریوش', N'Rivash')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (561, 11, N'درود', N'Dorud')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (562, 11, N'قدمگاه', N'Ghadamgah')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (563, 11, N'خرو', N'Kharv')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (564, 11, N'اسحق آباد', N'Es-haq Abad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (565, 11, N'ششتمد', N'Sheshtamad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (566, 11, N'شامكان', N'Shamkan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (567, 11, N'گلبهار', N'Golbahar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (568, 11, N'گلمكان', N'Golmakan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (569, 11, N'عشق آباد', N'Eshqabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (570, 12, N'صفی آباد', N'Safiabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (571, 12, N'اسفراین', N'Esfarayen')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (572, 12, N'بجنورد', N'Bojnord')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (573, 12, N'چناران شهر', N'Chenaran Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (574, 12, N'حصارگرمخان', N'Hesaar Garmkhan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (575, 12, N'سنخواست', N'Sankhvast')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (576, 12, N'شوقان', N'Shoqan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (577, 12, N'جاجرم', N'Jajarm')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (578, 12, N'لوجلی', N'Lujali')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (579, 12, N'خانلق', N'Khanlaq')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (580, 12, N'شیروان', N'Shirvan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (581, 12, N'زیارت', N'Ziarat')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (582, 12, N'قوشخانه', N'Qushkhaneh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (583, 12, N'تیتكانلو', N'Titkanlu')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (584, 12, N'فاروج', N'Faruj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (585, 12, N'قاضی', N'Ghazi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (586, 12, N'آوا', N'Ava')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (587, 12, N'پیش قلعه', N'Pish Qaleh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (588, 12, N'آشخانه', N'Ashkhaneh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (589, 12, N'ایور', N'Eyvar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (590, 12, N'گرمه', N'Garmeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (591, 12, N'درق', N'Derq')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (592, 12, N'راز', N'Raz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (593, 12, N'غلامان', N'Gholaman')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (594, 12, N'یکه سعود', N'Yekeh Saud')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (595, 13, N'اروندکنار', N'Arvandkenar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (596, 13, N'آبادان', N'Abadan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (597, 13, N'چویبده', N'Chavibdeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (598, 13, N'حسینیه', N'Hoseyniyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (599, 13, N'بیدروبه', N'Bidrobeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (600, 13, N'اندیمشک', N'Andimeshk')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (601, 13, N'آزادی', N'Azadi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (602, 13, N'چم گلک', N'Cham Golak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (603, 13, N'اهواز', N'Ahvaz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (604, 13, N'الهایی', N'Elhayi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (605, 13, N'ایذه', N'Izeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (606, 13, N'بندرامام خمینی', N'Bandar Imam Khomeini')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (607, 13, N'بندرماهشهر', N'Bandar Mahshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (608, 13, N'چمران', N'Chamran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (609, 13, N'سردشت', N'Sardasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (610, 13, N'بهبهان', N'Behbahan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (611, 13, N'منصوریه', N'Mansuriyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (612, 13, N'تشان', N'Tashan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (613, 13, N'خرمشهر', N'Khorramshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (614, 13, N'مقاومت', N'Moghavemat')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (615, 13, N'مینوشهر', N'Minushahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (616, 13, N'حمزه', N'Hamzeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (617, 13, N'سالند', N'Saland')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (618, 13, N'دزفول', N'Dezful')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (619, 13, N'شمس آباد', N'Shamsabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (620, 13, N'شهر امام', N'Shahr-e Emam')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (621, 13, N'صفی آباد', N'Safiabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (622, 13, N'میانرود', N'Mianrud')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (623, 13, N'سیاه منصور', N'Siah Mansur')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (624, 13, N'منتظران', N'Montazeran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (625, 13, N'چغامیش', N'Choghamish')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (626, 13, N'جندی شاپور', N'Jundi Shapur')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (627, 13, N'شهیون', N'Shahyun')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (628, 13, N'بستان', N'Bostan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (629, 13, N'سوسنگرد', N'Susangerd')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (630, 13, N'کوت سیدنعیم', N'Kut-e Seyyed Naeem')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (631, 13, N'ابوحمیظه', N'Abu Humeizeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (632, 13, N'رامهرمز', N'Ramhormoz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (633, 13, N'رود زرد ماشین', N'Rud-e Zard-e Mashin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (634, 13, N'سلطان آباد', N'Soltanabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (635, 13, N'باوج', N'Bavij')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (636, 13, N'شادگان', N'Shadegan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (637, 13, N'خنافره', N'Khanafareh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (638, 13, N'دارخوین', N'Dar Khvyn')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (639, 13, N'شوشتر', N'Shushtar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (640, 13, N'شرافت', N'Sherafat')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (641, 13, N'سرداران', N'Sardaran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (642, 13, N'گوریه', N'Guriyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (643, 13, N'عرب حسن', N'Arab Hasan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (644, 13, N'مسجدسلیمان', N'Masjed Soleyman')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (645, 13, N'گلگیر', N'Golgir')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (646, 13, N'عنبر', N'Anbar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (647, 13, N'شوش', N'Shush')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (648, 13, N'حر', N'Horr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (649, 13, N'فتح المبین', N'Fath ol-Mobin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (650, 13, N'باغ ملک', N'Baghmalek')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (651, 13, N'صیدون', N'Seydun')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (652, 13, N'میداود', N'Meydavud')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (653, 13, N'قلعه تل', N'Qaleh Tel')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (654, 13, N'جایزان', N'Jayezan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (655, 13, N'امیدیه', N'Omidiyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (656, 13, N'میانکوه', N'Miankuh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (657, 13, N'لالی', N'Lali')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (658, 13, N'تراز', N'Taraz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (659, 13, N'هندیجان', N'Hendijan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (660, 13, N'زهره', N'Zohreh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (661, 13, N'رامشیر', N'Ramshir')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (662, 13, N'مشراگه', N'Meshrageh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (663, 13, N'ترکالکی', N'Torkalaki')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (664, 13, N'سماله', N'Samaleh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (665, 13, N'گتوند', N'Gotvand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (666, 13, N'صالح شهر', N'Saleh Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (667, 13, N'جنت مکان', N'Jannat Makan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (668, 13, N'آبژدان', N'Abzhan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (669, 13, N'زاووت', N'Zavout')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (670, 13, N'قلعه خواجه', N'Qaleh Khvajeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (671, 13, N'هفتگل', N'Haftgel')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (672, 13, N'رفیع', N'Rofay')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (673, 13, N'هویزه', N'Hoveyzeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (674, 13, N'ملاثانی', N'Molasani')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (675, 13, N'ویس', N'Veys')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (676, 13, N'شیبان', N'Sheiban')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (677, 13, N'حمیدیه', N'Hamidiyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (678, 13, N'آغاجاری', N'Aghajari')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (679, 13, N'جولكی', N'Joolaki')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (680, 13, N'کوت عبداله', N'Kut-e Abdollah')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (681, 13, N'الوان', N'Elvan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (682, 13, N'شاوور', N'Shavur')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (683, 13, N'دهدز', N'Dehdez')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (684, 14, N'ابهر', N'Abhar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (685, 14, N'صایین قلعه', N'Sain Qaleh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (686, 14, N'هیدج', N'Hidaj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (687, 14, N'گرماب', N'Germab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (688, 14, N'زرین رود', N'Zarrin Rud')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (689, 14, N'قیدار', N'Qeydar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (690, 14, N'سهرورد', N'Sohrevard')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (691, 14, N'کرسف', N'Korasf')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (692, 14, N'نوربهار', N'Nourbahar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (693, 14, N'سجاس', N'Sajas')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (694, 14, N'نیک پی', N'Nik Pey')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (695, 14, N'زنجان', N'Zanjan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (696, 14, N'ارمغانخانه', N'Armaghankhaneh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (697, 14, N'حلب', N'Halab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (698, 14, N'زرین آباد', N'Zarrin Abad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (699, 14, N'خرمدره', N'Khorramdarreh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (700, 14, N'چورزق', N'Chavarzagh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (701, 14, N'آب بر', N'Ab Bar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (702, 14, N'دندی', N'Dandi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (703, 14, N'ماه نشان', N'Mah Neshan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (704, 14, N'سلطانیه', N'Soltaniyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (705, 15, N'امیریه', N'Amiriyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (706, 15, N'دامغان', N'Damghan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (707, 15, N'دیباج', N'Dibaj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (708, 15, N'کلاته', N'Kalateh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (709, 15, N'سمنان', N'Semnan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (710, 15, N'بسطام', N'Bastam')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (711, 15, N'مجن', N'Majan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (712, 15, N'كلاته خیج', N'Kalateh Khij')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (713, 15, N'بیارجمند', N'Beyarjomand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (714, 15, N'شاهرود', N'Shahroud')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (715, 15, N'رودیان', N'Roudian')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (716, 15, N'ایوانكی', N'Eyvanki')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (717, 15, N'گرمسار', N'Garmsar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (718, 15, N'شهمیرزاد', N'Shahmirzad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (719, 15, N'مهدی شهر', N'Mahdishahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (720, 15, N'درجزین', N'Darjazin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (721, 15, N'آرادان', N'Aradan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (722, 15, N'کهن آباد', N'Kohanabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (723, 15, N'میامی', N'Meyami')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (724, 15, N'رضوان', N'Rezvan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (725, 15, N'سرخه', N'Sorkheh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (726, 16, N'بزمان', N'Bazman')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (727, 16, N'ایرانشهر', N'Iranshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (728, 16, N'چاه بهار', N'Chabahar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (729, 16, N'پلان', N'Plan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (730, 16, N'خاش', N'Khash')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (731, 16, N'اسماعیل آباد', N'Esmaeilabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (732, 16, N'ده رییس', N'Deh Reyis')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (733, 16, N'زابل', N'Zabol')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (734, 16, N'بنجار', N'Bonjar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (735, 16, N'زاهدان', N'Zahedan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (736, 16, N'نصرت آباد', N'Nosratabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (737, 16, N'سرجنگل', N'Sarjangal')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (738, 16, N'سراوان', N'Saravan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (739, 16, N'محمدی', N'Mohammadi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (740, 16, N'گشت', N'Gasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (741, 16, N'سیركان', N'Sirkan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (742, 16, N'اسفندک', N'Espandak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (743, 16, N'بنت', N'Bent')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (744, 16, N'نیک شهر', N'Nikshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (745, 16, N'چانف', N'Chanf')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (746, 16, N'پیشین', N'Pishin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (747, 16, N'راسک', N'Rask')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (748, 16, N'پارود', N'Parood')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (749, 16, N'کنارک', N'Kenarak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (750, 16, N'جزینک', N'Jazinak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (751, 16, N'زهک', N'Zahak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (752, 16, N'دوست محمد', N'Doost Mohammad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (753, 16, N'قرقری', N'Qarqari')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (754, 16, N'گلمورتی', N'Gelmorti')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (755, 16, N'چگرد', N'Chegard')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (756, 16, N'مهرستان', N'Mehrestan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (757, 16, N'آشار', N'Ashar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (758, 16, N'سیب', N'Sib')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (759, 16, N'سوران', N'Soran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (760, 16, N'هیدوچ', N'Heydouch')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (761, 16, N'ادیمی', N'Adimi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (762, 16, N'محمدآباد', N'Mohammadabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (763, 16, N'علی اکبر', N'Ali Akbar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (764, 16, N'میرجاوه', N'Mirjaveh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (765, 16, N'ریگ ملک', N'Rig-e Malek')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (766, 16, N'قصرقند', N'Qasr-e Qand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (767, 16, N'ساربوک', N'Sarbuk')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (768, 16, N'فنوج', N'Fanouj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (769, 16, N'گتیج', N'Gateij')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (770, 16, N'محمدان', N'Mohammadan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (771, 16, N'بمپور', N'Bampur')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (772, 16, N'قاسم آباد', N'Qasemabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (773, 16, N'نوک آباد', N'Nookabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (774, 16, N'بریس', N'Beris')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (775, 16, N'نگور', N'Negur')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (776, 16, N'سرباز', N'Sarbaz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (777, 16, N'جالق', N'Jalq')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (778, 16, N'اسپکه', N'Espakeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (779, 16, N'زرآباد', N'Zarabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (780, 17, N'آباده', N'Abadeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (781, 17, N'ایزدخواست', N'Izadkhvast')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (782, 17, N'سورمق', N'Soormagh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (783, 17, N'صغاد', N'Soghad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (784, 17, N'بهمن', N'Bahman')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (785, 17, N'رونیز', N'Roniz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (786, 17, N'استهبان', N'Estahban')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (787, 17, N'ایج', N'Eij')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (788, 17, N'دژکرد', N'Dezhkord')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (789, 17, N'سده', N'Sedeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (790, 17, N'اقلید', N'Eqlid')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (791, 17, N'حسن آباد', N'Hasanabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (792, 17, N'دوزه', N'Dozeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (793, 17, N'قطب آباد', N'Qotbabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (794, 17, N'جهرم', N'Jahrom')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (795, 17, N'رستاق', N'Rastaq')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (796, 17, N'داراب', N'Darab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (797, 17, N'فدامی', N'Fadami')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (798, 17, N'دوبرجی', N'Doborji')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (799, 17, N'جنت شهر', N'Janat Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (800, 17, N'پاسخن', N'Pasokhan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (801, 17, N'اردکان', N'Ardekan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (802, 17, N'هماشهر', N'Homashahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (803, 17, N'شیراز', N'Shiraz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (804, 17, N'شهرصدرا', N'Shahre Sadra')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (805, 17, N'داریان', N'Daryan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (806, 17, N'خانه زنیان', N'Khaneh Zanian')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (807, 17, N'ششده', N'Sheshdeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (808, 17, N'قره بلاغ', N'Qarah Bolagh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (809, 17, N'زاهدشهر', N'Zahed Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (810, 17, N'میانشهر', N'Miyanshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (811, 17, N'فسا', N'Fasa')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (812, 17, N'نوبندگان', N'Nobandegan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (813, 17, N'فیروزآباد', N'Firouzabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (814, 17, N'میمند', N'Meymand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (815, 17, N'بالاده', N'Baladeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (816, 17, N'کنارتخته', N'Konar Takhteh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (817, 17, N'کازرون', N'Kazerun')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (818, 17, N'خشت', N'Khesht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (819, 17, N'لار', N'Lar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (820, 17, N'لطیفی', N'Latifi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (821, 17, N'خور', N'Khour')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (822, 17, N'دهکویه', N'Dehkuyyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (823, 17, N'بیرم', N'Beyram')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (824, 17, N'بنارویه', N'Banaruiyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (825, 17, N'عماد شهر', N'Emad Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (826, 17, N'کامفیروز', N'Kamfirouz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (827, 17, N'فتح آباد', N'Fathabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (828, 17, N'مرودشت', N'Marvdasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (829, 17, N'زنگی آباد', N'Zangi Abad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (830, 17, N'رامجرد', N'Ramjerd')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (831, 17, N'سیدان', N'Seydan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (832, 17, N'فاروق', N'Farough')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (833, 17, N'خانیمن', N'Khaniman')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (834, 17, N'بابامنیر', N'Baba Monir')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (835, 17, N'نورآباد', N'Nourabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (836, 17, N'خومه زار', N'Khumeh Zar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (837, 17, N'مشکان', N'Meshkan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (838, 17, N'نی ریز', N'Neyriz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (839, 17, N'قطرویه', N'Qatruyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (840, 17, N'لامرد', N'Lamerd')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (841, 17, N'اشکنان', N'Eshkanan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (842, 17, N'اهل', N'Ahl')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (843, 17, N'علامرودشت', N'Alamarvdasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (844, 17, N'چاه ورز', N'Chah Varz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (845, 17, N'خیرگو', N'Khirgoo')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (846, 17, N'بوانات', N'Bavanat')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (847, 17, N'مزایجان', N'Mezaijan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (848, 17, N'ارسنجان', N'Arsanjan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (849, 17, N'قادراباد', N'Qaderabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (850, 17, N'صفاشهر', N'Safashahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (851, 17, N'شهرپیر', N'Shahre Pir')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (852, 17, N'حاجی آباد', N'Hajiabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (853, 17, N'دبیران', N'Debiran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (854, 17, N'افزر', N'Afzar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (855, 17, N'قیر', N'Qir')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (856, 17, N'امام شهر', N'Emam Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (857, 17, N'مبارک آباددیز', N'Mobarak Abad-e Diz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (858, 17, N'کارزین (فتح آباد)', N'Karzin (Fath Abad)')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (859, 17, N'گله دار', N'Gelehdar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (860, 17, N'فال', N'Fal')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (861, 17, N'مهر', N'Mehr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (862, 17, N'وراوی', N'Varavi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (863, 17, N'خوزی', N'Khuzi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (864, 17, N'اسیر', N'Asir')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (865, 17, N'فراشبند', N'Farashband')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (866, 17, N'نوجین', N'Nowjin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (867, 17, N'دهرم', N'Dohram')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (868, 17, N'سعادت شهر', N'Saadat Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (869, 17, N'مادرسلیمان', N'Madar Soleyman')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (870, 17, N'محمله', N'Mahmaleh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (871, 17, N'خنج', N'Khonj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (872, 17, N'کوهنجان', N'Kohenjan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (873, 17, N'سروستان', N'Sarvestan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (874, 17, N'کوپن', N'Kopon')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (875, 17, N'مصیری', N'Masiri')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (876, 17, N'گراش', N'Gerash')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (877, 17, N'ارد', N'Ard')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (878, 17, N'اکبرآباد', N'Akbarabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (879, 17, N'مظفری', N'Mozaffari')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (880, 17, N'کوار', N'Kavar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (881, 17, N'طسوج', N'Tasuj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (882, 17, N'سلطان شهر', N'Soltan Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (883, 17, N'خرامه', N'Kherameh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (884, 17, N'معزابادجابری', N'Moaz Abad-e Jaberi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (885, 17, N'خیرآباد', N'Kheyrabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (886, 17, N'زرقان', N'Zarqan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (887, 17, N'لپویی', N'Lapui')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (888, 17, N'رحمت آباد', N'Rahmatabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (889, 17, N'بیضا', N'Beyza')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (890, 17, N'حسامی', N'Hessami')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (891, 17, N'کره ای', N'Korei')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (892, 17, N'توجردی', N'Tojordi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (893, 17, N'قایمیه', N'Qaemieh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (894, 17, N'نودان', N'Nowdan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (895, 17, N'باب انار', N'Baba Anar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (896, 17, N'خاوران', N'Khavaran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (897, 17, N'آباده طشک', N'Abadeh Tashk')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (898, 17, N'اوز', N'Evaz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (899, 17, N'کوره', N'Koreh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (900, 17, N'جویم', N'Juyom')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (901, 18, N'دانسفهان', N'Danesfahan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (902, 18, N'شال', N'Shal')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (903, 18, N'بویین زهرا', N'Buin Zahra')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (904, 18, N'سگزآباد', N'Sagezabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (905, 18, N'عصمت آباد', N'Esmatabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (906, 18, N'ارداق', N'Ardak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (907, 18, N'اسفرورین', N'Esfarvarin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (908, 18, N'خرمدشت', N'Khorramdasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (909, 18, N'ضیاآباد', N'Ziaabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (910, 18, N'تاكستان', N'Takestan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (911, 18, N'نرجه', N'Narjeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (912, 18, N'معلم كلایه', N'Moallem Kolaieh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (913, 18, N'رازمیان', N'Razmian')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (914, 18, N'سیردان', N'Sirdan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (915, 18, N'قزوین', N'Qazvin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (916, 18, N'اقبالیه', N'Eqbaliyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (917, 18, N'محمودآبادنمونه', N'Mahmoodabad Nemuneh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (918, 18, N'كوهین', N'Kuhin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (919, 18, N'خاكعلی', N'Khakali')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (920, 18, N'آبیك', N'Abyek')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (921, 18, N'زیاران', N'Ziaran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (922, 18, N'قشلاق', N'Qeshlaq')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (923, 18, N'شریفیه', N'Sharifieh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (924, 18, N'محمدیه', N'Mohammadieh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (925, 18, N'بیدستان', N'Bidestan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (926, 18, N'الوند', N'Alvand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (927, 18, N'آوج', N'Avaj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (928, 18, N'آبگرم', N'Abgarm')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (929, 19, N'دستجرد', N'Dastjerd')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (930, 19, N'قم', N'Qom')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (931, 19, N'قنوات', N'Ghanoat')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (932, 19, N'سلفچگان', N'Salafchegan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (933, 19, N'جعفریه', N'Jafariyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (934, 19, N'کهک', N'Kahak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (935, 20, N'آرمرده', N'Armardeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (936, 20, N'بانه', N'Baneh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (937, 20, N'كانی سور', N'Kaneh Sur')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (938, 20, N'بویین سفلی', N'Buin Sofla')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (939, 20, N'بابرشانی', N'Babarshani')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (940, 20, N'پیرتاج', N'Pirtaj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (941, 20, N'یاسوكند', N'Yasou Kand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (942, 20, N'بیجار', N'Bijar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (943, 20, N'توپ آغاج', N'Tup Aghaj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (944, 20, N'صاحب', N'Saheb')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (945, 20, N'سقز', N'Saqqez')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (946, 20, N'سنته', N'Sanateh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (947, 20, N'سنندج', N'Sanandaj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (948, 20, N'شویشه', N'Shuyesheh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (949, 20, N'حسین آباد', N'Hoseynabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (950, 20, N'قروه', N'Qorveh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (951, 20, N'سریش آباد', N'Serishabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (952, 20, N'دزج', N'Dezaj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (953, 20, N'مالوجه', N'Maloujeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (954, 20, N'دلبران', N'Delbaran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (955, 20, N'برده رشه', N'Bardeh Rasheh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (956, 20, N'چناره', N'Chenareh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (957, 20, N'مریوان', N'Marivan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (958, 20, N'كانی دینار', N'Kaneh Dinar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (959, 20, N'زرینه', N'Zarineh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (960, 20, N'دیواندره', N'Divandarreh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (961, 20, N'هزارکانیان', N'Hezar Kanian')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (962, 20, N'كامیاران', N'Kamyaran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (963, 20, N'موچش', N'Mouchesh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (964, 20, N'اورامان تخت', N'Oraman Takht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (965, 20, N'سروآباد', N'Sarvabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (966, 20, N'دهگلان', N'Dehgolan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (967, 20, N'بلبان آباد', N'Balabanabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (968, 21, N'بافت', N'Baft')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (969, 21, N'بزنجان', N'Bezenjan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (970, 21, N'کشکوییه', N'Kashkuiyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (971, 21, N'بم', N'Bam')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (972, 21, N'بروات', N'Baravat')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (973, 21, N'درب بهشت', N'Darbe Behesht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (974, 21, N'جبالبارز', N'Jebalbarez')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (975, 21, N'جیرفت', N'Jiroft')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (976, 21, N'علی آباد', N'Aliabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (977, 21, N'بلوک', N'Boluk')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (978, 21, N'رفسنجان', N'Rafsanjan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (979, 21, N'مس سرچشمه', N'Mes-e Sarcheshmeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (980, 21, N'بهرمان', N'Bahreman')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (981, 21, N'جوادیه الهیه', N'Javadiyeh Elahiyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (982, 21, N'صفاییه', N'Safaieh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (983, 21, N'زرند', N'Zarand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (984, 21, N'خانوک', N'Khanouk')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (985, 21, N'ریحان', N'Reyhan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (986, 21, N'یزدان شهر', N'Yazdan Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (987, 21, N'سیرجان', N'Sirjan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (988, 21, N'نجف شهر', N'Najaf Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (989, 21, N'پاریز', N'Pariz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (990, 21, N'هماشهر', N'Homashahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (991, 21, N'خواجو شهر', N'Khajoo Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (992, 21, N'زیدآباد', N'Zeydabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (993, 21, N'بلورد', N'Balvard')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (994, 21, N'شهربابک', N'Shahr-e Babak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (995, 21, N'خورسند', N'Khorsand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (996, 21, N'خاتون آباد', N'Khatoonabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (997, 21, N'جوزم', N'Jowzam')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (998, 21, N'دهج', N'Dehaj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (999, 21, N'شهداد', N'Shahdad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1000, 21, N'اندوهجرد', N'Anduhjerd')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1001, 21, N'گلباف', N'Golbaf')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1002, 21, N'جوپار', N'Joopar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1003, 21, N'ماهان', N'Mahan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1004, 21, N'محی آباد', N'Mahiabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1005, 21, N'کرمان', N'Kerman')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1006, 21, N'باغین', N'Baghin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1007, 21, N'زنگی آباد', N'Zangiabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1008, 21, N'اختیارآباد', N'Ekhtiyarabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1009, 21, N'راین', N'Rayen')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1010, 21, N'چترود', N'Chatrood')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1011, 21, N'کاظم آباد', N'Kazemabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1012, 21, N'کهنوج', N'Kahnooj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1013, 21, N'ده کهان', N'Deh Kahan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1014, 21, N'چاه مرید', N'Chah Morid')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1015, 21, N'بردسیر', N'Bardsir')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1016, 21, N'دشتکار', N'Dashtkar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1017, 21, N'لاله زار', N'Lalehzar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1018, 21, N'گلزار', N'Golzar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1019, 21, N'نگار', N'Negar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1020, 21, N'هجدک', N'Hajdak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1021, 21, N'راور', N'Ravar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1022, 21, N'عنبرآباد', N'Anbarabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1023, 21, N'دوساری', N'Dow Sari')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1024, 21, N'مردهک', N'Mordehk')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1025, 21, N'منوجان', N'Manujan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1026, 21, N'نودژ', N'Nowdezh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1027, 21, N'کیانشهر', N'Kianshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1028, 21, N'کوهبنان', N'Koohbanan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1029, 21, N'زهکلوت', N'Zahkalut')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1030, 21, N'رودبار', N'Rudbar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1031, 21, N'چاه دادخدا', N'Chah Dadkhoda')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1032, 21, N'رمشک', N'Rameshk')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1033, 21, N'قلعه گنج', N'Qaleh Ganj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1034, 21, N'گنبکی', N'Gonbaki')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1035, 21, N'رحمت آباد', N'Rahmatabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1036, 21, N'عباس آباد سردار', N'Abbasabad Sardar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1037, 21, N'محمدآباد', N'Mohammadabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1038, 21, N'رابر', N'Rabor')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1039, 21, N'هنزا', N'Honza')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1040, 21, N'فهرج', N'Fahraj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1041, 21, N'دهنو اسلام آباد', N'Dehno Eslamabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1042, 21, N'انار', N'Anar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1043, 21, N'امین شهر', N'Amin Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1044, 21, N'نرماشیر', N'Narmashir')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1045, 21, N'نظام شهر', N'Nezamshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1046, 21, N'فاریاب', N'Fariab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1047, 21, N'پاسفید', N'Pasfied')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1048, 21, N'ارزوییه', N'Orzueeyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1049, 21, N'علی آباد', N'Aliabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1050, 22, N'حمیل', N'Hamil')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1051, 22, N'اسلام آبادغرب', N'Eslamabad-e Gharb')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1052, 22, N'هلشی', N'Holashi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1053, 22, N'کرمانشاه', N'Kermanshah')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1054, 22, N'رباط', N'Robat')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1055, 22, N'کوزران', N'Kozaran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1056, 22, N'قلعه', N'Ghaleh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1057, 22, N'باینگان', N'Bayangan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1058, 22, N'بانوره', N'Banureh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1059, 22, N'پاوه', N'Paveh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1060, 22, N'نودشه', N'Nowsud')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1061, 22, N'نوسود', N'Nowsud')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1062, 22, N'سرپل ذهاب', N'Sarpol-e Zahab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1063, 22, N'سنقر', N'Sonqor')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1064, 22, N'سطر', N'Satar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1065, 22, N'سومار', N'Soumar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1066, 22, N'قصرشیرین', N'Qasr-e Shirin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1067, 22, N'کنگاور', N'Kangavar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1068, 22, N'گودین', N'Gowdin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1069, 22, N'گیلانغرب', N'Gilan-e Gharb')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1070, 22, N'سرمست', N'Sarmast')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1071, 22, N'جوانرود', N'Javanrud')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1072, 22, N'شروینه', N'Sharvineh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1073, 22, N'دینور', N'Dinavar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1074, 22, N'صحنه', N'Sahneh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1075, 22, N'بیستون', N'Bisotun')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1076, 22, N'هرسین', N'Harsin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1077, 22, N'تازه آباد', N'Tazehabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1078, 22, N'ازگله', N'Ezgeleh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1079, 22, N'میرآباد', N'Mirabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1080, 22, N'گهواره', N'Gahvareh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1081, 22, N'کرند', N'Karand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1082, 22, N'ریجاب', N'Rijab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1083, 22, N'شاهو', N'Shaho')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1084, 22, N'روانسر', N'Ravansar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1085, 23, N'یاسوج', N'Yasuj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1086, 23, N'مادوان', N'Madavan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1087, 23, N'گراب سفلی', N'Gerab Sofla')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1088, 23, N'چیتاب', N'Chitab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1089, 23, N'قلعه رییسی', N'Ghaleh Raisi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1090, 23, N'دهدشت', N'Dehdasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1091, 23, N'دیشموك', N'Dishmok')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1092, 23, N'سوق', N'Suq')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1093, 23, N'دوگنبدان', N'Dogonbadan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1094, 23, N'پاتاوه', N'Pataveh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1095, 23, N'سی سخت', N'Sisakht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1096, 23, N'لیكك', N'Likak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1097, 23, N'چرام', N'Choram')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1098, 23, N'سرفاریاب', N'Sarfariab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1099, 23, N'باشت', N'Basht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1100, 23, N'بوستان', N'Boostan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1101, 23, N'لنده', N'Landeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1102, 23, N'مارگون', N'Margon')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1103, 24, N'بندرگز', N'Bandar-e Gaz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1104, 24, N'نوكنده', N'Nowkandeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1105, 24, N'بندرتركمن', N'Bandar-e Torkaman')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1106, 24, N'سیجوال', N'Siyajual')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1107, 24, N'علی آباد', N'Aliabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1108, 24, N'مزرعه', N'Mazraeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1109, 24, N'سنگدوین', N'Sangdevin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1110, 24, N'فاضل آباد', N'Fazelabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1111, 24, N'كردكوی', N'Kordkuy')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1112, 24, N'گرگان', N'Gorgan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1113, 24, N'جلین', N'Jelin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1114, 24, N'سرخنكلاته', N'Sarkhon Kalateh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1115, 24, N'قرق', N'Qarq')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1116, 24, N'كرند', N'Karand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1117, 24, N'اینچه برون', N'Incheboron')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1118, 24, N'گنبدكاووس', N'Gonbad-e Kavus')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1119, 24, N'مینودشت', N'Minudasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1120, 24, N'دوزین', N'Dozin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1121, 24, N'انبارآلوم', N'Anbar Alum')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1122, 24, N'آق قلا', N'Aqqala')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1123, 24, N'كلاله', N'Kalaleh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1124, 24, N'فراغی', N'Faraghi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1125, 24, N'نوده خاندوز', N'Nowdeh Khanduz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1126, 24, N'آزادشهر', N'Azadshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1127, 24, N'نگین شهر', N'Neginshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1128, 24, N'خان ببین', N'Khanbebin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1129, 24, N'رامین', N'Ramian')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1130, 24, N'دلند', N'Daland')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1131, 24, N'تاتارعلیا', N'Tatar-e Olya')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1132, 24, N'مراوه', N'Maraveh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1133, 24, N'گلیداغ', N'Galidagh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1134, 24, N'گمیش تپه', N'Gomishan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1135, 24, N'سیمین شهر', N'Siminshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1136, 24, N'گالیكش', N'Galikesh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1137, 24, N'صادق اباد', N'Sadeqabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1138, 25, N'آستارا', N'Astara')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1139, 25, N'لوندویل', N'Lavandevil')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1140, 25, N'كیاشهر', N'Kiashahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1141, 25, N'آستانه اشرفیه', N'Astaneh Ashrafieh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1142, 25, N'بندرانزلی', N'Bandar-e Anzali')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1143, 25, N'هشتپر (تالش)', N'Hashtpar (Talesh)')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1144, 25, N'لیسار', N'Lissar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1145, 25, N'اسالم', N'Asalem')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1146, 25, N'حویق', N'Havigh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1147, 25, N'چوبر', N'Chobar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1148, 25, N'سنگر', N'Sangar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1149, 25, N'کوچصفهان', N'Kuchesfahan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1150, 25, N'لولمان', N'Lulaman')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1151, 25, N'لشت نشاء', N'Lashtenesha')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1152, 25, N'پیربازار', N'Pirbazar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1153, 25, N'رشت', N'Rasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1154, 25, N'خشكبیجار', N'Khoshkebijar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1155, 25, N'توتكابن', N'Tutkabon')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1156, 25, N'جیرنده', N'Jirandeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1157, 25, N'لوشان', N'Lowshan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1158, 25, N'رودبار', N'Rudbar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1159, 25, N'منجیل', N'Manjil')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1160, 25, N'رستم آباد', N'Rostamabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1161, 25, N'بره سر', N'Barehsar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1162, 25, N'رحیم آباد', N'Rahimabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1163, 25, N'رودسر', N'Rudsar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1164, 25, N'چابكسر', N'Chaboksar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1165, 25, N'كلاچای', N'Kelachay')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1166, 25, N'واجارگاه', N'Vajaargah')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1167, 25, N'مرجقل', N'Marjaghal')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1168, 25, N'صومعه سرا', N'Someh Sara')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1169, 25, N'گوراب زرمیخ', N'Gurab Zarmikh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1170, 25, N'طاهرگوراب', N'Taher Gurab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1171, 25, N'ضیابر', N'Ziyabar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1172, 25, N'فومن', N'Fouman')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1173, 25, N'ماسوله', N'Masuleh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1174, 25, N'ماکلوان', N'Maklavan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1175, 25, N'لنگرود', N'Langarud')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1176, 25, N'چاف و چمخاله', N'Chaf va Chamkhaleh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1177, 25, N'اطاقور', N'Otaghvar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1178, 25, N'كومله', N'Komleh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1179, 25, N'شلمان', N'Shalman')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1180, 25, N'لاهیجان', N'Lahijan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1181, 25, N'رودبنه', N'Rudbeneh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1182, 25, N'احمدسرگوراب', N'Ahmad Sar Gorab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1183, 25, N'شفت', N'Shaft')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1184, 25, N'رانكوه', N'Rankuh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1185, 25, N'املش', N'Amlash')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1186, 25, N'پره سر', N'Pareh Sar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1187, 25, N'رضوانشهر', N'Rezvanshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1188, 25, N'دیلمان', N'Deylaman')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1189, 25, N'سیاهكل', N'Siahkal')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1190, 25, N'بازار جمعه', N'Bazaar Jomeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1191, 25, N'ماسال', N'Masal')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1192, 25, N'خمام', N'Khomam')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1193, 25, N'چوکام', N'Chowkam')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1194, 26, N'شول آباد', N'Shulabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1195, 26, N'الیگودرز', N'Aligudarz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1196, 26, N'تیتکان بزنوید', N'Titkan Baznavid')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1197, 26, N'شاهپورآباد', N'Shahpourabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1198, 26, N'چمن سلطان', N'Chaman Sultan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1199, 26, N'اشترینان', N'Oshtorinan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1200, 26, N'ونایی', N'Vanaei')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1201, 26, N'بروجرد', N'Borujerd')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1202, 26, N'سپیددشت', N'Sepiddasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1203, 26, N'بیران شهر', N'Beyranshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1204, 26, N'زاغه', N'Zagheh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1205, 26, N'خرم آباد', N'Khorramabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1206, 26, N'هفت چشمه', N'Haft Cheshmeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1207, 26, N'نورآباد', N'Nourabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1208, 26, N'برخوردار', N'Barkhordar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1209, 26, N'چالانچولان', N'Chalan Chulan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1210, 26, N'دورود', N'Dorud')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1211, 26, N'گراب', N'Gerab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1212, 26, N'کوهدشت', N'Kuhdasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1213, 26, N'کوهنانی', N'Kohnani')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1214, 26, N'درب گنبد', N'Darb Gonbad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1215, 26, N'مومن آباد', N'Momenabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1216, 26, N'ازنا', N'Azna')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1217, 26, N'پلدختر', N'Poldokhtar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1218, 26, N'سراب حمام', N'Sarab Hamam')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1219, 26, N'معمولان', N'Mamulan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1220, 26, N'فیروزآباد', N'Firouzabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1221, 26, N'الشتر', N'Alishtar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1222, 26, N'سراب دوره', N'Sarab Dowreh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1223, 26, N'چم پلک', N'Cham Pelak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1224, 26, N'ویسیان', N'Veysian')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1225, 26, N'سوری', N'Suri')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1226, 26, N'چقابل', N'Chaghalv')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1227, 27, N'رینه', N'Rineh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1228, 27, N'گزنك', N'Gazanak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1229, 27, N'آمل', N'Amol')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1230, 27, N'دابودشت', N'Dabudasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1231, 27, N'امامزاده عبدالله', N'Emamzadeh Abdullah')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1232, 27, N'بابکان', N'Babakan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1233, 27, N'خوش رودپی', N'Khosh Roudpey')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1234, 27, N'امیركلا', N'Amirkola')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1235, 27, N'بابل', N'Babol')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1236, 27, N'گلوگاه', N'Galugah')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1237, 27, N'مرزیكلا', N'Marzikola')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1238, 27, N'زرگر', N'Zargar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1239, 27, N'گتاب', N'Gatab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1240, 27, N'بهشهر', N'Behshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1241, 27, N'رستمكلا', N'Rostamkola')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1242, 27, N'خلیل شهر', N'Khalilshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1243, 27, N'شیرود', N'Shiroud')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1244, 27, N'تنكابن', N'Tonekabon')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1245, 27, N'نشتارود', N'Nashtaroud')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1246, 27, N'خرم آباد', N'Khorramabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1247, 27, N'رامسر', N'Ramsar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1248, 27, N'كتالم وسادات شهر', N'Ketalem and Sadat Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1249, 27, N'كیاسر', N'Kiasar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1250, 27, N'فریم', N'Farim')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1251, 27, N'ساری', N'Sari')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1252, 27, N'پایین هولار', N'Payin Holar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1253, 27, N'اكند', N'Ekand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1254, 27, N'فرح آباد', N'Farahabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1255, 27, N'آلاشت', N'Alasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1256, 27, N'پل سفید', N'Pol Sefid')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1257, 27, N'زیرآب', N'Zirab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1258, 27, N'قایم شهر', N'Qaemshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1259, 27, N'ارطه', N'Arateh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1260, 27, N'بلده', N'Baladeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1261, 27, N'چمستان', N'Chamestan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1262, 27, N'نور', N'Noor')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1263, 27, N'رویان', N'Royan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1264, 27, N'ایزدشهر', N'Izadshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1265, 27, N'پول', N'Pul')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1266, 27, N'کجور', N'Kojour')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1267, 27, N'نوشهر', N'Nowshahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1268, 27, N'بابلسر', N'Babolsar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1269, 27, N'بهنمیر', N'Beh Namir')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1270, 27, N'هادی شهر', N'Hadi Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1271, 27, N'سرخرود', N'Sarkhroud')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1272, 27, N'محمودآباد', N'Mahmoudabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1273, 27, N'نكا', N'Neka')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1274, 27, N'چالوس', N'Chalus')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1275, 27, N'هچیرود', N'Hachiroud')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1276, 27, N'مرزن آباد', N'Marzanabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1277, 27, N'كوهی خیل', N'Kouhi Khil')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1278, 27, N'جویبار', N'Juybar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1279, 27, N'گلوگاه', N'Galugah')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1280, 27, N'آستانه سرا', N'Astaneh Sara')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1281, 27, N'فریدونكنار', N'Fereydunkenar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1282, 27, N'عباس اباد', N'Abbasabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1283, 27, N'سلمان شهر', N'Salman Shahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1284, 27, N'کلارآباد', N'Kelarabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1285, 27, N'سورك', N'Surak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1286, 27, N'طبقده', N'Tabaqdeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1287, 27, N'كیاكلا', N'Kiakola')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1288, 27, N'شیرگاه', N'Shirgah')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1289, 27, N'كلاردشت', N'Kelardasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1290, 28, N'اراک', N'Arak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1291, 28, N'داودآباد', N'Davoudabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1292, 28, N'ساروق', N'Saruq')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1293, 28, N'کارچان', N'Karchan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1294, 28, N'آشتیان', N'Ashtian')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1295, 28, N'تفرش', N'Tafresh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1296, 28, N'خمین', N'Khomein')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1297, 28, N'قورچی باشی', N'Qurchebashi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1298, 28, N'دلیجان', N'Delijan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1299, 28, N'نراق', N'Naragh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1300, 28, N'ساوه', N'Saveh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1301, 28, N'آوه', N'Aveh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1302, 28, N'غرق آباد', N'Gharqabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1303, 28, N'نوبران', N'Nowbaran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1304, 28, N'آستانه', N'Astaneh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1305, 28, N'شازند', N'Shazand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1306, 28, N'هندودر', N'Hendudar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1307, 28, N'مهاجران', N'Mohajeran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1308, 28, N'توره', N'Tureh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1309, 28, N'شهباز', N'Shahbaz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1310, 28, N'محلات', N'Mahallat')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1311, 28, N'نیمور', N'Nimvar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1312, 28, N'رازقان', N'Razqan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1313, 28, N'مامونیه', N'Mamuniyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1314, 28, N'خشکرود', N'Khoshkrud')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1315, 28, N'پرندک', N'Parandak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1316, 28, N'زاویه', N'Zaviyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1317, 28, N'کمیجان', N'Komijan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1318, 28, N'میلاجرد', N'Milajerd')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1319, 28, N'جاورسیان', N'Javeresian')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1320, 28, N'خنداب', N'Khandab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1321, 28, N'فرمهین', N'Farahan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1322, 28, N'خنجین', N'Khanjin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1323, 28, N'تلخاب', N'Talkhab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1324, 29, N'ابوموسی', N'Abu Musa')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1325, 29, N'فین', N'Fin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1326, 29, N'بندرعباس', N'Bandar Abbas')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1327, 29, N'تازیان پایین', N'Tazian-e Pain')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1328, 29, N'تخت', N'Takht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1329, 29, N'قلعه قاضی', N'Qaleh Qazi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1330, 29, N'هرمز', N'Hormuz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1331, 29, N'چارك', N'Chark')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1332, 29, N'كیش', N'Kish')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1333, 29, N'كنگ', N'Kong')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1334, 29, N'بندرلنگه', N'Bandar Lengeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1335, 29, N'لمزان', N'Lamazan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1336, 29, N'سوزا', N'Suza')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1337, 29, N'رمكان', N'Ramkan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1338, 29, N'لافت', N'Laft')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1339, 29, N'قشم', N'Qeshm')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1340, 29, N'درگهان', N'Dargahan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1341, 29, N'طبل', N'Tabl')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1342, 29, N'سندرك', N'Senderk')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1343, 29, N'میناب', N'Minab')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1344, 29, N'تیرور', N'Tirur')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1345, 29, N'هشتبندی', N'Hashtbandi')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1346, 29, N'زهوكی', N'Zahuki')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1347, 29, N'كرگان', N'Kargan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1348, 29, N'بندزرک', N'Bandar Zarak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1349, 29, N'بندرجاسك', N'Bandar Jask')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1350, 29, N'لیردف', N'Lirdaf')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1351, 29, N'زیارتعلی', N'Ziarat Ali')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1352, 29, N'دهبارز', N'Dehbarez')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1353, 29, N'بالاشهر', N'Balashahr')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1354, 29, N'بیکاء', N'Bika')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1355, 29, N'فارغان', N'Farghan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1356, 29, N'حاجی اباد', N'Hajiabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1357, 29, N'سرگز', N'Sargaz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1358, 29, N'جناح', N'Janah')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1359, 29, N'هنگوییه', N'Henguiyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1360, 29, N'بستك', N'Bastak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1361, 29, N'کوهیچ', N'Kuhij')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1362, 29, N'رویدر', N'Ruydar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1363, 29, N'خمیر', N'Khamir')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1364, 29, N'پل', N'Pol')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1365, 29, N'كوشكنار', N'Kushknar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1366, 29, N'پارسیان', N'Parsian')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1367, 29, N'دشتی', N'Dashti')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1368, 29, N'کوهستک', N'Kuhestak')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1369, 29, N'سیریك', N'Sirik')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1370, 29, N'گروک', N'Gerouk')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1371, 29, N'سردشت', N'Sardasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1372, 29, N'گوهران', N'Gowharan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1373, 30, N'فرسفج', N'Farsafaj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1374, 30, N'تویسركان', N'Tuyserkan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1375, 30, N'سركان', N'Sarkan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1376, 30, N'ازندریان', N'Azandarian')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1377, 30, N'جوكار', N'Jowkar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1378, 30, N'سامن', N'Samen')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1379, 30, N'ملایر', N'Malayer')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1380, 30, N'اسلام شهر آق گل', N'Eslamshahr Aq Gol')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1381, 30, N'زنگنه', N'Zangeneh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1382, 30, N'فیروزان', N'Firuzan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1383, 30, N'نهاوند', N'Nahavand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1384, 30, N'برزول', N'Barzul')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1385, 30, N'گیان', N'Giyan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1386, 30, N'قهاوند', N'Qahavand')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1387, 30, N'مریانج', N'Maryanaj')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1388, 30, N'همدان', N'Hamedan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1389, 30, N'جورقان', N'Jourqan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1390, 30, N'گل تپه', N'Gol Tappeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1391, 30, N'کبودرآهنگ', N'Kabudrahang')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1392, 30, N'شیرین سو', N'Shirin Su')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1393, 30, N'اسدآباد', N'Asadabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1394, 30, N'پالیز', N'Paliz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1395, 30, N'آجین', N'Ajin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1396, 30, N'لالجین', N'Lalejin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1397, 30, N'مهاجران', N'Mohajeran')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1398, 30, N'بهار', N'Bahar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1399, 30, N'صالح آباد', N'Salehabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1400, 30, N'دمق', N'Damaq')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1401, 30, N'رزن', N'Razan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1402, 30, N'فامنین', N'Famenin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1403, 30, N'کرفس', N'Karafs')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1404, 30, N'قروه درگزین', N'Qorveh Darjazin')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1405, 31, N'خرانق', N'Kharanaq')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1406, 31, N'اردكان', N'Ardakan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1407, 31, N'احمدآباد', N'Ahmadabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1408, 31, N'عقدا', N'Aqda')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1409, 31, N'بافق', N'Bafq')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1410, 31, N'تفت', N'Taft')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1411, 31, N'نیر', N'Nir')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1412, 31, N'بخ', N'Bakh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1413, 31, N'مهریز', N'Mehriz')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1414, 31, N'یزد_منطقه تاریخی', N'Yazd_Historical Region')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1415, 31, N'یزد', N'Yazd')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1416, 31, N'شاهدیه', N'Shahedieh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1417, 31, N'حمیدیا', N'Hamidia')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1418, 31, N'میبد', N'Meybod')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1419, 31, N'ندوشن', N'Nodoushan')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1420, 31, N'بفروییه', N'Bafrooyeh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1421, 31, N'مهردشت', N'Mehrdasht')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1422, 31, N'ابركوه', N'Abarkooh')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1423, 31, N'خضرآباد', N'Khezrabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1424, 31, N'اشكذر', N'Ashkezar')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1425, 31, N'مجومرد', N'Majomerd')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1426, 31, N'هرات', N'Herat')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1427, 31, N'بهاباد', N'Bahabad')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1428, 31, N'مروست', N'Marvast')
GO
INSERT [Cities] ([ID], [ProvinceID], [Title], [LatinTitle]) VALUES (1429, 31, N'زارچ', N'Zarach')
GO
SET IDENTITY_INSERT [Cities] OFF
GO
SET IDENTITY_INSERT [Provinces] ON 
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (1, N'آذربایجان شرقی', N'East Azerbaijan', N'041')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (2, N'آذربایجان غربی', N'West Azerbaijan', N'044')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (3, N'اردبیل', N'Ardabil', N'045')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (4, N'اصفهان', N'Isfahan', N'031')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (5, N'البرز', N'Alborz', N'026')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (6, N'ایلام', N'Ilam', N'084')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (7, N'بوشهر', N'Bushehr', N'077')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (8, N'تهران', N'Tehran', N'021')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (9, N'چهارمحال و بختیاری', N'Chaharmahal and Bakhtiari', N'038')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (10, N'خراسان جنوبی', N'South Khorasan', N'056')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (11, N'خراسان رضوی', N'Razavi Khorasan', N'051')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (12, N'خراسان شمالی', N'North Khorasan', N'058')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (13, N'خوزستان', N'Khuzestan', N'061')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (14, N'زنجان', N'Zanjan', N'024')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (15, N'سمنان', N'Semnan', N'023')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (16, N'سیستان و بلوچستان', N'Sistan and Baluchestan', N'054')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (17, N'فارس', N'Fars', N'071')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (18, N'قزوین', N'Qazvin', N'028')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (19, N'قم', N'Qom', N'025')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (20, N'کردستان', N'Kurdistan', N'087')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (21, N'کرمان', N'Kerman', N'034')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (22, N'کرمانشاه', N'Kermanshah', N'083')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (23, N'کهگیلویه و بویراحمد', N'Kohgiluyeh and Boyer-Ahmad', N'074')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (24, N'گلستان', N'Golestan', N'017')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (25, N'گیلان', N'Gilan', N'013')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (26, N'لرستان', N'Lorestan', N'066')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (27, N'مازندران', N'Mazandaran', N'011')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (28, N'مرکزی', N'Markazi', N'086')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (29, N'هرمزگان', N'Hormozgan', N'076')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (30, N'همدان', N'Hamedan', N'081')
GO
INSERT [Provinces] ([ID], [Title], [LatinTitle], [AreaCode]) VALUES (31, N'یزد', N'Yazd', N'035')
GO
SET IDENTITY_INSERT [Provinces] OFF
GO
ALTER TABLE [Cities]  WITH CHECK ADD  CONSTRAINT [FK_Cities_ProvinceID] FOREIGN KEY([ProvinceID])
REFERENCES [Provinces] ([ID])
GO
ALTER TABLE [Cities] CHECK CONSTRAINT [FK_Cities_ProvinceID]
GO

```

- Just copy and paste this script into your SQL Server management tool and run it. ^_^

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
