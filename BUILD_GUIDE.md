# Automated APK Build Guide

## কিভাবে কাজ করে? 🚀

এই প্রজেক্টে **GitHub Actions** সেটাপ করা হয়েছে যাতে automatically APK তৈরি হয়।

### আপনাকে কিছু করতে হবে না!

শুধু code push করুন, বাকিটা automatic হবে। ✨

## APK পেতে হলে:

### **১. GitHub এ যান:**
```
https://github.com/sameul098766-bit/Ariyan-khan/actions
```

### **২. সর্বশেষ ওয়ার্কফ্লো খুলুন:**
- "Build Android APK" ক্লিক করুন
- সবুজ ✓ চিহ্ন দেখলে বিল্ড সফল

### **৩. APK ডাউনলোড করুন:**
- স্ক্রল করে নিচে যান
- "Artifacts" সেকশন দেখবেন
- `apk-debug` ডাউনলোড করুন (অথবা `apk-release`)

---

## কখন বিল্ড হয়? 📅

✅ **যখনই আপনি code push করবেন** (main branch এ)
✅ **Pull Request তৈরি করলে**
✅ **ম্যানুয়ালি চালাতে চাইলে**: Actions ট্যাব → "Run workflow"

---

## APK ইনস্টল করুন (আপনার ফোনে):

```bash
# ADB দিয়ে ইনস্টল করুন
adb install -r app-debug.apk
```

অথবা যদি ADB না থাকে, এক্স-প্লোর দিয়ে APK ফাইলে ডাবল ক্লিক করুন!

---

## ট্রাবল শুটিং:

**❌ বিল্ড ফেইল হলে:**
- Actions ট্যাব খুলুন
- ফেইলড workflow ক্লিক করুন
- Logs দেখুন কেন fail হয়েছে

**❌ APK ডাউনলোড না হলে:**
- Workflow complete হওয়া পর্যন্ত অপেক্ষা করুন
- Page refresh করুন
- Artifacts সেকশন চেক করুন

---

**সহায়তা দরকার? বলবেন!** 😊
