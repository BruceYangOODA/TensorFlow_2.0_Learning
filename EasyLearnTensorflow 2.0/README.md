

# [輕鬆學會 Google TensorFlow 2.0 ](https://github.com/taipeitechmmslab/MMSLAB-TF2)
## 人工智慧深度學習實作開發

常見的監督式學習方法  
最鄰近法(K-Nearest Neighbors, KNN)  
決策樹(Decision Trees)和隨機森林(Random Forests)  
支援向量機(Support Vector Machines, SVM)  
深度神經網路(Deep Neural Networks, DNN)



conda install pydot
https://www2.graphviz.org/Packages/stable/windows/10/cmake/Release/x64/
path setting -> C:\Program Files (x86)\Graphviz2.44\bin



Kaggle  
https://www.kaggle.com/harlfoxem/housesalesprediction


[Python实现Github下载工具](https://blog.csdn.net/sherpahu/article/details/81022575)  

02_Regression_kc_house_data  
03_Pokemon_PK  
04_CNN_cifar10  
05_BatchNormalization_cifar10  
06_CustomModel_cifar10  
07_TensorBoard  
08_load_classical_model  
Lab9.ipynb  

### 02_Regression_kc_house_data
Regression -> MSE(Mean Squared Error) or MAE(Mean Absolute Error)  
二元分類 -> BCE(Binary CroosEntropy)  
多元分類 -> CCE(Categorical CrossEntropy)  
BCE 損失函數為 sigmoid激活函數和 CrossEntropy損失函數，所以又稱為 Sigmoid CrossEntropy  
onehot encoding 類別之間沒有連續關係，訓練出來的表現會比用數值訓練的好  

from Ipython.display import Image  
from tensorflow.keras import utils  
utils.plot_model(model, to_file=filepath)  
Image(filepath)  

data["year"] = pd.to_numeric(data["date"].str.slice(0,4))  
data.drop(labels=["id","date"], axis="columns", inplace=True)  
np.random.permutation(x : int or array_like)  
model_cbk = callbacks.TensorBoard(log_dir=log_dir)  
model_mcbk = callbacks.ModelCheckpoint(model_dir+"model_02.h5", monitor="val_mean_absolute_error", save_best_only=True, mode="min")  

method_1  
%load_ext tensorboard  
%tensorboard --logdir lab2-logs  
method_2  
cmd  ->
tensorboard --logdir lab2-logs  
http://localhost:6006/  
變更瀏覽的阜號  
tensorboard -port 9527 --logdir lab2-logs  
http://localhost:9527/  

### 03_Pokemon_PK
from urllib.request import urlretrieve  
urlretrieve(url, filename=filepath)  
data_df = data_df.set_index(str_index)  
data_df.info()  
data_df["Type 1"].value_counts(dropna=False)    
data_df["Type 1"].fillna("empty", inplace=True)  
type1_dict = dict(enumerate(data_df["Type 1"].cat.categories))  
data_df["Type 1"] = data_df["Type 1"].cat.codes  
data_df["Type 1"] = data_df["Type 1"].cat.codes.values  
model_cbk = keras.callbacks.TensorBoard(log_dir=log_dir)  
model_mckp = keras.callbacks.ModelCheckpoint()  

### 04_CNN_cifar10
pip install tensorflow-datasets  
pip install git+https://github.com/tensorflow/datasets.git  

import tensorflow_datasets as tfds  
tfds.list_builders()  顯示TensorFlow Datasets目前提供的數據集  

model_cbk = keras.callbacks.TensorBoard(log_dir=log_dir)  
model_mckp = keras.callbacks.ModelCheckpoint(model_dir + '/Best-model-1.h5', monitor='val_categorical_accuracy', save_best_only=True, mode='max')  
### 05_BatchNormalization_cifar10
使用 Sigmoid或 Tanh作為激活函數，建議使用 Glorot初始函數  
使用 ReLU或其他變形作為激活函數，建議使用 He初始函數  
使用 ReLU作為激活函數，其性能優於 Sigmoid或 Tanh  

BatchNormalization 對輸入網路的每一批次batch資料，在每一層的網路網路輸出進行標準化  
權重初始化，可以使用較大的學習率訓練網路，加速網路訓練速度  
BatchNormalization 優點整理  
* 不需依賴權重初始化方法
* 減少梯度消失或梯度爆炸
* 避免過度擬合(減少Dropout或Regularization的使用)
* 加快學習速度(減少Internal Covariate Shift的問題，可以使用較大的學習率訓練)
### 06_CustomModel_cifar10
### 07_TensorBoard

### 08_load_classical_model
model = tf.keras.applications.InceptionV3(include_top=True, weights='imagenet')  
top3_indexs = np.argsort(preds)[0, ::-1][:3]   
conda install tensorflow-hub  
hub.KerasLayer(module_url, input_shape=(299, 299, 3), output_shape=(1001, ), name='Inception_v3') 

Lab9.ipynb

