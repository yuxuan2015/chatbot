# chatbot
一个可以使用自己语料进行训练的中文聊天机器人，欢迎大家实践交流。

#关于语料的说明

本次训练的语料是从互联网上找到的shooter的训练语料，语料质量很差劲，仅作为演示代码来用，大家可以使用自己的语料
[语料下载地址](https://pan.baidu.com/s/1kWYIOVt)，将文件下载后放到data目录下。

#seq2seq版本代码执行顺序

1、在下载好代码和语料之后，将语料文件放入data目录下。

2、按照 数据预处理器（data_utls.py)-->execute.py(执行器)-->web/app.py（预测可视化模块）的顺序执行就可以了。

3、超参配置在seq2seq.ini和seq2seq_sever.ini文件中配置。

4、详细的代码讲解可以参与我的chat文章(http://gitbook.cn/books/5a4a16da1f2e8d585e464f44/index.html)。

#seqGAN版本代码执行顺序

1 、在下载好代码和语料之后，将语料文件放入source_data目录下。

2、按照 数据预处理器（source_data_utls.py)-->execute.py(执行器)-->app.py（可视化模块）的顺序执行就可以了


#参考代码和文献

http://blog.topspeedsnail.com/archives/10735/comment-page-1#comment-1161。

http://www.easyapple.net/?p=1384&from=singlemessage&isappinstalled=0。

[SeqGAN: Sequence Generative Adversarial Nets with Policy Gradient](https://arxiv.org/abs/1609.05473)

[seqGAN实现中文对话系统](https://github.com/vpegasus/seqGan_chatbot)

#建议环境
```
ubuntu16.04
python3.6
tensorflow>=1.10.1或者tensorflow-gpu>=1.10.1
flask==0.11.1
```

# Transfomer实现chatbot

1 [Chinese-Chatbot-base-on-Transformer](https://github.com/ericosmic/Chinese-Chatbot-base-on-Transformer)

2 [ChineseQABot](https://github.com/st9007a/ChineseQABot)

3 [transformer-chatbot](https://github.com/Zhihan1996/transformer-chatbot)

4 [Transformer-in-generating-dialogue](https://github.com/EternalFeather/Transformer-in-generating-dialogue)

5 [Seq2seqChatbots](https://github.com/ricsinaruto/Seq2seqChatbots)

6 [chatbots2s](https://github.com/lang-ai/chatbots2s)

#关于版权

本代码遵循Apache2.0开源协议，作为一个平台供大家学习和研究交流，不过希望大家fork和给star。

#已更新功能清单:

V1.1:已经增加中文分词，效果是变得更好了。注意在使用分词后，需要增加词典的大小，否则的话会导致词典无法覆盖训练集，导致出现很多的UNK。直接在seq2seq.ini中修改超参数enc_vocab_size和dec_vocab_size的值即可。

V2.0:增加一个基于SeqGan的版本，以增加训练的效果。如想详细了解SeqGan的原理和代码讲解，可以参阅我在小象学院的课程视频http://www.chinahadoop.cn/course/1227






