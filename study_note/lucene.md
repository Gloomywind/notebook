# 1. 概念

## 1.1 全文检索（Full-TextRetrieval）

- 一种解释：
  - 是指以文本作为检索对象，找出含有指定词汇的文本。
  - 全面、准确和快速是衡量全文检索系统的关键指标。
- 另一种解释：
  - 非结构化数据又一种叫法叫全文数据。从全文数据中进行检索就叫全文检索。
- 结构化数据
  - 结构化数据：指具有固定格式或有限长度的数据，如数据库，元数据等;
  - 非结构化数据：指不定长或无固定格式的数据，如邮件，word文档等;
  - 半结构化数据，如XML，HTML等，当根据需要可按结构化数据来处理，也可抽取出纯文本按非结构化数据来处理。
- 关于全文检索，我们要知道：
  - 1，只处理文本。
  - 2，不处理语义。
  - 3，搜索时英文不区分大小写。
  - 4，结果列表有相关度排序。

## 1.2 document

- MaxFieldLength：指定字段最多可存记录的大小 
- Document
  - 就是类似于我们数据库表中的一条记录，进一步说一个Document由多个Field所组成
- Field
  - 就是一条记录中的一个字段
- Store
  - yes : 表示此字段所对应的值要进行保存
  - no:  表示此字段所对应的值不保存[pdf文件、MPA音乐等一切大文本一般来说都不需要我们进行保存，只保存PATH]
- Index
  - NO：表示此字段不需要进行分词也不建立索引
  - ANALYZED：表示此字段进行分词后并建立索引
  - NOT_ANALYZED：表示此字段不进行分词但要建立索引[整个字段为一个词]

## 1.3 倒排索引

- 英文原名Inverted index，大概因为 Invert 有颠倒的意思，就被翻译成了倒排。但是倒排这个名称很容易让人理解为从A-Z颠倒成Z-A。
- 我喜欢叫她“反向索引”
- 一个未经处理的数据库中，一般是以文档ID作为索引，以文档内容作为记录。而Inverted index 指的是将单词或记录作为索引，将文档ID作为记录，这样便可以方便地通过单词或记录查找到其所在的文档。

