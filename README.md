# ocrScanDocs
recognize Chinese characters for efficient doc input

调研进度：
- 成熟软件，市面上有一些文字识别软件例如ABBYY-俄罗斯
Abbyy OCR SDK/API.
OnlineOCR.
Google Docs OCR.
i2OCR.
FreeOnlineOCR.
Tesseract Online Demo (flunked even the 300 dpi OCR test)
NOTE: https://www.zhihu.com/question/19593313
真正能把中文OCR做得比较专业的，一共也没几家，国内2家，国外2家。国内是文通和汉王，国外是ABBYY和IRIS（台湾原来有2家丹青和蒙恬，这两年没什么动静了）。像大家提到的紫光OCR、CAJViewer、MS Office、清华OCR、包括慧视小灵鼠，这些都是文通的产品或者使用文通的识别引擎，尚书则是汉王的产品，和中晶扫描仪捆绑销售的。这两家的中文识别率都是非常不错的。而国外的2家，主要特点是西方语言的识别率很好，而且支持多种西欧语言，产品化程度也很高，不过中文方面速度和识别率还是有差距的，当然这两年人家也是在不断进步。Google的开源项目，至少在中文方面，和这些家相比，各项性能指标水平差距还蛮大的呢。

- 类似应用，识别收据
1. Free Chinese Character Recognition with Google Translate 6 December, 2012 @ 23:00pm UTC
http://chinesehacks.com/resources/free-chinese-character-recognition-google-translate/

2. Creating a Modern OCR Pipeline Using Computer Vision and Deep Learning, 2017/4
https://blogs.dropbox.com/tech/2017/04/creating-a-modern-ocr-pipeline-using-computer-vision-and-deep-learning/
	
3. Receipt recognition, June 2017
https://dzone.com/articles/using-ocr-for-receipt-recognition


- 开源项目：github上也有一些开源的OCR项目-google Tesseract等，咱们需要投入研发去修正，部署，测试，改进，最终做demo，出咱们自己的版本。
1. https://github.com/JinpengLI/deep_ocr
2. https://github.com/chineseocr/chinese-ocr

- 技术对比：目前技术有tesseract，或者deep learning，我们需要基于准确性，可维护性进行选择。
- KPI：图片文字识别准确度能达到80-90%，应该不是100%，所以咱们后续还需提供校对，手工编辑的环节


项目需求问题列表（持续更新）：
- 文档是手写还是打印 - TanMJ
- 结果信息（标题、日期）等位置是否固定



