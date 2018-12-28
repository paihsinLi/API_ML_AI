| 发布日期 | 2018-11-23 |
| ------ | ------ |
| Epic | 厨房大师 |
| 文件现状 | 进行中 |
| 文件主人 | 李佰芯 |
| 领头设计者 | 李佰芯 |
| 领头开发者 | 李佰芯 |
| 领头测试者 | 李佰芯 |
## 目标: 
识别菜谱，提供美食烹饪方法，技巧学习、交流指导。
## 问题 : 
帮助不会做菜甚至想学做菜的人也能学会做菜，甚至知道如何搭配菜式，并且可以和志同道合的人一起交流想法。
## 不做 : 
（语音识别）用户通过语音询问得到菜式在百度百科上的相关信息
## 加值宣言: 
研究发现，目前已有不少菜谱类APP视频教学做菜，将美食菜谱、社交互动、美食画报整合为一体的APP，例如"豆果美食"等。但是随着人工智能的发展，人工智能快速识别菜谱成为一大优势。但是市面上这些应用都还有没有可以拍照进行菜谱识别的功能。现将采用百度的菜品识别API对菜谱APP产品进行加值和优化。主要层面 ：运用了机器学习中视觉技术的细粒度图像识别的菜品识别功能，通过输入的一张图片（清晰度和解析度正常），即可输出图片的菜品名称、菜式做法、置信度。
## 核心价值: 
解决用户想要知道美食的名称以及烹饪方法。
## 用户痛点: 
在朋友圈和微博上看到的美食和餐厅吃过的美食却不知道菜名和做法，可是又十分想尝试自己做。
## 使用场景: 
用户使用此主要功能时，主要是想尝试快速识别这道菜的做法或分享自己做菜的过程和想法。
## 需求: 

| 序号 | 使用案例 | 问题需求 | 对应功能 |
| ------ | ------ | ------ | ------ |
| 1 | 想做饭给对象吃，但是不知道如何下手 | 想获取全头到尾的全套指导 | 菜品搭配，菜谱功能 |
| 2 | 突然想吃某道菜，但是之前从来没有做过 | 想获得某道菜的制作方式 | 识别菜式 |
| 3 | 做了一道新菜，分享给对做菜感兴趣的人 | UGC段视频分享 | 用户分享功能,点赞和转发功能 |
   - 所对映的标题：菜谱识别
   - 重要程度：重要
   - 笔记：百度图像识别API请求回应  
## AI产品概率性与用户痛点: 
- 百度视觉技术的图像识别技术保证：
1. 稳定性好提供24小时云端高稳定服务，宕机率低，故障恢复快，单图毫秒级响应，服务可用性高达99.95%
2. 准确度高：基于百度丰富的海量数据，利用深度学习技术及精准的算法迭代模型，不断提高准确性
3. 功能丰富：支持上千种物体识别及场景识别，并在持续增加中，让你更好的读懂世界
- 阿里云图像识别产品优势:
1. 识别精准度高:图像识别等算法精度处于业内领先水平
2. 识别效率高:支持实时识别
3. 服务定制化:服务与SDK相结合，根据客户需求快速定制开发
4. 一站式解决方案:全力打造一站式解决方案，根据客户需求快速定制开发
- 该产品因照片识别或拍照不清晰造成识别不准确的状况，对正面影响并不大。
## API使用风险评估 : 
[原文链接](http://tech.ifeng.com/a/20150512/41080218_0.shtml)
人类对ImageNet图像的识别错误率大约在5%。相比之下，微软的人工智能系统的错误率为4.94%，谷歌为4.8%，百度如今已将这一错误率进一步降至4.58%。
- 错误方法解决
1. 用户可以手动输入帮助机器更正错误，确保机器能够准确识别。
2. 系统会反馈给用户，该识别的菜式与您预想有偏差。
## 交互过程
#### 1.界面识别
![Aaron Swartz](https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/界面识别.png)
#### 2.识别模块
![Aaron Swartz](https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/识别模块.png)
#### 3.拍照模块
![Aaron Swartz](https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/拍照模块.png)
#### 4.菜谱模块
![Aaron Swartz](https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/菜谱模块.png)
- 口头操作说明:用户点击拍照/选取图像识别，跳转到图库选择，若点击拍照识别，则进入实时拍照，成功后则到识别出来的菜谱模块。
## 产品结构
#### 1.产品结构图
![Aaron Swartz](https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/产品结构图.png)
#### 2.产品信息结构图
![Aaron Swartz](https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/产品信息结构图.png)
#### 3.产品流程图
![Aaron Swartz](https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/产品流程图.png)
## API图像识别
- 首先进入到百度AI的官网，找到图像识别需要的API
- 接下来就是代码调用部分了，要使用API，我们需要得到一个叫“access_token”。它需要“API Key”和“Secret Key”来获取。
- 把Api Key和Secret Key提交给https://aip.baidubce.com/oauth/2.0/token?grant_type=client_credentials
- 然后它就会把access_token返回给你，读取下来，然后因为是json格式，所以用json.load()转成字典
- 然后复制access_token那行代码，组合并调用，打开本地相册文件（要识别的美食）
- 再把处理好的img和刚获得的access_token扔进一个字典里面，然后把字典提交给网址(https://aip.baidubce.com/rest/2.0/image-classify/v2/advanced_general)，它会以json格式返回一个分析结果给我们。（得到我们想要的菜式）
#### API的运用:
`import  requests, sys#获取access_token
`
```import  requests, sys#获取access_token
import ssl
header={'Content-Type': 'application/json; charset=UTF-8'}
# client_id 为官网获取的AK， client_secret 为官网获取的SK
host ='https://aip.baidubce.com/oauth/2.0/token?grant_type=client_credentials&client_id=o6N6MbRpRa5gWFIf70UZdl7V&client_secret=SxdDxagclKGG5Lncqh0bKSFuCTQ1dFWp'
res=requests.post(host,json=header)
print(res.text)
```
得到access_token：
`24.35833cf62ab5848149456a0369b98ff8.2592000.1536748894.282335-11667xxx
`

组合并调用
```import base64
import requests
import  urllib.parse
request_url = "https://aip.baidubce.com/rest/2.0/image-classify/v2/dish"
# 二进制方式打开图片文件
f = open('C:\\Users\\index\\Pictures\\3.jpg', 'rb')
img = base64.b64encode(f.read())
 
params = {"image":img,"top_num":5}
urllib.parse.urlencode(params)
header={'Content-Type':'application/x-www-form-urlencoded'}
access_token = 'access_token":"24.35833cf62ab5848149456a0369b98ff8.2592000.1536748894.282335-1166xxx
request_url = request_url + "?access_token=" + access_token
request = requests.post(url=request_url, data=params,)
print(request.text)
```
打开本地文件.jpg（菜谱图片）,得到返回值:

`{"log_id": 6222410495897780005, "result_num": 5, "result": [{"calorie": "313", "has_calorie": true, "name": "老式面包", "probability": "0.438405"}, {"calorie": "371", "has_calorie": true, "name": "手撕面包", "probability": "0.058642"}, {"calorie": "378", "has_calorie": true, "name": "牛角面包", "probability": "0.0558874"}, {"calorie": "282", "has_calorie": true, "name": "烤面包", "probability": "0.0494301"}, {"calorie": "392", "has_calorie": true, "name": "小面包", "probability": "0.0390798"}]}
`
## 其他功能阐述
#### 1.功能权限
- 未登录状态: 未登录状态下可查看菜谱
- 已登录状态: 已登录状态下可执行所有操作
#### 2.键盘说明
- 点击手机注册/手机登陆输入框时弹出数字键盘
- 点击其他输入框时弹出字母键盘
#### 3.登录页面/用户注册页面
- 当文本框没有字符的时候，登录按钮不可点击，灰色状态；当帐号和密码输入后，按钮亮起，可以点击，登录成功后，进入首页，否则Toast提示“帐号或密码错误”
- 入口：点击登录页面的注册按钮
#### 4.分享功能
- 入口：点击设置页面的“分享”按钮
- 当点击设置页面的“分享”按钮，从底部滑出弹框，点击图标跳入该图标的第三页面
- 分享成功跳转回原页面，提示“分享成功”
- 分享取消跳转回原页面，无提示
- 分享失败跳转回原页面，提示“很遗憾，分享失败”
#### 5.设置页面
- 点击“清理缓存”按钮，自动清理APP缓存
- 点击“喜好设置”按钮，进入喜好设置页面
- 点击“鼓励一下”按钮，进入appstore为爱厨房评分
- 点击“修改密码”按钮，进入修改密码页面
## 产品原型链接
<https://paihsinli.github.io/API_ML_AI/%E4%BA%A7%E5%93%81%E5%8E%9F%E5%9E%8B/#g=1&p=智能菜谱识别>
## 产品结构图链接
<https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/产品结构图.png>
## 产品信息结构图链接
<https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/产品信息结构图.png>
## 产品流程图
<https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/产品流程图.png>
## 界面识别
<https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/界面识别.png>
## 识别模块
<https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/识别模块.png>
## 拍照模块
<https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/拍照模块.png>
## 菜谱模块
<https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/菜谱模块.png>
