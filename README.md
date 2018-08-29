# 1 简介
&#8195;该库用于'达观杯'比赛的文本分类任务的基础实现，主要包括机器学习(ml)和深度学习(dl)两大部分，机器学习部分基于sklearn/lightgbm包实现，深度学习部使用pytorch深度学习框架。其中，机器学习部分主要包含特征工程和分类器两大部分，特征工程部分主要针对文本分类任务的 hash/lsa/lda/doc2vec特征提取/特征选择/特征组合/特征构造进行了实现，而分类器部分主要有逻辑回归/SVM/随机森林/Bagging/Adaboost/GBDT/Xgboost/LightGBM等。深度学习主要实现了word2vec/构建lstm模型/训练可视化等。（注：此库只是基础实现，并不是最优！！！）<br>
# 2 ml
- 1）运行环境
numpy/scipy/sklearn/xgboost/lightgbm
- 2）文件夹说明
[data]:用于存放原始数据集<br>
[features]:用于存放特征工程的代码以及生成的特征文件<br>
[code]:用于存放训练的代码<br>
[results]:用于存放测试集的训练结果，以便提交给比赛官方<br>
- 3）使用案例：
（1）生成tfidf特征<br>
直接运行features文件夹中的**tfidf.py**;<br>
（2）生成lsa特征<br>
运行features文件夹中的**lsa.py**；(注：运行前请确保tfidf特征已经生成)<br>
（3）生成lda特征<br>
运行features文件夹中的**lda.py**；(注：运行前请确保tf特征已经生成)<br>
(4)使用逻辑回归分类器进行训练<br>
修改code文件夹中的**sklearn_config.py**中的*clf_name='lr'*,然后运行**sklearn_train.py**即开始训练。<br>
(5)使用lgb进行训练<br>
修改code文件夹中的**lgb.py**中的*features_path*，然后直接运行**lgb.py**即可开始训练。<br>
