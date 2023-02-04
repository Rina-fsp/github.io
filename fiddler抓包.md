# github.io
fiddler抓包
如何通过fiddler定位前后端bug？
![image](https://user-images.githubusercontent.com/124430018/216761762-959a41d8-7787-49a3-8500-7620724869d9.png)
![image](https://user-images.githubusercontent.com/124430018/216761784-6aa23006-93a0-494e-8cfd-6ab6e4e0eda5.png)

第一种情况：fiddler 在没有设置过过滤器的情况下面没有抓到请求信息，可能是前端页面元素没有绑定事件，也有可能是前端发生了JS 错误，这就是前端的bug 。

第二种情况：若抓取到的请求返回的结果错误，我们要确认一下，是否是前端传输的数据是错的，是的话就是前端的bug ，如果确定传值是正确的话，那就是后端的bug 。

第三种情况：若抓取到的请求返回值中间的http 的状态码是500的话，说明是后端服务器一般的内部错误，那这就是后端的bug 。

第四种情况：若抓取到的请求返回值中间的http 的状态码是404的话，说明可能后端服务器根本就没有对应地址的服务，当然还有可能是前端JS 提交请求的时候提交了错误的地址。
参考：https://www.cnblogs.com/sulanyuan/p/13395956.html
