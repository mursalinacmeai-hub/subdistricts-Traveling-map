# উপজেলা ভ্রমণ ম্যাপ

বাংলাদেশের উপজেলা-ভিত্তিক ম্যাপ। ভিজিটর যে উপজেলাগুলোতে গিয়েছেন সেগুলো ম্যাপে ক্লিক করে বা তালিকা/সার্চ থেকে সিলেক্ট করবেন, এবং ম্যাপটি PNG ছবি হিসেবে ডাউনলোড করতে পারবেন।

- কোনো বিল্ড স্টেপ নেই — সাধারণ HTML/CSS/JS (D3 দিয়ে ম্যাপ রেন্ডার)
- সিলেকশন ব্রাউজারে (localStorage) সেভ থাকে
- জুম/প্যান, হোভারে নাম, বিভাগ → জেলা → উপজেলা তালিকা, সার্চ, ৫টি রঙের থিম, কাস্টম শিরোনাম

## Vercel-এ ডিপ্লয়

**GitHub দিয়ে (সুপারিশকৃত)**
1. এই ফোল্ডারটি একটি GitHub রিপোজিটরিতে পুশ করুন।
2. vercel.com → Add New → Project → রিপোজিটরি ইম্পোর্ট করুন।
3. Framework Preset: **Other**, Build Command ও Output Directory ফাঁকা রাখুন → Deploy।

**CLI দিয়ে**
```bash
npm i -g vercel
cd upazila-map
vercel --prod
```

## ম্যাপ ডাটা

ডিফল্টভাবে অ্যাপ `/data/bangladesh.geojson` খোঁজে; ফাইল না থাকলে স্বয়ংক্রিয়ভাবে jsDelivr CDN থেকে লোড করে। দ্রুত ও নির্ভরযোগ্য লোডের জন্য ফাইলটি নিজের সাইটে রাখতে পারেন:

```bash
curl -L https://cdn.jsdelivr.net/gh/ifahimreza/bangladesh-geojson/src/data/bangladesh.geojson -o data/bangladesh.geojson
```

ডাটা সোর্স: [geoBoundaries](https://www.geoboundaries.org) (CC BY 4.0) via [ifahimreza/bangladesh-geojson](https://github.com/ifahimreza/bangladesh-geojson)। ছবির নিচে ও সাইটের ফুটারে ক্রেডিট দেওয়া আছে — এটি রাখুন।
