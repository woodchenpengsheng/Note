## 中文分词-结巴
### 其他分词工具背景介绍

> 中文分词相关的工具

- 结巴 [jiaba](https://github.com/fxsjy/jieba)
- [Hanlp](https://github.com/hankcs/HanLP)

### 在wps项目里面结巴的使用情况
#### 如何加载的
在我们项目代码里面，结巴的加载是通过doc_wasm_jieba_loader.js来完成的。

1. 划词通过worker线程来完成
2. 全局保留结巴对象，需要用的地方直接调用接口，然后通过回调的方式来完成更新

#### 暴露的接口
1. window.Jieba
2. window.Jieba.cut
> 分词的实现通过worker来完成。这里有个问题，前一次的请求还没结束的时候，新发了下一次的请求怎么办？(不用考虑)

