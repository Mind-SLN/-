一、文本向量化
*概念：
(1)One hot presentation：词典中每个单词的频率
问题：维度灾难；语义鸿沟；词序信息
(2)word2vec/doc2vec：根据上下文与目标词之间的关系建模
基于“分布假说”：上下文相似的词，语义也相似
1、word2vec:语义信息
*词向量的训练：
(1)文本预处理，分词
(2)训练词向量，保存为*.word2vec文件



*相似度演示：
(1)单词相似度

gensim.models.Word2Vec.load(.word2vec_file_path)
.similarity(word1,word2)
.most_similarity(word)

(2)文本相似度
①关键词提取
②关键词向量化；各词向量相加，得到文本总向量

④计算两个文本向量的相似度



2、doc2vec:语义信息+词序信息
*段落向量的训练：
(1)文本预处理，TaggedWikiDocument分词，考虑tag属性，训练模型

(2)段落向量训练
import gensim.models as g


*相似度演示：
文本相似度
将文档分词后放在doc中，用infer_vector直接转换成转换成向量
