
哈工大自然语言处理工具LTP
============
平台官网：<https://www.ltp-cloud.com/>
------------
功能简介
------------
**1.	分句   **  
在中文文章中，语句是以句子为单元组织起来的。所以，要进篇章级别或者段落级别的自然语言处理，首先要进行分句处理。此部分实现比较简单，以句号，感叹号，问号为句子结束标志，完成分句任务。

**2.	分词   **  
中文分词 (Word Segmentation,) 指的是将汉字序列切分成词序列。 因为在汉语中，词是承载语义的最基本的单元。分词是信息检索、文本分类、情感分析等多项中文自然语言处理任务的基础。
切分歧义是分词任务中的主要难题。LTP的分词模块基于机器学习框架，可以很好地解决歧义问题。同时，模型中融入了词典策略，使得LTP的分词模块可以很便捷地加入新词信息。

**3.	词性标注  **  
词性标注(Part-of-speech Tagging, POS)是在给定句子分词结果时，给出词语的相应词性。 这里的词性类别可能是名词、动词、形容词或其他。
词性标注也是自然语言处理的一项基础而重要的任务，对于依存句法分析、语义理解等任务有重要意义。
命名实体识别
命名实体识别 (Named Entity Recognition, NER)任务的目的是识别出句子中的人名、地名、机构名，在自动问答，聊天机器人等任务中有非常重要的影响。

**4.	依存句法分析   **  
依存语法 (Dependency Parsing, DP) 通过分析语言单位内成分之间的依存关系揭示其句法结构。 直观来讲，依存句法分析识别句子中的“主谓宾”、“定状补”这些语法成分，并分析各成分之间的关系。
LTP的依存句法分析的标签及对应意义和解释，参考网页https://www.ltp-cloud.com/intro/  的描述。

**5.	语义角色标注    **  
语义角色标注 (Semantic Role Labeling, SRL) 是一种浅层的语义分析技术，标注句子中某些短语为给定谓词的论元 (语义角色) ，如施事、受事、时间和地点等。其能够对问答系统、信息抽取和机器翻译等应用产生推动作用。 

**6.	语义依存分析   **  
语义依存分析 (Semantic Dependency Parsing, SDP)，分析句子各个语言单位之间的语义关联，并将语义关联以依存结构呈现。 使用语义依存刻画句子语义，好处在于不需要去抽象词汇本身，而是通过词汇所承受的语义框架来描述该词汇，而论元的数目相对词汇来说数量总是少了很多的。语义依存分析目标是跨越句子表层句法结构的束缚，直接获取深层的语义信息。 


LTP使用方法
-------
(1)	LTP支持在网页上在线演示其所有功能，通过文本的可视化，以树和有向图等直观的方式，呈现给用户直观的结果表示方式。但只适合了解LTP的功能，不适合批量处理数据。

在线演示的网址为： <https://www.ltp-cloud.com/demo/>

(2)	LTP支持在线调用API，在线上处理数据。这种方式简便快捷，不用下载源代码，但由于LTP平台对使用频率默认限制为每个IP 200次/秒，且对用户处理有流量的限制，这种方法只适合小批量的数据处理。对于建立大规模的语料库和大量的数据分析，是远远不够的。
(3)	下载ltp的源码到在本地，用python直接进行调用。Github上有pyltp工具，下载安装之后就可以处理大批量的语料数据了。项目地址：<https://github.com/HIT-SCIR/pyltp，这里有一个安装及使用教程：http://www.jianshu.com/p/867478f0e674>
使用本地的ltp，则不受流量和访问频率的限制，可以处理大规模的语料，用以语料库的建设。


Ltp工具是一个较为完备的处理中文语料的工具包，尽管在使用过程中发现部分分词结果和句法分析结果与预期不符，但整体而言准确率是可以接受的。

