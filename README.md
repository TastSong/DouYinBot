# 抖音机器人(寻找漂亮的你)

##  特性

- [x] **自动翻页**
- [x] **颜值检测**
- [x] **人脸识别**
- [x] **自动点赞**
- [x] **自动关注**
- [x] 随机防 Ban
- [ ] 自动回复

##  原理

- 打开《抖音短视频》APP，进入主界面
- 获取手机截图，并对截图进行压缩 (Size < 1MB)；
- 请求 [人脸识别 API](http://ai.qq.com/)；
- 解析返回的人脸 Json 信息，对人脸检测切割；
- 当颜值大于门限值 `BEAUTY_THRESHOLD`时，点赞并关注；
- 下一页，返回第一步；

## 使用教程
- Python版本：3.0及以上
- ADB用于计算机控制安卓手机 [ADB配置](https://jingyan.baidu.com/article/17bd8e52f514d985ab2bb800.html) 
- 在 [ai.qq.com](https://ai.qq.com) 免费申请 `AppKey` 和 `AppID`
1. 获取源码：`git clone https://github.com/wangshub/Douyin-Bot/`
2. 进入源码目录： `cd Douyin-Bot`
3. 安装依赖： `pip install -r requirements.txt`
4. 运行程序：`python douyin-bot.py`

## 注意

- 目前暂时只适配了 一加5(1920x1080 分辨率)，如果手机不是该分辨率，请修改 `config/` 文件夹下面的配置文件；
- `config.json`配置文件参考：
    - `center_point`: 屏幕中心点`(x, y)`，区域范围 `rx, ry`
    - `follow_bottom`: 关注按钮位置`(x, y)`，区域范围 `rx, ry`
    - `star_bottom`: 点赞按钮位置`(x, y)`，区域范围 `rx, ry`
    

## 脸部截取

![](https://github.com/TastSong/DouYinBot/tree/master/Douyin-Bot/screenshot/faces.png)

