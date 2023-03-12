# Bilibili-up-自动取关
B站自动取关
-----------------------------需求分析----------------------------------
随着优质且有趣的up增多，我们关注了越来越多的up，但大多数up是我们频率极少会去看的。于是乎，关注一时爽  
![image](https://user-images.githubusercontent.com/100819839/224519518-f7fb00a6-f384-4ef1-b1e6-b8cb56bd6913.png)  
    
  
-----------------------------源代码-----------------------------------  
简介：
本代码只是在浏览器内置的控制台中使用，详细下述。程序语言为javascript
var ms = 250; // 暂停250毫秒
var ii = 0;
var xx = $(".be-dropdown-item:contains('取消关注')");
console.log("本页关注了", xx.length, "个up主！");
tt = setInterval(function(){
  if (0 <= ii && ii < xx.length) {
    xx[ii].click(); // 自动点击【取消关注】
  } else {
    clearInterval(tt); // 停止批量操作
    console.log("OK！你已取消了对本页所有up主的关注！");
  }
  ii += 1;
}, ms+ii*10); // 暂停多少毫秒，再执行下一次点击，时间间隔增加一点儿变化
————————————————
版权声明：本文为CSDN博主「新池坡南」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/zhulewen/article/details/125179073

________________
使用文档：
	①登录哔哩哔哩官网 --> 用户头像-->关注
		②到取关的那页「一般有20个/页」
			③打开控制台「按F12」
				④将「代码」输入
