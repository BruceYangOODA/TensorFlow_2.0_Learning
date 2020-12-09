
# [TensorFlow與Keras :Python深度學習應用實務](https://www.flag.com.tw/books/product/F9744)  


04_activation  
05_model_SafeLoad  
06_pandas_normalization  
07_img_mask  
08_CNN_mnist  
09_EncoderDecoder_mnist  
11_GRU_LSTM_imdb  



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
### 07_img_mask
from scipy import signal  
c_digit = signal.convolve2d(img, sharpen, boundary="symm", mode="same")  
img = np.load(file_path, allow_pickle=False, encoding='ASCII')  
### 08_CNN_mnist
preds = model.predict_classes(x_test)  
probs = model.predict_proba(x_test_digit, batch_size=1)   
### 09_EncoderDecoder_mnist
### 11_GRU_LSTM_imdb
word_index = imdb.get_word_index()  
decode_word_map = dict([(value, key) for (key, value) in word_index.items()])  
decoded_indices = [decode_word_map.get(i-3, "?") for i in X_train[0]]  
x_train = keras.preprocessing.sequence.pad_sequences(x_train, maxlen=max_words)  


