
### [Tensorflow API](https://www.tensorflow.org/api_docs/python/tf/transpose)  ### [Keras API](https://keras.io/api/)
### [Numpy API](https://numpy.org/doc/stable/reference/index.html)

[关于 Markdown](https://xianbai.me/learn-md/article/syntax/paragraphs-and-line-breaks.html)  

Tensorflow_2.0_Towards

02_Tensorflow_basic_API  
03_Keras_intro  

### 02_Tensorflow_basic_API
tf.convert_to_tensor()   
tf.Variable()  
tf.random.normal(shape, mean=0.0, stddev=1.0)  高斯分配  
tf.random.truncated_normal(shape, mean=0.0, stddev=1.0)  超過兩倍stddev 重新隨機  
tf.random.uniform(shape, minval=0, maxval=None) 隨機均勻分配  
tf.transpose(a, perm=None)  維度置換  
tf.expand_dims(input, axis)  維度擴張  
tf.stack(values, axis=0)  陣列合併  
tf.unstack(value, num=None, axis=0)  陣列分離  
tf.split(value, num_or_size_splits, axis=0)  陣列切分  
tf.reshape(tensor, shape)  
tf.sort(values, axis=-1, direction='ASCENDING') 值排序direction='DESCENDING'  
tf.argsort(values, axis=-1, direction='ASCENDING')  索引 值排序  
tf.math.top_k(values, k=5)  
tf.pad(tensor, paddings) padding [上,下],[左,右]  
tf.clip_by_value(t, clip_value_min, clip_value_max)  設定上下限值
### 陣列運算
tf.add()  
tf.matmul()  
tf.reduce_mean(input_tensor, axis=None, keepdims=False)  維度平均值  
tf.argmax(input, axis=None, output_type=tf.dtypes.int64)  維度最高值 index  


### 03_Keras_intro
自定義 Layer  
自定義 Model  
模型儲存  
檔案讀取  
model.save_weigits(filepath)  
model = create_model()  
model.load_weights(filepath)  

model.save(filepath)  
model = models.load_model(filepath)  

tf.data.TextLineDataset(filenames)  
tf.keras.utils.get_file(fname, origin=URL)  
pd.read_csv(filepath)  
