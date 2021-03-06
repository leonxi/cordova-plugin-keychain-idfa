# 说明

通过IDFA+KEYCHAIN的方式获取ios的唯一设备id.

如果不想使用Adsupport,请尝试另外一种获取方式：[UUID+KEYCHAIN](https://github.com/jasonz1987/cordova-plugin-keychain-uuid)

具体说明请参考：http://www.jason-z.com/post/22



# 示例

[Ionic3 Demo](https://github.com/jasonz1987/ionic-keychain-idfa-demo)



# 安装

```
cordova plugin add cordova-plugin-keychain-idfa
```



# 接口

### 从keychain中获取设备ID

```javascript
var args = {
  'key':'com.jason-z.test.idfa'
};

KeychainIDFA.getDeviceID((id)=>{
 console.log(id);   
},(err)=>{
    console.log(err);
})
```



### 从keychain中删除设备ID

```javascript
var args = {
  'key':'com.jason-z.test.idfa'
};

KeychainIDFA.deleteDeviceID((id)=>{
 console.log(id);   
},(err)=>{
    console.log(err);
})
```



*此处的key是用来标识keychain存储的键值，根据自己定义。*



# 重要说明

由于引入了AdSupport.Framework，并且你的应用里没有接入广告，需要在提交到appstore审核的时候正确勾选，否则有可能被苹果拒绝。参考配置如下：

![appstore审核](screenshot-1.png)

# 赞赏

如果我的插件帮助到了你，欢迎赞赏。

![赞赏](donate.png)

