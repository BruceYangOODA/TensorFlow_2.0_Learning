
# [TensorFlow與Keras :Python深度學習應用實務](https://www.flag.com.tw/books/product/F9744)  


04_activation  
05_model_SafeLoad  
06_pandas_normalization  



### 04_activation  
### 05_model_SafeLoad
df.to_html(path)  
json_str = model.to_json()  f.write(json_str)  
model.save_weights(weight_path)  
model.save(model_path)  
### 06_pandas_normalization
import seaborn as sns  
sns.pairplot(df, hue="target")  
df.describe()  
df.info()  
df[["age"]] = df[["age"]].fillna(value=age_mean)  
target_mapping = {"setosa":0, "versicolor":1, "virginica":2}  
Y = df["target"].map(target_mapping)  
embarked_one_hot = pd.get_dummies(df["embarked"], prefix="embarked")  
tb = pd.crosstab(Y_target, Y_pred, rownames=["label"], colnames=["predict"])   







