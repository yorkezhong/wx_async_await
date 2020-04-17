### wx_async_await
支持小程序使用async和await。

###  注意事项
- 关闭小程序开发工具中的ES6转ES5。详情-->本地设置-->取消勾选ES6转ES5

###  使用示例

```js
   //封装wx.request
 function ajax(url, data) {
    return new Promise((resolve, reject) => {
    wx.request({
      url: url,
      data: data,
      header: {
        "content-type": 'application/x-www-form-urlencoded'
      },
      success: (result) => {
          resolve(result);
      },
      fail: (err) => {
        reject(err);
      },
    });
  });
}
//使用
async function test(){
let res=await ajax("xxxxx", {})
}
```

