# DeepLearning-DNN-Scratch
交大深度學習課程作業 手刻DNN

## Overview
### /deeplearning/Activations/activations.py
|Name|Description|
|----|----|
|Softmax|Activation function (SoftMax)|
|ReLU|Activation function (ReLU)|
|Leaky_ReLU|Activation function (Leaky ReLU)|
|Defult|Activation function (不經過函數變換直接輸出)|
|calculate_derivative|用來處理關於Activation function的微分|

### /deeplearning/Layer/layer.py
Input (Class) 
|Name|Description|
|----|----|
|__init__	|用來定義輸入層，input_shape為輸入資料的張量大小(shape)|

Dense (Class)  
|Name|Description|
|----|----|
|__init__	|用來定義全連接層，units為神經元個數，activation用於設置Activation function，use_bias用於決定是否要在計算中加入bias|

### /deeplearning/Losses/losses.py
|Name|Description|
|----|----|
|cross_entropy_error|Loss function (Cross Entropy Error)|
|sum_square_error|Loss function (Sum Square Error)|
|root_mean_square_error|Loss function (Root Mean Square Error)|
|calculate_derivative|用來處理關於Loss function的微分，index用來設置要對y_pred, y_true中的哪一項數值進行微分|

### /deeplearning/Model/model.py
|Name|Description|
|----|----|
|xavier_initialization|用來計算適合的權重初始值，n_in為上一層的神經元數，n_out為下一層的神經元數，weight_size是所需權重的張量|
Model (Class)

|Name|Description|
|----|----|
|__init__|用來定義模型|
|add	將layer添加至模型|
|initialize|建立各層之間的關係，設置權重和偏量的初始值，設置Loss function，metrics用於設置顯示的指標|
|visual|顯示結構|
|predict|預測|
|update|更新權重和偏量|
|average_update_value|平均所有樣本對權重的影響|
|forward|正向傳播|
|backward|反向傳播|
|caculate_error_rate|計算錯誤率|
|train|訓練|
