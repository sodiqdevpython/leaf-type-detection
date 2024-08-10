Error:
![image](https://github.com/user-attachments/assets/90a5b8a7-def7-41a8-9af5-20be2230f633)


Fully error message include:


PS C:\sodiq\ai> python .\main.py
2024-08-10 09:16:11.569780: I tensorflow/core/util/port.cc:153] oneDNN custom operations are on. You may see slightly different numerical results due to floating-point round-off errors from different computation orders. To turn them off, set the environment variable `TF_ENABLE_ONEDNN_OPTS=0`.
2024-08-10 09:16:12.625502: I tensorflow/core/util/port.cc:153] oneDNN custom operations are on. You may see slightly different numerical results due to floating-point round-off errors from different computation orders. To turn them off, set the environment variable `TF_ENABLE_ONEDNN_OPTS=0`.
Traceback (most recent call last):
  File "C:\Users\99899\AppData\Local\Programs\Python\Python312\Lib\site-packages\keras\src\ops\operation.py", line 234, in from_config
    return cls(**config)
           ^^^^^^^^^^^^^
  File "C:\Users\99899\AppData\Local\Programs\Python\Python312\Lib\site-packages\keras\src\layers\convolutional\depthwise_conv2d.py", line 120, in __init__
    super().__init__(
  File "C:\Users\99899\AppData\Local\Programs\Python\Python312\Lib\site-packages\keras\src\layers\convolutional\base_depthwise_conv.py", line 106, in __init__
    super().__init__(
  File "C:\Users\99899\AppData\Local\Programs\Python\Python312\Lib\site-packages\keras\src\layers\layer.py", line 266, in __init__
    raise ValueError(
ValueError: Unrecognized keyword arguments passed to DepthwiseConv2D: {'groups': 1}

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "C:\sodiq\ai\main.py", line 7, in <module>
    model = load_model("keras_model.h5", compile=False)
            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\99899\AppData\Local\Programs\Python\Python312\Lib\site-packages\keras\src\saving\saving_api.py", line 189, in load_model
    return legacy_h5_format.load_model_from_hdf5(
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\99899\AppData\Local\Programs\Python\Python312\Lib\site-packages\keras\src\legacy\saving\legacy_h5_format.py", line 133, in load_model_from_hdf5
    model = saving_utils.model_from_config(
            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\99899\AppData\Local\Programs\Python\Python312\Lib\site-packages\keras\src\legacy\saving\saving_utils.py", line 85, in model_from_config
    return serialization.deserialize_keras_object(
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\99899\AppData\Local\Programs\Python\Python312\Lib\site-packages\keras\src\legacy\saving\serialization.py", line 495, in deserialize_keras_object
    deserialized_obj = cls.from_config(
                       ^^^^^^^^^^^^^^^^
  File "C:\Users\99899\AppData\Local\Programs\Python\Python312\Lib\site-packages\keras\src\models\sequential.py", line 342, in from_config
    layer = saving_utils.model_from_config(
            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\99899\AppData\Local\Programs\Python\Python312\Lib\site-packages\keras\src\legacy\saving\saving_utils.py", line 85, in model_from_config
    return serialization.deserialize_keras_object(
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\99899\AppData\Local\Programs\Python\Python312\Lib\site-packages\keras\src\legacy\saving\serialization.py", line 495, in deserialize_keras_object      
    deserialized_obj = cls.from_config(
                       ^^^^^^^^^^^^^^^^
  File "C:\Users\99899\AppData\Local\Programs\Python\Python312\Lib\site-packages\keras\src\models\sequential.py", line 342, in from_config
    layer = saving_utils.model_from_config(
            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\99899\AppData\Local\Programs\Python\Python312\Lib\site-packages\keras\src\legacy\saving\saving_utils.py", line 85, in model_from_config
    return serialization.deserialize_keras_object(
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\99899\AppData\Local\Programs\Python\Python312\Lib\site-packages\keras\src\legacy\saving\serialization.py", line 495, in deserialize_keras_object      
    deserialized_obj = cls.from_config(
                       ^^^^^^^^^^^^^^^^
  File "C:\Users\99899\AppData\Local\Programs\Python\Python312\Lib\site-packages\keras\src\models\model.py", line 521, in from_config
    return functional_from_config(
           ^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\99899\AppData\Local\Programs\Python\Python312\Lib\site-packages\keras\src\models\functional.py", line 477, in functional_from_config
    process_layer(layer_data)
  File "C:\Users\99899\AppData\Local\Programs\Python\Python312\Lib\site-packages\keras\src\models\functional.py", line 457, in process_layer
    layer = saving_utils.model_from_config(
            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\99899\AppData\Local\Programs\Python\Python312\Lib\site-packages\keras\src\legacy\saving\saving_utils.py", line 85, in model_from_config
    return serialization.deserialize_keras_object(
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\99899\AppData\Local\Programs\Python\Python312\Lib\site-packages\keras\src\legacy\saving\serialization.py", line 504, in deserialize_keras_object      
    deserialized_obj = cls.from_config(cls_config)
                       ^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\99899\AppData\Local\Programs\Python\Python312\Lib\site-packages\keras\src\ops\operation.py", line 236, in from_config
    raise TypeError(
TypeError: Error when deserializing class 'DepthwiseConv2D' using config={'name': 'expanded_conv_depthwise', 'trainable': True, 'dtype': 'float32', 'kernel_size': [3, 3], 'strides': [1, 1], 'padding': 'same', 'data_format': 'channels_last', 'dilation_rate': [1, 1], 'groups': 1, 'activation': 'linear', 'use_bias': False, 'bias_initializer': {'class_name': 'Zeros', 'config': {}}, 'bias_regularizer': None, 'activity_regularizer': None, 'bias_constraint': None, 'depth_multiplier': 1, 'depthwise_initializer': {'class_name': 'VarianceScaling', 'config': {'scale': 1, 'mode': 'fan_avg', 'distribution': 'uniform', 'seed': None}}, 'depthwise_regularizer': None, 'depthwise_constraint': None}.

Exception encountered: Unrecognized keyword arguments passed to DepthwiseConv2D: {'groups': 1}
