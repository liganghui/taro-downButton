## taro 倒计时按钮组件

封装好的倒计时按钮组件 , 可自定义样式 , 避免重复造轮子 .  

已测试通过 : ```微信小程序```  ```H5```

原则上 react-native  与 其他小程序也支持 , 但没测试过 . 如有问题 可自行修改源码或向我提Issues

> ### 演示效果 

> ### 使用方法

  1. 拷贝```DownButton```文件夹到你的```components```目录下 
  2. 引用组件到页面中 , 然后调用即可  示例代码 :
  ``` javascript
  import DownButton from "../../components/DownButton";

  countDownButtonPressed(){
    //调用组件方法 开始按钮倒计时
    this.countDownButton.startCountDown();
  };

<DownButton
    onClick={this.countDownButtonPressed.bind(this)}
    ref={ref => {
        this.countDownButton = ref;
    }}
></DownButton>

  ```
  3. 如不满意按钮的样式 , 你可以打开组件下的```index.scss```调整 .

> ### API

参数| 说明 |  类型 | 默认值 | 必填
-|-|-|-|-
id | 按钮的身份标识,同一个页面的按钮是同一个id | Number | 1 | 否
beginText | 初始状态按钮title | String | 获取验证码 | 否
endText | 读秒结束后按钮的title | String |  重新获取 | 否
count | 总的计时数 单位是秒s | Number |  60 | 否
onClick | 按下按钮的事件,但是触发倒数(startCountDown)需要你自己来调用 | Function |  Null | 是
changeWithCount | 读秒变化的函数,该函数带有一个参数count,表示当前的剩余时间 | Function |  x秒(x为当前剩余秒) | 否
end | 读秒完毕后的回调,读秒结束触发 | Function |  Null | 否
end | 读秒完毕后的回调,读秒结束触发 | Function |  Null | 否
end | 读秒完毕后的回调,读秒结束触发 | Function |  Null | 否
end | 读秒完毕后的回调,读秒结束触发 | Function |  Null | 否
disableStyle | 按钮禁用的时候样式名 | String |  有默认 见index.scss | 否
activeStyle | active情况下按钮样式名 | String |  有默认 见index.scss | 否
disableTextStyle | 按钮禁用的时候里面文字的样式名 | String |  有默认 见index.scss | 否
activeTextStyle | active情况下按钮里面文字的样式名 | String |  有默认 见index.scss | 否
frameStyle | 按钮追加的样式名 | String |  Null | 否






