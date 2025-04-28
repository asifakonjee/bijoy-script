## ইনস্টল পদ্ধতি

মূলত এই রিপোজিটরিটির স্ক্রিপ্ট দ্বারা fcitx5 এবং ibus এর সাথে ব্যবহারের জন্যে বিজয় ক্ল্যাসিক এবং বিজয় ইউনিকোড কিবোর্ড সহজে ইন্সটল করতে পারবেন।


## সহজ ইন্সটল পদ্ধতি

### fcitx5 এর জন্যে
টার্মিনাল ওপেন করে নিচের কমান্ডটি কপি করে টার্মিনালে পেস্ট করুনঃ
```bash
bash -c "$(wget -q https://raw.githubusercontent.com/asifakonjee/bijoy-script/master/fcitx5.sh -O -)"
```

### ibus এর জন্যে
টার্মিনাল ওপেন করে নিচের কমান্ডটি কপি করে টার্মিনালে পেস্ট করুনঃ
```bash
bash -c "$(wget -q https://raw.githubusercontent.com/asifakonjee/bijoy-script/master/ibus.sh -O -)"
```


## শেষ ধাপ

### fcitx5 এর জন্যে
রিস্টার্ট করুন বা লগ আউট করে পুনরায় লগ ইন করুন। এবার fcitx5 configtool ওপেন করে সেখানে add layout এ গিয়ে bijoy লিখে সার্চ করুন এবং bn-bijoyClassic এবং bn-bijouUnicode কিবোর্ড এড করুন। এরপর Global Options এ গিয়ে ভাষা পরিবর্তনের জন্যে আপনার পছন্দমতো কিবোর্ড শর্টকাট এড করে নিন। কেডিই প্লাজমা ডেস্কটপ এনভাইরনমেন্টের ক্ষেত্রে এর পাশাপাশি সেটিংসে গিয়ে Virtual Keyboard লিখে সার্চ করুন এবং সেখানে fcitx5 সিলেক্ট করে দিন। এরপরেও যদি ব্রাউজার বা লিব্রে অফিসে বাংলা লিখতে সমস্যা হয় তাহলে নিচের লেখাগুলো কপি করে `` /etc/environment `` ফাইলে এড করে দিনঃ
```bash
GTK_IM_MODULE=fcitx
QT_IM_MODULE=fcitx
XMODIFIERS=@im=fcitx
```

### ibus এর জন্যে
রিস্টার্ট করুন বা লগ আউট করে পুনরায় লগ ইন করুন। এবার ibus preferences এ গিয়ে input method>add>Bangla -এ গিয়ে bijoy Classic এবং  bijoy Unicode এড করে দিন। কেডিই প্লাজমা ডেস্কটপ এনভাইরনমেন্টের ক্ষেত্রে এর পাশাপাশি সেটিংসে গিয়ে Virtual Keyboard লিখে সার্চ করুন এবং সেখানে ibus-wayland সিলেক্ট করে দিন। এরপরেও যদি ব্রাউজার বা লিব্রে অফিসে বাংলা লিখতে সমস্যা হয় তাহলে নিচের লেখাগুলো কপি করে `` /etc/environment `` ফাইলে এড করে দিনঃ
```bash
GTK_IM_MODULE=ibus
QT_IM_MODULE=ibus
XMODIFIERS=@im=ibus
```

## Modifications

### বর্তমানে বিজয় লিনাক্স ব্যক্তিগত ব্যবহারের জন্য বিনামূলয়ে বিতরণ করা হচ্ছে। যদি এটি ভবিষ্যতে পরিবর্তন হয় বা মূল্য নির্ধারণ করা হয় তাহলে এই রিপোজিটরি স্থাহীভাবে রিমুভ করে দেওয়া হবে কেননা বিজয় প্রোপাইটারি কিবোর্ড লেআউট। 

This repository will install modified versions of `bn-bijoyClassic.mim` and `bn-bijoyUnicode.mim`, originally provided by Ananda Computers at [bijoyekushe.net.bd](https://bijoyekushe.net.bd/index.php?action=bijoy_linux). All rights of these files are to copyright © Mustafa Jabbar.

The following modifications were made to address various issues and discrepancies with the Windows version of the Bijoy Keyboard:
1. Fixed mapping for `_`, which was previously pointed to "থ".
2. Fixed mapping for `'`, which was previously broken.
3. Fixed mapping for `"`, which was previously broken.
4. Added a built-in Smart Quotes feature.
