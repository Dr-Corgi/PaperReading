## Frame Semantic Parsing

### Open-Domain Frame Semantic Parsing Using Transformers \[Element Coginition\]


## Prompting
### Prompt for Extraction? PAIE: Prompting Argument Interaction for Event Argument Extraction

### Ontology-enhanced Prompt-tuning for Few-shot Learning

### KnowPrompt: Knowledge-aware Prompt-tuning with Synergistic Optimization for Relation Extraction

## Pretrain Language Model with Knowledge
### K-BERT: Enabling Language Representation with Knowledge Graph

## Knowledge Grounded Dialogue
### DukeNet: A Dual Knowledge Interaction Network for Knowledge-Grounded Conversation
- 显式地建模了Knowledge-Tracking和Knowledge-Shifting两个过程
- 提出了一个Dual架构，通过先验和后验概率的相互逼近来无监督地实现Knowledge-Tracking模型的训练
- 通过Shifter计算τ时刻的知识分布，并采用后验Tracker重构τ-1时刻的知识状态，将重构概率视为reward

### Incremental Transformer with Deliberation Decoder for Document Grounded Conversations
- 使用Incremental Transformer增量地编码多轮对话历史
- 使用Deliberation Network在解码阶段引入Document知识，实现Knowledge-Grounded

### RefNet: A Reference-aware Network for Background Based Conversation
- 类似于CopyNet，利用复制机制从Background Knowle中复制，解决短语不完整的问题

### Sequential Latent Knowledge Selection for Knowledge-Grounded Dialogue
- 通过学习Latent Distribution解决Context-Knowledge之间的一对多问题

### Thinking Globally, Acting Locally: Distantly Supervised Global-to-Local Knowledge Selection for Background Based Conversation
- 构建Global Knowledge Selection模块，在token-level生成上提供全局知识
- 利用 Distant Supervision+Jaccard相似度 进行GKS的学习，不需要对数据进行额外的注释

### Difference-aware Knowledge Selection for Knowledge-grounded Conversation Generation
- 利用差异函数Diff(·)计算每则候选Knowledge与历史Knowledge之间的差异
- 差异本身无法反映候选Knowledge的好坏[*] 

### Unsupervised Knowledge Selection for Dialogue Generation
- 利用远程监督+知识蒸馏学习无gold-label下的KGDG问题。
- 利用微调+预训练模型解决知识不匹配问题
- 不采用Gold Label进行KS模块的训练，
- 远程监督：首先评估每个候选knowledge与target response之间的相似程度，将最相似的knowledge片段作为gold。

### Reinforced Multi-Teacher Selection for Knowledge Distillation
- 利用多个Teacher模型进行蒸馏，并且动态地为Teacher模型分配权重

### Knowledge Aware Conversation Generation with Explainable Reasoning over Augmented Graphs
- 将非结构化文本扩展到知识图上，再利用RL Agent在图上进行游走
- 每一次的initial state s_0是从哪里开始? [*] 

### Multiple knowledge syncretic transformer for natural dialogue generation
- 在非结构化知识的基础上结合token级别的label knowledge
- 将Encoder改造为接收Context和Unstructured Knowledge作为输入的网络

### PLATO-2: Towards Building an Open-Domain Chatbot via Curriculum Learning
- 提出了一个两阶段的对话学习：第一阶段进行粗粒度的通用响应学习，采用经典的Transformer-based E2E方法构建响应生成模型；第二阶段进行细粒度的学习，具体又划分为两步：①学习一个Latent Variable，并根据采样结果生成N个候选结果，②通过RCE选出最优的响应进行回复
- 在进行Stage 2.1的训练时，对于同一个Context会有多个不同的Target Response吗？否则对于不同的Latent Variable，其学习目标是相同的响应？[*]

### More is Better: Enhancing Open-Domain Dialogue Generation via Multi-Source Heterogeneous Knowledge
- MSKE可同时利用多个异构知识源提高知识覆盖率；提出Multi-Reference Selection来选择上下文和知识以避免不同知识源之间的主题冲突；提出基于Multi-Reference的生成方法
- 使用四种不同来源的知识：Dialogue、Commonsense、Text、Infobox
