---
tags: tip
title: ওহ গিট, আমি মারাত্মক ভুল করে ফেলেছি, কেও আমাকে বল git এর ম্যাজিক টাইম মেশিন আছে!?!
id: magic-time-machine
order: 1
---

```git
git reflog
# আপনি একটা লিস্ট পাবেন
# যেখানে git এর সকল ব্রাঞ্চ এর সব commit দেখতে পাবেন
# প্রত্যেক আইটেম এর একটা ইনডেক্স HEAD@{index} থাকবে
# ওই ইনডেক্স টা খুঁজে বের করেন, যেটার পরের কমিট থেকে ঝামেলা শুরু হয়েছে
git reset HEAD@{index}
# ম্যাজিক টাইম মেশিন
```

আপনি এটা ব্যাবহার করে ভুলবশত ডিলিট হয়ে যাওয়া যেকোনো কিছু ফিরে পাবেন, কিংবা সরিয়ে ফেলতে পারবেন এমন কিছু যেটা রেপো এর কিচু ভেঙ্গে ফেলতে পারে, অথবা কোন খারাপ merge রিকোভার করতে পার, এমনকি সেই সময় ফিরে যেতে পারেন যেখানে আপনি আসলেই কাজ করেছেন। 
আমি `reflog`  অনেক ব্যাবহার করি। যারা এটা এড করার উপদেশ দিসে তাদের অনেক অনেক অনেক অনেক সাধুবাদ। 