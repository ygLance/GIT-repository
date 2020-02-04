# Brute Force 算法

* 一种垃圾算法//O(n*m)
**关键**
对a(string),b(pattern)分别遍历,
当遍历到b的尾部,且a\[p\]==b\[pos\]时,
ans++;pos=0;p++
或a\[p\]==b\[pos\]而没到尾部时,
p++;pos++;
或者a\[p\]!=b\[pos\]时
pos=0;p=p-(pos-1);//p回到开始为这一轮pos匹配的位置后一位

a循环完时结束
