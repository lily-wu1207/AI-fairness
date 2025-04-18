# AI公平性研究
## 1.公平性的定义？
公平性指模型的预测结果不应该受敏感属性的影响（直接/代理的影响），在具体的矩阵度量上，可分为群体公平和个体公平两种，可数学化表示为预测结果/真实结果与敏感属性独立。
## 2.如何解决？
歧视的产生分为数据、算法、用户交互三方面，且彼此互相影响。在AI模型处理上，主要解决数据和算法带来的歧视。目前，主流的AI公平性模型主要分为处理pre-processing, in-processing, post-processing三个部分：  
pre-processing：在处理前，通过数据变型transform，数据加权，数据采样、GAN生成等方式对数据集进行“修正”；  
in-processing：在处理中，可以通过施加公平性约束 / 设计相关损失函数、通过对抗训练降低鉴别器预测出敏感属性的能力、在表示学习方面，有基于信息论或是条件对比学习降低表示与敏感属性的互信息（mutual information），有基于解纠缠表征（disentangled representation）使得敏感和非敏感属性出现在表示中不同维度从而将敏感属性与最终表征分离；还有通过GNN或者因果分析进行歧视链的发现和去除歧视的研究。  
post-processing：在处理后，有通过校验（calibration），设置阈值（thresholding）等方式对模型的输出进行“修正”。  
## 3.具体应用领域？
目前，除了传统的CV，NLP模型中公平性的研究之外，也有许多其他模型或是具体应用场景需要引入公平性的研究。如现有的supernet训练，pruning网络剪枝，深度度量学习DML等都会存在甚至放大数据集中的偏见；在如联邦学习VFL，医疗数据迁移EHR等应用场景中也需要保证模型结果的公平性。
## 4.存在的问题/可研究的方向？
公平性与准确性之间的trade-off；敏感属性标签缺失的情况下公平性的保障；与具体领域/现有模型的结合 -- 定义相关的公平标准，设计相关算法等。
## 5. 我目前的研究进展（感兴趣的方向）
偏技术 - 刻板印象结合模型可解释性：利用probing, representation learning等方法定位模型刻板印象到具体的参数结构 

偏应用 - 刻板印象结合agent社交传播：研究在agent的互动场景下，刻板印象是如何进行传播的，以及如何进行干预



