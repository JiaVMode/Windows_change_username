# Win11修改用户名（注册表法）
help user change the username which was set in Chinese

# 一、创建一个新的账户，并给予管理员权限
![image](https://github.com/user-attachments/assets/016f2608-30f2-4525-8716-76dd50250f8b)
![image](https://github.com/user-attachments/assets/299775e2-130f-45a3-967c-d758156d5a1f)
![image](https://github.com/user-attachments/assets/c88048eb-2306-4c78-b8b5-c35debb62718)
![image](https://github.com/user-attachments/assets/8571d332-5196-44c0-aad1-c7439f0c8fbb)
![image](https://github.com/user-attachments/assets/41f46ece-c2b5-47f4-8463-c545659fab84)

# 二、注销需要修改的用户（然后切换到刚创建的管理员用户）
![image](https://github.com/user-attachments/assets/0e492b42-847c-4746-9165-14fbd333f11c)\

# 三、在创建的用户下修改
Win+R输入regedit打开注册表\
![image](https://github.com/user-attachments/assets/c3555abe-8ec8-42e3-984d-63f578ab7447)\
定位到这个文件夹下：\
计算机\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion
找到RegisteredOwner\
![image](https://github.com/user-attachments/assets/7cace9cd-4003-4f22-9b78-75fbf1ccf3d0)\

右键选择修改，将后面的改为你想修改的名字即可。
# 四、修改账户对应的SID下的用户名
定位到：\
计算机\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\ProfileList
文件夹下\
一般有几个文件\
![image](https://github.com/user-attachments/assets/2930f00e-d33e-4eee-8417-47e282b77bcb)\
查看右边ProfileImagePath
找到值为你需要修改的名字\
![image](https://github.com/user-attachments/assets/8f30cfaa-2889-4e0c-9748-fec7da10c9c8)
右键选择修改，也将后面的改为你想修改的名字即可。
# 五、将C盘目录下的用户文件夹改为你新建的名字即可
1. 按Win+E启动资源管理器并导航到C:\users\
![image](https://github.com/user-attachments/assets/6f43f39f-d703-412c-85bd-2101db53ced9)\
2. 右键单击要更改的用户文件夹，然后选择重命名。\
![image](https://github.com/user-attachments/assets/4de166af-bd38-4552-aa3e-dd47a802a8c0)\
3.重新登录即可，修改成功
** 警告：三个名字要修改的一样**
# 六、修改用户属性下的名字（不改也不影响使用）
1. 按Win+R，输入netplwiz。\
![image](https://github.com/user-attachments/assets/ebb0f02b-f074-4bcf-9cc3-317a367b7c3d)\
2. 选择你登录的用户，然后单击“属性”按钮\
![image](https://github.com/user-attachments/assets/1ff529d5-2ce0-4129-9b18-0b8b89621bd1)\
3. 设置的用户名和全名\
![image](https://github.com/user-attachments/assets/570bd145-ed6c-40ac-9421-bfe0cc22d84a)

# 附：有些只修改了一部分注册表导致以下情况的
![image](https://github.com/user-attachments/assets/fc27c6dd-73e1-4a29-bd32-19650ab55528)\
打开注册表所在位置，你会发现第四步用户SID下会有两个相同名称但后缀不一样的文件。把两个文件中的修改位置的名字改回原来的位置，然后注销重新登录。即可恢复，再重新按上面步骤修改即可。

