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
研究发现，目前已有不少菜谱类APP视频教学做菜，将美食菜谱、社交互动、美食画报整合为一体的APP，例如"豆果美食"等。但是随着人工智能的发展，人工智能快速识别菜谱成为一大优势。现将采用百度的菜品识别API对菜谱APP产品进行加值和优化。主要层面 ：运用了机器学习中视觉技术的细粒度图像识别的菜品识别功能，通过输入一张美食图片，即可输出图片的菜品名称、菜式做法步骤。
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
2. 系统会反馈给用户："亲，没查到你想要的"或提示该识别的菜式与您预想有偏差。
## API使用比较分析
1. 百度API识别的图片比较单一，识别菜名和菜谱识别结果数组，还有对应百度百科的描述
2. 谷歌API识别出菜谱由来和菜谱关键字，主料和辅料并提供了具体的菜谱做法步骤
- 总的来说：谷歌API比较满足用户需求，识别速度较快的是：百度API，精准度较高的是谷歌API。
## 交互过程
#### 1.界面识别
![Aaron Swartz](https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/界面识别.png)
#### 2.识别模块
![Aaron Swartz](https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/识别模块.png)
#### 3.拍照模块
![Aaron Swartz](https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/拍照模块.png)
#### 4.菜谱模块
![Aaron Swartz](https://github.com/paihsinLi/API_ML_AI/blob/master/结构图/菜谱模块.png)
- 口头操作说明：用户点击拍照/选取图像识别，跳转到图库选择，若点击拍照识别，则进入实时拍照，成功后则到识别出来的菜谱模块。
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
### API的运用:
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
 
params = {"image":img,"top_num":1}
urllib.parse.urlencode(params)
header={'Content-Type':'application/x-www-form-urlencoded'}
access_token = 'access_token":"24.35833cf62ab5848149456a0369b98ff8.2592000.1536748894.282335-1166xxx
request_url = request_url + "?access_token=" + access_token
request = requests.post(url=request_url, data=params,)
print(request.text)
```
打开本地文件.jpg（菜谱图片）,得到返回值:

`{"log_id": 6222410495897780005, "result_num": 1, "result": [{"name": "秘制红烧肉"}{"baike_info": {
			"baike_url": "http://baike.baidu.com/item/%E9%85%B8%E6%B1%A4%E9%B1%BC/1754055",
			"description": "酸汤鱼，是黔桂湘交界地区的一道侗族名菜，与侗族相邻的苗、水、瑶等少数民族也有相似菜肴，但其中以贵州侗族酸汤鱼最为有名，据考证此菜肴最早源于黎平县雷洞镇牙双一带。制作原料主要有鱼肉、酸汤、山仓子等香料。成菜后，略带酸味、幽香沁人、鲜嫩爽口开胃，是贵州“黔系”菜肴的代表作之一。这道菜通常先自制酸汤，之后将活鱼去掉内脏，入酸汤煮制。"
		}}]}
`

Ajax运用artTemplate实现菜谱

GoogleAPI：https://www.google.cn 在这上面找到菜谱大全数据接口文档

key后面的数据是固定的，rn和pn是参数，后面的数值可以自定义，dtype是jsonp，最后加上输入的值  txt

`url:"http://apis.Google.cn/cook/query?key=1993189fed228f8036959eb6e187b419&rn=3&pn=0&dtype=jsonp&menu="+txt
`

代码展示

```<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>菜谱</title>
    <style>
        .all {
            margin-top: 30px;
        }
        .xh {
            float: left;
            margin-right: 20px;
            color: red;
            font-style: italic;
            font-size: 30px;
        }
        #menu {
            width: 500px;
        }
    </style>
 
    <script src="./jquery-2.2.0.js"></script>
    <script src="template-native-debug.js"></script>
    <script>
        //1、从服务器获取数据
        //2、解析从服务器获取的数据
        $(function(){
            $("#btnSearch").click(function(){
 
                var menu=$("#menu");
                menu.text("正在加载...");//页面加载慢时显示
                //获取文本框的值
                var txt=$("#txtSearch").val();
                //对用户输入的内容进行URL编码
                txt=encodeURIComponent(txt);
                //发送异步请求 jsonp
                $.ajax({
                    type:"get",
                    url:"http://apis.google.cn/cook/query?key=1993189fed228f8036959eb6e187b419&rn=3&pn=0&dtype=jsonp&menu="+txt,
                    dataType:"jsonp",
                    success:function(data) {
                        //清空容器
                        menu.text("");
 
                        //解析数据
 
                        if (data.resultcode != 200) {
                            menu.text("亲，没查到你想要的");
                            return;
                        }
                        //解析数据 模板引擎
 
                        var html = template("tpl", data.result);
                        menu.html(html);
                    },
                    error:function(){
                        menu.text("错误");
                    }
                });
            });
        })
 
    </script>

//模板引擎

    <script id="tpl" type="text/html">
        <% for(var i=0;i< data.length;i++) { %>
        <div class="all">
            <h2><%= data[i].title %></h2>
            <p class="intro"><%= data[i].imtro %></p>
            <% for(var j=0;j< data[i].albums.length;j++) { %>
                <img src="<%= data[i].albums[j] %>">
            <% } %>
            <p class="zl">主料：<%= data[i].ingredients %></p>
            <p class="fl">辅料：<%= data[i].burden %></p>
            <div class="steps">
                <% for(var k=0;k< data[i].steps.length;k++) { %>
                    <em class="xh"><%= k+1 %>.</em>
                    <div class="c">
                        <p><% data[i].steps[k].step %></p>
                        <p><img src= "<%= data[i].steps[k].img %>"></p>
                    </div>
                <% } %>
            </div>
        </div>
        <hr>
        <% } %>
 
    </script>
</head>
<body>
    <input type="text" id="txtSearch">
    <input type="button" value="搜索" id="btnSearch">
    <div id="menu"></div>
</body>
</html>
```
解析数据如下
``` {
     "resultcode": "200",
     "reason": "Success",
     "result": {
         "data": [{
             "id": "45",
             "title": "秘制红烧肉",
             "tags": "家常菜;热菜;烧;煎;炖;红烧;炒锅",
             "imtro": "做红烧肉的豆亲们很多，大家对红烧肉的热爱更不用我说，从名字上就能反映出来。一些高手们对红烧肉的认识更是令我佩服，单单就红烧肉的做法、菜谱都看得我是眼花缭乱，口水横流。单纯的红烧肉我平时还真没做过，再不抓紧时间做一回解解馋，不是对不起别人，而是太对不起我自己了！ 这道菜的菜名用了秘制二字来形容，当然是自己根据自己多年吃货的经验想象出来的，我不介意把自己的做法与大家共享，只为大家能同我一样，吃到不同口味的红烧肉。不同的人们根据自己的习惯都有不同的做法，味道也不尽相同。我的秘制的关键就是必须用玫瑰腐乳、冰糖和米醋这三种食材，腐乳和冰糖可以使烧出来的肉色泽红亮，米醋能解腻，令肥肉肥而不腻，此法烧制的红烧肉软糯中略带咸甜，的确回味无穷！",
             "ingredients": "五花肉,500g",
             "burden": "玫瑰腐乳,适量;盐,适量;八角,适量;草果,适量;香叶,适量;料酒,适量;米醋,适量;生姜,适量",
             "albums": ["http:\/\/img.google.cn\/cookbook\/t\/0\/45_854851.jpg"],
             "steps": [{
                 "img": "http:\/\/img.google.cn\/cookbook\/s\/1\/45_0824e37faf00b71e.jpg",
                 "step": "1.将五花肉煮至断生状态"
             },
             {
                 "img": "http:\/\/img.google.cn\/cookbook\/s\/1\/45_b6d7329b703f6e85.jpg",
                 "step": "2.切成大小一致的块"
             },
             {
                 "img": "http:\/\/img.google.cn\/cookbook\/s\/1\/45_6ee9e8dab0516333.jpg",
                 "step": "3.放在锅内煎"
             },
             {
                 "img": "http:\/\/img.google.cn\/cookbook\/s\/1\/45_b9afd6d4dd81f55c.jpg",
                 "step": "4.入生姜"
             },
             {
                 "img": "http:\/\/img.google.cn\/cookbook\/s\/1\/45_d0170fbe236421f9.jpg",
                 "step": "5.放八角草果各一个，香叶一片"
             },
             {
                 "img": "http:\/\/img.google.cn\/cookbook\/s\/1\/45_639b12210745fa41.jpg",
                 "step": "6.放冰糖"
             },
             {
                 "img": "http:\/\/img.google.cn\/cookbook\/s\/1\/45_c25e0cedd2012f45.jpg",
                 "step": "7.加料酒"
             },
             {
                 "img": "http:\/\/img.google.cn\/cookbook\/s\/1\/45_eb68327980f022dd.jpg",
                 "step": "8.加玫瑰腐乳和腐乳汁及适量盐"
             },
             {
                 "img": "http:\/\/img.google.cn\/cookbook\/s\/1\/45_ac17263a11507a41.jpg",
                 "step": "9.加米醋"
             },
             {
                 "img": "http:\/\/img.google.cn\/cookbook\/s\/1\/45_f5489af5d12b4930.jpg",
                 "step": "10.加水继续炖"
             },
             {
                 "img": "http:\/\/img.google.cn\/cookbook\/s\/1\/45_8e0cf83cb7306281.jpg",
                 "step": "11.直至肉变软糯汤汁收干即可"
             }]
         }]
```
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
