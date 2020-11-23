

# [輕鬆學會 Google TensorFlow 2.0 ](https://github.com/taipeitechmmslab/MMSLAB-TF2)
## 人工智慧深度學習實作開發


conda install pydot
https://www2.graphviz.org/Packages/stable/windows/10/cmake/Release/x64/
path setting -> C:\Program Files (x86)\Graphviz2.44\bin



Kaggle  
https://www.kaggle.com/harlfoxem/housesalesprediction


02_Regression_kc_house_data  



### 02_Regression_kc_house_data
Regression -> MSE(Mean Squared Error) or MAE(Mean Absolute Error)  
二元分類 -> BCE(Binary CroosEntropy)  
多元分類 -> CCE(Categorical CrossEntropy)  

from Ipython.display import Image  
from tensorflow.keras import utils  
utils.plot_model(model, to_file=filepath)  
Image(filepath)  

data["year"] = pd.to_numeric(data["date"].str.slice(0,4))  
data.drop(labels=["id","date"], axis="columns", inplace=True)  
np.random.permutation(x : int or array_like)  
model_cbk = callbacks.TensorBoard(log_dir=log_dir)  
model_mcbk = callbacks.ModelCheckpoint(model_dir+"model_02.h5", monitor="val_mean_absolute_error", save_best_only=True, mode="min")  


