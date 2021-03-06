## এক্সেপশন   

এটি এমন একটি ইভেন্ট যা ঘটে তখনই, যখন একটি প্রোগ্রামের স্বাভাবিক এক্সিকিউশনের মধ্যে কোন বাধার উৎপত্তি হয়। অর্থাৎ যখন একটি পাইথন স্ক্রিপ্ট এমন কোন একটি সমস্যাপূর্ণ অবস্থার সম্মুখীন হয় যা সে এড়িয়ে যেতে পারে না অথবা সমাধান করতে পারে না অতঃপর প্রোগ্রামের এক্সিকিউশন বন্ধ হয়ে যায় - সেরকম ঘটনাকে এক্সেপশন বলা হয়। এক্সেপশন এর আভিধানিক অর্থ থেকেও বোঝা যায় যে ব্যাতিক্রম কোন অবস্থার উৎপত্তি।   

সাধারণত ভুল কোড বা ইনপুটের জন্য প্রোগ্রামের মধ্যে এক্সেপশন তৈরি হয় যা সঠিকভাবে হ্যান্ডেল না করলে প্রোগ্রাম অনাকাঙ্ক্ষিত ভাবে বন্ধ হয়ে যেতে পারে। একটি উদাহরণ দিয়ে আমারা বোঝার চেষ্টা করি - 

```python
a = 2500
b = 0

print(a/b)
print("I did it")
```  

আউটপুট, 

```python
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
```  

উপরের প্রোগ্রামে, গণিতের নিয়ম অনুযায়ী `a` কে `b` দিয়ে ভাগ করা সম্ভব না আর তাই যখনই  `print(a/b)` স্টেটমেন্টটি এক্সিকিউট হতে চেয়েছে তখনি এক ধরণের ব্যাতিক্রম অবস্থার উৎপত্তি হয়েছে যাকে এক্সেপশন বলা হচ্ছে। আর তাই পাইথন ওই প্রোগ্রামের পরবর্তী স্টেটমেন্ট গুলো এক্সিকিউট না করে বরং প্রোগ্রাম এক্সিকিউশন বন্ধ করে দিয়েছে। কিন্তু দেখা যাচ্ছে কোডের লেখায় বা নিয়মে কিন্তু কোন ভুল নাই। শুধুমাত্র রান টাইমেই এই পরিস্থিতি তৈরি হয়েছে। তাই এরকম অবস্থায় পাইথন এক্সেপশন তৈরি করে।  

প্রোগ্রামের মধ্যে বিভিন্ন কারনে বিভিন্ন রকম exception তৈরি হয়। কিছু কিছু নির্দিষ্ট কারণের জন্য ঘটা অনাকাঙ্ক্ষিত অবস্থা গুলোর সাপেক্ষে পাইথনে অনেক এক্সেপশন আছে। নিচে কয়েকটি উল্লেখ করা হলঃ  

<table class="table table-bordered">
<tbody><tr>
<th><b>এক্সেপশনের নাম</b></th>
<th><b>বর্ণনা</b></th>
</tr>
<tr>
<td>Exception</td>
<td>সব রকম এক্সেপশনের বেজ ক্লাস</td>
</tr>
<tr>
<td>StopIteration</td>
<td>যখন একটি ইটারেটরের next() মেথডটি কোন অবজেক্টকে পয়েন্ট করে না</td>
</tr>
<tr>
<td>ArithmeticError</td>
<td>নিউমেরিক ক্যাল্কুলেশনের জন্য তৈরি হয় এমন এক্সেপশনের বেজ ক্লাস</td>
</tr>
<tr>
<td>OverflowError</td>
<td>যখন একটি নিউমেরিক টাইপের ম্যাক্সিমাম লিমিট অতিক্রম করে</td>
</tr>
<tr>
<td>ZeroDivisonError</td>
<td>যখন শূন্য দিয়ে ভাগের ঘটনা ঘটে</td>
</tr>
<tr>
<td>ImportError</td>
<td>যখন import স্টেটমেন্ট ফেইল করে অর্থাৎ কোন কারনে import সম্পন্ন হয় না</td>
</tr>
<tr>
<td><p>IndexError</p><p>KeyError</p></td>
<td><p>যখন একটি সিকোয়েন্স টাইপ অবজেক্টে চাহিদা মোতাবেক ইনডেক্স পাওয়া যায় না</p></td>
</tr>
<tr>
<td>NameError</td>
<td>যখন নির্দিষ্ট নামের কোন আইডেন্টিফায়ারকে লোকাল বা গ্লোবাল স্কোপে খুঁজে পাওয়া যায় না</td>
</tr>
<tr>
<td><p>IOError</p></td>
<td><p>যখন ইনপুট বা আউটপুট সম্পর্কিত কোন অপারেশন সফল হয় না যেমন ফাইল থেকে পড়ার জন্য ওপেন ফাংশন কাজ করতে না পারলে</p></td>
</tr>
<tr>
<td><p>SyntaxError</p><p>IndentationError</p></td>
<td><p>পাইথন প্রোগ্রাম লেখার সময় ভুল কোন কি-ওয়ার্ড বা স্টেটমেন্ট থাকলে</p></td>
</tr>
<tr>
<td>RuntimeError</td>
<td>যখন কোন একটি এক্সেপশন ঘটে যা পাইথনের নির্দিষ্ট কোন ক্যাটাগরির এক্সেপশনের মধ্যেই পরে না</td>
</tr>
</tbody></table>