# 项目需求：
文档输入：
- 文档 
- 文档以打印为主 
- 结果信息（标题、日期）等位置不固定
- 包括印章等带背景的文字区域

程序功能：
- OCR
- 文字识别校对，手工再编辑接口

系统输出：
- 格式化信息
- 导出格式：Excel，json，txt等接口
- 二期：与文档信息系统无缝集成

# 可行性方案设计
产品将包括：
### 硬件
- 摄像头，灯，光滑平整的扫描区域等

    ![扫描仪](https://github.com/jasonzhang079/ocrScanDocs/blob/master/pics/scanner.jpg)
    

### 软件
- 确保机器可以识别各种背景中的中文（代码+demo如下）
- 依照项目要求，依据将影响识别度的文档情况（包括但不限于：布局、背景颜色、字体），设计详细识别方案

### 文档
- 保修文档
- 使用手册，尽可能简单

## 调研进度：
- 成熟软件，市面上有一些文字识别软件例如ABBYY-俄罗斯
Abbyy OCR SDK/API.
OnlineOCR.
Google Docs OCR.
i2OCR.
FreeOnlineOCR.
Tesseract Online Demo (flunked even the 300 dpi OCR test)
NOTE: https://www.zhihu.com/question/19593313
真正能把中文OCR做得比较专业的，一共也没几家，国内2家，国外2家。国内是文通和汉王，国外是ABBYY和IRIS（台湾原来有2家丹青和蒙恬，这两年没什么动静了）。像大家提到的紫光OCR、CAJViewer、MS Office、清华OCR、包括慧视小灵鼠，这些都是文通的产品或者使用文通的识别引擎，尚书则是汉王的产品，和中晶扫描仪捆绑销售的。这两家的中文识别率都是非常不错的。而国外的2家，主要特点是西方语言的识别率很好，而且支持多种西欧语言，产品化程度也很高，不过中文方面速度和识别率还是有差距的，当然这两年人家也是在不断进步。Google的开源项目，至少在中文方面，和这些家相比，各项性能指标水平差距还蛮大的呢。

## 类似应用
1. Free Chinese Character Recognition with Google Translate 6 December, 2012 @ 23:00pm UTC
http://chinesehacks.com/resources/free-chinese-character-recognition-google-translate/

2. Creating a Modern OCR Pipeline Using Computer Vision and Deep Learning, 2017/4
https://blogs.dropbox.com/tech/2017/04/creating-a-modern-ocr-pipeline-using-computer-vision-and-deep-learning/
	
3. Receipt recognition, June 2017
https://dzone.com/articles/using-ocr-for-receipt-recognition


### 开源项目

github上也有一些开源的OCR项目-google Tesseract等，咱们需要投入研发去修正，部署，测试，改进，最终做demo，出咱们自己的版本。
1. https://github.com/JinpengLI/deep_ocr
2. https://github.com/chineseocr/chinese-ocr
3. https://github.com/wanghaisheng/awesome-ocr
4. https://github.com/JarveeLee/SynthText_Chinese_version

##  DEMO
### 1. 布局一致的文字识别


![身份证](https://github.com/jasonzhang079/ocrScanDocs/blob/master/pics/id_card_img.jpg)

识别结果：

```
...
ocr res:
============================================================
name
韦小宝
============================================================
address
北京市东城区累山前街4号
紫禁城敬事房
============================================================
month
12
============================================================
minzu
汉
============================================================
year
1654
============================================================
sex
男
============================================================
id
1X21441114X221243X
============================================================
day
20

```

- 技术对比：目前技术有tesseract，或者deep learning，我们需要基于准确性，可维护性进行选择。
- KPI：图片文字识别准确度能达到80-90%，应该不是100%，所以咱们后续还需提供校对，手工编辑的环节



### 2. 带背景的文字识别DEMO


![车牌](https://github.com/jasonzhang079/ocrScanDocs/blob/master/pics/plateNumber.png)



![明信片](https://github.com/jasonzhang079/ocrScanDocs/blob/master/pics/chineseWithBackground.png)



