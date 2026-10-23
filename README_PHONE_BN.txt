MIGRAINE CARE — PHONE-ONLY APK BUILD PROJECT

এই project GitHub Actions ব্যবহার করে ক্লাউডে Android debug APK build করার জন্য প্রস্তুত করা হয়েছে। কম্পিউটার লাগবে না, তবে GitHub account ও internet দরকার।

ফাইলগুলো:
- www/ : অ্যাপের web source
- package.json, capacitor.config.json : Capacitor configuration
- .github/workflows/build-apk.yml : GitHub Actions build workflow

PHONE-ONLY STEPS:
1. এই ZIP extract করুন Android ফোনের Downloads-এ।
2. ফোনের browser-এ github.com খুলে sign in/create account করুন।
3. New repository তৈরি করুন, নাম দিন migraine-care-android, Public বা Private বেছে Create repository চাপুন।
4. repository-তে Add file > Upload files ব্যবহার করে ZIP extract করা ফাইল/ফোল্ডারগুলো upload করুন। Hidden .github folder কিছু mobile file picker-এ দেখা নাও যেতে পারে। যদি দেখা না যায়, GitHub website-এ Add file > Create new file দিয়ে path `.github/workflows/build-apk.yml` তৈরি করে workflow code বসান; অথবা এমন file manager ব্যবহার করুন যা hidden folder দেখায়।
5. সব ফাইল `main` branch-এ commit করুন।
6. repository-এর Actions tab-এ যান। “Build Migraine Care APK” workflow খুলে Run workflow চাপুন (অথবা main-এ push/commit হলে স্বয়ংক্রিয়ভাবে চলবে)।
7. Build শেষ হলে workflow run খুলে নিচে Artifacts থেকে `migraine-care-debug-apk` download করুন। ZIP artifact খুলে `app-debug.apk` বের করুন।
8. APK ট্যাপ করে Install করুন। Android-এ প্রয়োজন হলে এই file manager/browser-এর জন্য Install unknown apps অনুমতি দিন।

গুরুত্বপূর্ণ:
- GitHub UI-তে পুরো folder upload মোবাইলে অসুবিধা হলে এটি আপনার ফোন/ব্রাউজারের সীমাবদ্ধতা হতে পারে। .github হলো hidden folder; সেটি workflow file-সহ অবশ্যই repo-তে থাকতে হবে।
- এটি debug APK। এটি পরীক্ষা/নিজের ফোনে ইনস্টল করার জন্য; Play Store release-এর জন্য signed release build, privacy policy, testing ইত্যাদি দরকার।
- Owner password demo only; localStorage password নিরাপদ নয়। Gmail sign-in, real secure admin, cloud sync, background alarm, AI chat ও doctor service এখনো এই prototype-এ বাস্তবায়িত নয়।
- Health app হিসেবে প্রকাশের আগে চিকিৎসা-তথ্য যাচাই ও privacy/security review আবশ্যক।
