    我的实验环境:
    python: 3.10.14
    torch: 2.2.2+cu121
    torchvision: 0.17.2+cu121
    timm: 1.0.7
    mmcv: 2.2.0
    mmengine: 0.10.4
    
    
  1. 执行pip uninstall ultralytics把安装在环境里面的ultralytics库卸载干净.<这里需要注意,如果你也在使用yolov8,最好使用anaconda创建一个虚拟环境供本代码使用,避免环境冲突导致一些奇怪的问题>
    2. 卸载完成后同样再执行一次,如果出现WARNING: Skipping ultralytics as it is not installed.证明已经卸载干净.
    3. 如果需要使用官方的CLI运行方式或者多卡运行,需要把ultralytics库安装一下,执行命令:<pip install -e .>,请注意此命令需要在本项目的路径下执行,当然安装后对本代码进行修改依然有效.注意:不需要使用(官方的CLI运行方式、多卡运行),可以选择跳过这步.
    4. 额外需要的包安装命令:
        pip install timm==1.0.7 thop efficientnet_pytorch==0.7.1 einops grad-cam==1.4.8 dill==0.3.8 albumentations==1.4.11 pytorch_wavelets==1.3.0 tidecv PyWavelets opencv-python -i https://pypi.tuna.tsinghua.edu.cn/simple
        以下主要是使用dyhead必定需要安装的包,如果安装不成功dyhead没办法正常使用!如果执行了还是不成功,可看最下方mmcv安装问题.
        pip install -U openmim -i https://pypi.tuna.tsinghua.edu.cn/simple
        mim install mmengine -i https://pypi.tuna.tsinghua.edu.cn/simple
        mim install "mmcv>=2.0.0" -i https://pypi.tuna.tsinghua.edu.cn/simple
    5. 运行时候如果还缺什么包就请自行安装即可.