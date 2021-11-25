记录一下自己配置tensorflow所遇问题，包括anaconda、CUDA、Cudnn、tensorflow、kares在Windows10下的安装。

问题一：anaconda3安装时，记得勾选第一个勾 

答：针对新手安装，勾选该选项可以直接配置好环境 
![image](https://user-images.githubusercontent.com/92359626/143460717-993bf7d6-ead1-4bb5-b9f6-5795674450fd.png)

问题二：anaconda安装时，记得选对路径

答：英文路径，可以不默认装在C盘

问题三：CUDA安装时路径

答：针对新手，最好使用默认C盘地址安装。如果C盘空间不够，再考虑换成其它盘，但是会有安装失败的风险 。

问题四：由于版本是tensorflow-gpu=1.13.2，会使用cuda10.0，与cuda10.0对应的cudnn是7.4.1.5。

答：tensorflow最好使用python3.6版本进行配置，不然在下载时，cmd会弹出版本不兼容的错误。可以使用anaconda存放多个python版本，例如我anaconda自带的是python3.8，但是创建了一个新环境，使用python3.6配置tensorflow及Kares。

如下图所示，可切换兼容不同的python版本。demo为3.8，tensorflow-gpu为3.6。环境均可以自己命名。


![image](https://user-images.githubusercontent.com/92359626/143460752-5acfe09c-0f97-4d68-b312-c283a7368f7f.png)

问题五：tensorflow库安装时，弹：Cache entry deserialization failed, entry ignored

答：输入 python -m pip install -U pip，如果不成功，多试几次

问题六：ModuleNotFoundError: No module named 'kares'

答：应该有两种情况，一个是没有下载kares依赖库，一个是装到其他的环境上去了，当前代码所运行的环境，或者目前激活的环境，不是装有库的环境

问题七：如何将pycharm切换成python3.6（TensorFlow-gpu）版本

答：如图所示步骤，选取anaconda-evn-TensorFlow-python.exe文件

![image](https://user-images.githubusercontent.com/92359626/143460787-1d4eaeda-7480-48be-8f22-98c4aa915af2.png)
![image](https://user-images.githubusercontent.com/92359626/143460816-fa0528cb-53f2-430d-a8ce-e3c688108a41.png)
![image](https://user-images.githubusercontent.com/92359626/143460802-5f09484f-461c-46e9-b30c-96d0c54f3e24.png)
![image](https://user-images.githubusercontent.com/92359626/143460832-38ba3d13-b872-4f9d-ad7d-7bccb886a75b.png)

 最后，可以看到pycharm成功切换至py3.6，且是配置好环境的python版本，例如存在kares依赖库

