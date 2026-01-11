# 按键拍照功能实现步骤
<video width="600" controls>
  <source src="video/video1.mp4" type="video/mp4">
  您的浏览器不支持视频标签
</video>

## 1. 生成表情包，可以使用大模型或者在网上下载对应的表情包，我这里再豆包生成的表情包，如下
![图片](img/image1.jpg)
## 2.图片转成数组格式的.c文件
转换工具: https://pan.baidu.com/s/1Pllifs02bsIRoMCBkaTfTQ?pwd=56a6
![图片](img/image2.jpg)
## 3.添加电量监测成员变量
![图片](img/image3.jpg)
转成64和32两套数据
![图片](img/image4.jpg)
![图片](img/image5.jpg)
## 4. .c文件名一定要对应代码中表情包对应的文件名，跟这里对应
![图片](img/image6.jpg)
文件放在这个目录下覆盖原有的文件
![图片](img/image7.jpg)
## 5.一定要编译下后再烧录才会生效

## 6.如果在你的显示屏上表情显示太小可以在如下地方进行修改表情显示大小
![图片](img/image7.jpg)
## 7.到此大功告成！！！！