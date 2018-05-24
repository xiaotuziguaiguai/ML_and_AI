解决Kaggle步骤：
1、识别问题
2、分离数据
3、构造提取特征
4、组合数据
5、分解
6、选择特征
7、选择算法进行训练
一、识别问题
分类or回归
label为二进制时，为分类，label为实数时，为回归
二、分离数据
分类问题StratifiedKFold
from sklearn.cross_validation import StratifiedFolk
回归问题 KFold
from sklearn.cross_validation import kFold
三、构造特征
需要将数据转化为模型需要的形式，数字，类别，文字，当数据是类别的形式，需要将它的每一类提取出来作为单独一列，用二进制表示
理解：有多少类就有多少维度，如：二分类 0 1,1，0
from sklearn.preprocessing import LabelEncoder 
or
from sklearn.preprocessing import OneHotEncoder
四、组合数据
数据稠密
import numpy as np 
X = np.hstack()
数据稀疏
from scipy import sparse
X = sparse.hstack()
五、分解
PCA:主成分分析，分析、简化数据集，减少数据集的维度，同时保持数据集中的对方差贡献最大的特征
from sklearn.decomposition import PCA
SVD:找到标准正交基后方差最大的维度，降维度去噪，文本数据转化成稀疏矩阵
from sklearn.decomposition import TruncatedSVD
六、选择特征
当特征个数越多时，分析特征训练模型所需的时间就越长，
完全搜索，启发式搜索，随机算法
Random Forest
from sklearn.ensemble import Random ForestClassifier
xgboost
import xgboost as xgb
稀疏矩阵
from sklearn.teature_selection import SelectKBest
from sklearn.feature_selection import chi2
七、选择算法进行训练
Classification
Random Forest
GBM
Logistic Regression 
Naive Bayes
Support Vector Machines
K-Nearest Neighbors
Regression 
Random Forest
GBM
linear Regression 
Ridge
Lasso
SVR

