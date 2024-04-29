# Undergraduate-design
Risk Assessment of Loan decision based on Data Mining -- Taking the online loan data of Lending Club as an example
摘  要
本文针对P2P网贷市场中的信贷风险预测问题进行了深入研究。目前P2P网贷研究主要集中在运营模式、交易行为、借贷风险和社会网络等方面，但现实中多方面因素的影响难以全面考虑。通过对大量贷款数据的分析和挖掘，对从2007年到2020年实际发放的贷款信息，总计有2925493行数据，142个字段总结重要的可用借款人信息，综合数据集的已知借款人的基础历史信息与借款信息，针对信贷数据繁杂且包含信息混杂等问题，基于业务理解进行数据理解，提出基于贷款申请信息的属性划分方法，并结合客户细分形成信贷数据对象。数据的选择和处理上，根据官方网站对客户的的二级评级进行等级分类赋分，通过数据预处理技术，包括空值和重复行的删除、离群异常值的去除、单位和符号的去除，以及数据归一化处理，来确保数据集的质量和一致性。在剔除无关变量后，通过特征工程，包括特征衍生、特征抽象和特征缩放，对数据进行了进一步的优化，以提高模型的预测能力，初步处理得到18个有效列。
在特征衍生阶段，研究者利用主成分降维技术对六个高共线性特征进行降维处理，将六个特征简化为三个特征，以减少模型复杂度并提高预测精度。在特征抽象阶段，研究者采用了分类和独热编码处理对文本数据进行量化，并对客户的等级数据进行了数值映射，以便更好地适应机器学习模型。
结合处理后数据集的数据不平衡特点，分别采用随机欠采样和随机过采样对样本观测值进行采样评估，并通过实验验证了过采样技术在提高模型性能方面的有效性。使用Keras调谐器进行超参数调优得到最佳超参数，最终建立ANN网络模型对向量化的特征进行分类，并建立了相应的风险评估和预测模型，预测能够全部归还贷款，延期归还，欠款的客户，准确率达到84.52%。与逻辑回归模型和xgboost模型相比，ANN模型在预测效果上具有明显优势。
实验结果表明，随机欠采样和随机过采样相比准确率88%>13%，增加少部分样本的随机过采样在该不均衡大规模数据集更适用，能够有效地处理样本数据集。使用Keras调谐器进行超参数调优，构建了一个具有4到20个隐藏层和32到512个神经元的深度学习模型，以预测三分类问题。模型的输出层使用Softmax激活函数，并采用多类交叉熵作为损失函数。经过多次实验，模型的准确率达到84.52%，显示出较高的分类准确性。与传统的风险评估方法相比，该模型基于大数据集，能够捕捉数据中的复杂关系，为金融机构提供风险评估参考。模型的超参数调优灵活性、多分类处理能力、交叉熵损失函数的应用以及多性能指标评估，使其在实际应用中具有良好的可调性和适用价值。特征分析表明，贷款期限、信用账户数量、贷款利率等特征对于区分不同贷款客户类别至关重要。对于低风险的Paid类型客户，建议降低贷款门槛和简化申请流程；对于高风险的Late和Default类型客户，则需要加强监测、调整还款计划和贷后管理。为金融机构提供风险评估结果参考，为平台减小一定风险。
关键字：数据挖掘；贷款；风险评估；ANN人工神经网络；
 
Abstract
This paper focuses on the credit risk prediction in P2P lending market. At present, the research of P2P lending mainly focuses on the operation mode, transaction behavior, lending risk and social network. However, it is difficult to fully consider the influence of many factors in reality. Through the analysis and mining of a large number of loan data, there are a total of 2,925,493 lines of data for the actual loan information issued from 2007 to 2020. 142 fields summarize important available borrower information, and the basic historical information and loan information of known borrowers are integrated in the data set. Based on business understanding, this paper proposed an attribute division method based on loan application information, and combined with customer segmentation to form credit data objects. In the selection and processing of data, according to the official website, the secondary rating of customers is classified and assigned, and the quality and consistency of the data set are ensured by data preprocessing techniques, including the deletion of null values and duplicate rows, the removal of outliers, the removal of units and symbols, and data normalization. After eliminating irrelevant variables, the data were further optimized by feature engineering, including feature derivation, feature abstraction, and feature scaling, to improve the predictive power of the model, and 18 valid columns were obtained by preliminary processing.
In the feature derivation stage, the principal component dimension reduction technology is used to reduce the dimension of the six high collinearity features, and the six features are simplified into three features to reduce the complexity of the model and improve the prediction accuracy. In the feature abstraction stage, the researchers used classification and one-hot encoding processing to quantify the text data, and mapped the customer's rating data numerically, so as to better adapt to the machine learning model.
Combined with the data imbalance characteristics of the processed data set, random undersampling and random oversampling are used to sample and evaluate the sample observations respectively, and the effectiveness of oversampling technology in improving the performance of the model is verified by experiments. The Keras tuner was used to optimize the hyperparameters to obtain the best hyperparameters. Finally, an ANN network model was established to classify the vectorized features, and the corresponding risk assessment and prediction model was established. Compared with logistic regression model and xgboost model, ANN model has obvious advantages in prediction effect.
The experimental results show that the accuracy of random under-sampling and random over-sampling is 88%>13%, and the random over-sampling with a small number of samples is more suitable for the imbalanced large-scale data set, which can effectively process the sample data set. Hyperparameter tuning using Keras tuner, a deep learning model with 4 to 20 hidden layers and 32 to 512 neurons is constructed to predict three-class classification problems. The output layer of the model uses Softmax activation function and adopts multi-class cross-entropy as the loss function. After many experiments, the accuracy of the model reaches 84.52%, which shows high classification accuracy. Compared with traditional risk assessment methods, the model is based on large data sets, which can capture complex relationships in the data and provide risk assessment reference for financial institutions. The flexibility of hyperparameter tuning, multi-classification processing ability, the application of cross-entropy loss function and multiple performance index evaluation of the model make it have good adjustability and applicable value in practical applications. Feature analysis shows that features such as loan duration, number of credit accounts, and loan interest rate are crucial for distinguishing different loan customer categories. For low-risk Paid customers, it is recommended to lower the threshold of loan and simplify the application process. For high risk Late and Default type customers, it is necessary to strengthen the monitoring, adjustment of repayment plan and post-loan management. It provides a reference for the risk assessment results of financial institutions and reduces a certain risk for the platform.
key words: Data mining; Loan; Risk assessment; ANN artificial neural network;
