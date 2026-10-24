SH TOURNAMENT SYLHET — Fixed Manual Payment + Rules Page

ফাইল:
- index.html: Player Panel, আলাদা Rules Page, Back buttons, Transaction ID submit
- admin.html: Admin Panel, Pending Payment Approve/Reject
- firestore.rules: paymentRequests-এর নিয়মসহ Firestore Rules template

সেটআপ:
1. বর্তমান GitHub ফাইল ও Firestore Rules-এর ব্যাকআপ রাখুন।
2. GitHub-এ index.html এবং admin.html প্রতিস্থাপন করুন।
3. Firebase Console > Firestore Database > Rules-এ firestore.rules-এর কনটেন্ট বসিয়ে Publish করুন।
4. নিশ্চিত করুন যে আপনার Admin account-এর users/{UID} ডকুমেন্টে role = admin আছে।
5. Player Panel-এ login করে কোনো paid match-এ TEST-TXN-001 দিয়ে submit পরীক্ষা করুন। বাস্তব টাকা পাঠাবেন না।
6. Admin Panel > Payments-এ pending request দেখুন। শুধু বাস্তব লেনদেন যাচাইয়ের পর Approve করুন।

গুরুত্বপূর্ণ:
- এই সিস্টেম Manual Transaction ID Review; payment gateway নয়।
- Firebase Storage ব্যবহার করা হয়নি; screenshot upload নেই।
- Rules-এ Admin role নিজে তৈরি করা যাবে না; নিরাপদে Admin role সেট করতে হবে।
- কোড Firebase-এর live project-এ স্বয়ংক্রিয়ভাবে deploy হয়নি; GitHub ও Firebase Console-এ আলাদাভাবে আপলোড/Publish করতে হবে।
- Rules publish করার পরও permission error হলে exact error ও Firebase data schema পরীক্ষা করতে হবে।
