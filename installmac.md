
苹果电脑: 安装Rime鼠须管输入法框架和汉字树拼形输入法（注：将逐步简化安装步骤）


1）用游览器从以下网址下载并安装鼠须管输入法框架0.15.2

https://rime.im/

![alt text](https://github.com/hanzishu/hanzishu/blob/main/mac0152.png)
                       
注意：因为该程序不在苹果应用商店，为了运行该程序，你需要到“系统喜好-〉安全和隐私”处，作以下设置.

![alt text](https://github.com/hanzishu/hanzishu/blob/main/privacy.png)
       
                       
2） 选择鼠须管 

![alt text](https://github.com/hanzishu/hanzishu/blob/main/choosesquirrelkeymapping.png)
                      
3） 安装汉字树拼形输入法和袖珍拼音文件

从一个终端，执行以下指令 （建议一行一行复制/拷贝）:

cd ~/Library/Rime
curl -fsSL https://git.io/rime-install | bash -s -- hanzishu/hanzishu
curl -fsSL https://git.io/rime-install | bash -s -- rime/rime-pinyin-simp

注意：如果你遇到“No such file or dictionary”的信息，你可以直接下载下面4个文件，然后拷贝到安装地点 ~/library/rime (就是/users/[你的名字]/library/rime). 如果文件的内容显示在游览器上，你可以将它存在本地文件。在Finder程序中，你可以选择Go > Go to Folder, 然后在窗口中打入‘Go’到达~/Library。

https://github.com/hanzishu/hanzishu/blob/main/hanzishu.dict.yaml
https://github.com/hanzishu/hanzishu/blob/main/hanzishu.schema.yaml
https://github.com/rime/rime-pinyin-simp/blob/master/pinyin_simp.dict.yaml
https://github.com/rime/rime-pinyin-simp/blob/master/pinyin_simp.schema.yaml
[Note: There is an underscore '_' between ‘pinyin’ and ‘simp.dict.yaml’.]

4） 将选择的输入法写入一个新创立的文件	

从一个终端，执行以下指令（建议一行一行复制/拷贝）:

cd ~/Library/Rime
echo "patch:" > ~/Library/Rime/default.custom.yaml
echo " schema_list:" >> ~/Library/Rime/default.custom.yaml
echo " - schema: hanzishu" >> ~/Library/Rime/default.custom.yaml
echo " - schema: pinyin_simp" >> ~/Library/Rime/default.custom.yaml
      

5） 重新部置		Re-deploy

在鼠松管设置中，执行“重新部置”指令.

![alt text](https://github.com/hanzishu/hanzishu/blob/main/deploymenu.png)
                           
现在，在需要时，你就可以按照第二步选择鼠须管, 在各个程序中,比如，游览器，微软的Word或Excel等，使用汉字树拼形输入法输入汉字了。



