# 🤲 DeenOne Dua API

> Official open-source Islamic Dua & Supplications API and comprehensive dataset for **DeenOne** (বাংলা ও ইংরেজি অর্থসহ কুরআন ও সুন্নাহর প্রামাণ্য দোয়া ভাণ্ডার).

---

## ✨ Features

- 📖 **৪২১টি প্রামাণ্য দোয়া (421 Authentic Duas)** from Hisnul Muslim and the Holy Quran
- 🕌 **খাঁটি আরবি ইবারত (Full Arabic with Tashkeel)** styled for authentic Quranic calligraphy
- 🇧🇩 **সহজ ও বিশুদ্ধ বাংলা অর্থ (Accurate Bengali Translations)**
- 🇬🇧 **English Translations** for every supplication
- 🔤 **বিশুদ্ধ বাংলা উচ্চারণ (Bengali Transliteration)**
- 🗂️ **১৮টি প্রধান ক্যাটাগরি (18 Topic Categories)**:
  - ঘুম ও জাগ্রত (Sleep & Waking Up)
  - সকাল - সন্ধ্যা (Morning & Evening)
  - সালাত ও যিক্‌র (Salah & Dhikr)
  - আশ্রয় ও হেফাজত (Protection & Refuge)
  - কুরআনের দোয়া (Quranic Duas)
  - অসুস্থতা ও মৃত্যু (Illness & Death)
  - সামাজিক শিষ্টাচার (Social & Ettiquette)
  - শুকরিয়া ও তওবা (Gratitude & Repentance)
  - সম্পত্তি ও রিজিক (Wealth & Sustenance)
  - সফর ও ভ্রমণ (Travel & Journey)
  - পিতামাতা ও পরিবার (Parents & Family)
  - প্রকৃতি ও আবহাওয়া (Nature & Weather)
  - রমাদান ও সিয়াম (Ramadan & Fasting)
  - হজ্জ ও উমরা (Hajj & Umrah)
  - রুকইয়াহ ও ঝাড়ফুঁক (Ruqyah)
  - খাদ্য ও পানীয় (Food & Drink)
  - পবিত্রতা ও অজু (Purification & Wudu)
  - পোশাক পরিধান (Clothes & Dressing)
- 🔍 **রিয়েল-টাইম অনুসন্ধান (Real-Time Search)** in Bengali, English, Arabic, and Tags
- ⚡ **জিরো ল্যাগ ও অফলাইন ক্যাশিং (Instant Offline Caching)**

---

## 📁 Repository Structure

```text
dua-api/
├── hisnul_muslim_all_duas.json   # Full compiled dataset (18 categories, 421 authentic duas)
├── category.csv                  # 18 authentic categories
├── duanames.csv                  # Dua names, chapter associations, tags
├── duadetails.csv                # Full Arabic text, pronunciation, Bengali & English meanings, references
├── src/
│   └── index.ts                  # Cloudflare Worker / Hono API service
├── wrangler.jsonc                # Cloudflare Worker configuration
└── README.md
```

---

## 📡 Live Raw Dataset Endpoints

For direct raw integration without third-party dependencies:

- **Complete JSON Dataset:**
  ```text
  https://raw.githubusercontent.com/riadmonir/dua-api/main/hisnul_muslim_all_duas.json
  ```
- **Categories CSV:**
  ```text
  https://raw.githubusercontent.com/riadmonir/dua-api/main/category.csv
  ```
- **Duas CSV:**
  ```text
  https://raw.githubusercontent.com/riadmonir/dua-api/main/duanames.csv
  ```
- **Details & Translations CSV:**
  ```text
  https://raw.githubusercontent.com/riadmonir/dua-api/main/duadetails.csv
  ```

---

## 🗄️ Dua Schema

Each Dua item in `hisnul_muslim_all_duas.json` has the following structure:

```json
{
  "global_id": 2,
  "category_id": 1,
  "category_name": "ঘুম ও জাগ্রত",
  "name": "ঘুম থেকে জেগে উঠার সময়ের যিক্‌রসমূহ #১",
  "chapter": "ঘুম থেকে জেগে উঠার সময়ের যিক্‌রসমূহ",
  "tags": "ঘুম উঠা জেগে",
  "arabic": "الْحَمْدُ لِلَّهِ الَّذِي أَحْيَانَا بَعْدَ مَا أَمَاتَنَا وَإِلَيْهِ النُّشُورُ",
  "transliteration": "আলহামদু লিল্লাহিল্লাযী আহ্ইয়ানা বা'দা মা আমাতানা ওয়া ইলাইহিন্ নুশূর",
  "translation": "সমস্ত প্রশংসা আল্লাহর জন্য, যিনি আমাদের মৃত্যুর পর জীবিত করলেন এবং তাঁরই কাছে সবার পুনরুত্থান।",
  "english": "All praise is for Allah who gave us life after having taken it from us and unto Him is the resurrection.",
  "reference": "সহীহ বুখারী: ৬৩১২, সহীহ মুসলিম: ২৭১১"
}
```

---

## 🛠️ Self-Hosting with Cloudflare Workers

```bash
# 1. Clone repository
git clone https://github.com/riadmonir/dua-api.git
cd dua-api

# 2. Install dependencies
npm install

# 3. Run locally
npm run dev

# 4. Deploy to your Cloudflare account
npm run deploy
```

---

## 📄 License

This dataset and code are provided open-source under the MIT License for the benefit of the Muslim community.
Supplications are sourced from the authentic DeenOne Muslim (حصن المسلم).
