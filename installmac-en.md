
Apple Mac computer: Install Rime/Squirrel input platform and Hanzishu pictographic typing method (Note: Will gradually simplify the installation steps)


1）Use browser to download Squirrel input platform from following address：

https://rime.im/download/

Choose the newest Squirrel version, for example, Squirrel 0.16.2.

At the bottom of Assets, find the corresponding zip file “Squirrel-0.16.2.zip” and download it

Install the downloaded program by following the instructions.
                       
Note: Since the app is not from App Store, you need to go to “System Preferences->Security & Privacy” tab, and make the following settings in order to run the installation program.

![alt text](https://github.com/hanzishu/hanzishu/blob/main/privacy.png)
       
                       
2）  After installation, choose Squirrel from Mac's input method menu.

![alt text](https://github.com/hanzishu/hanzishu/blob/main/choosesquirrel.png)
                      
3） Install Hanzishu input method and Pinyin documents

From a terminal, execute following commands (suggest copy/paste one line at a time):

cd ~/Library/Rime

curl -fsSL https://git.io/rime-install | bash -s -- hanzishu/hanzishu

curl -fsSL https://git.io/rime-install | bash -s -- rime/rime-pinyin-simp

Note: In case you hit “No such file or dictionary” error, you can download the following four files directly, then copy to the installation location located at ~/library/rime (which is /users/[your_username]/library/rime). If the content of the file is displayed in a browser, you can save it to a local location. In the Finder, you can choose Go > Go to Folder, then in the dialog, type ~/Library, and choose ‘Go’ to go to the ~/Library folder.

https://github.com/hanzishu/hanzishu/blob/main/hanzishu.dict.yaml

https://github.com/hanzishu/hanzishu/blob/main/hanzishu.schema.yaml

https://github.com/rime/rime-pinyin-simp/blob/master/pinyin_simp.dict.yaml

https://github.com/rime/rime-pinyin-simp/blob/master/pinyin_simp.schema.yaml

4） Write the selected input methods into the default.custom.yaml file 	

From a terminal, execute following commands (suggest copy/paste one line at a time):

cd ~/Library/Rime

echo "patch:" > ~/Library/Rime/default.custom.yaml

echo " schema_list:" >> ~/Library/Rime/default.custom.yaml

echo " - schema: hanzishu" >> ~/Library/Rime/default.custom.yaml

echo " - schema: pinyin_simp" >> ~/Library/Rime/default.custom.yaml
      

5） Re-deploy

In Squirrel settings, execute “Deploy” command.

![alt text](https://github.com/hanzishu/hanzishu/blob/main/deploymenu.png)
                           
Now, when needed, you can choose Squirrel as shown in step 2, and use Hanzishu input method to type in Chinese characters in each program like browser, Microsoft Word or Excel, etc.

Go back to the main instrcution page： https://github.com/hanzishu/hanzishu/blob/main/README-en.md



