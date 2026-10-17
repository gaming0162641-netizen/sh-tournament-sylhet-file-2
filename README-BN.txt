SH TOURNAMENT SYLHET — Firebase PWA Starter

এই ZIP-এ index.html, manifest.json, sw.js এবং firestore.rules আছে।

গুরুত্বপূর্ণ:
- এটি starter UI, সম্পূর্ণ tournament/payment app নয়।
- Firebase config এখনো index.html-এ সংযুক্ত নয়; তাই login/database ফিচার চালু নয়।
- বাস্তব deposit, withdrawal, entry fee, refund বা cash prize চালু নেই। এসবের জন্য trusted backend/Cloud Functions এবং payment provider integration দরকার।
- ক্লায়েন্ট থেকে কখনো wallet balance পরিবর্তন করার নিয়ম দেবে না।

Firestore Rules সেট করার আগে:
1. Firebase Console > Firestore Database > Rules খুলে বর্তমান কোডের কপি রাখো।
2. firestore.rules ফাইলের সম্পূর্ণ কোড কপি করে Rules editor-এ বসাও এবং Publish করো।
3. Rules অ্যাপের ডেটা-স্ট্রাকচারের সঙ্গে মিলিয়ে পরীক্ষা করতে হবে।
4. প্রথম admin অ্যাকাউন্ট তৈরি করার পর users/{UID} ডকুমেন্টে role: "admin" কেবল Firebase Console থেকে হাতে সেট করতে হবে। UID নিশ্চিত না হয়ে কাউকে admin করো না।
5. production-এ দেওয়ার আগে Firebase Rules Playground/Emulator দিয়ে পরীক্ষা করো।

Website Share:
- Share Website বাটন ফোনের Share menu খুলবে, না হলে URL copy করার চেষ্টা করবে।
- file:// দিয়ে খোলা লোকাল ফাইলের লিংক অন্যরা খুলতে পারবে না।
- সবাইকে একই সাইটে আনতে HTTPS hosting-এ publish করতে হবে, যেমন GitHub Pages বা Firebase Hosting; তারপর সেই public URL share করো।
