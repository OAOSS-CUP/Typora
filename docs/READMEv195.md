# Typora安装教程

## 下载

[Release](https://github.com/OAOSS-CUP/Typora/releases)

点击Assets中的exe
![image](https://github.com/user-attachments/assets/9639a393-99d2-4e07-9bac-e36b5dc9f12a)


## 安装

勾选创建桌面快捷方式

![image-20240930151617742](https://github.com/user-attachments/assets/cb177e15-3902-432b-98c7-51a8c885e212)

点击Install，等待下载完成

![image-20240930151652277](https://github.com/user-attachments/assets/45e98106-0f91-4e39-8a7b-fd3b97acfa62)

下载完成后，**不要勾选Launch Typora**（不过勾选了关掉也行）

![image-20240930151853836](https://github.com/user-attachments/assets/32069226-2ae6-41df-abfc-c15bf9a1f61f)

在桌面找到Typora图标，右键选择**打开文件所在位置**

![image-20240930151950551](https://github.com/user-attachments/assets/497d342d-7840-4469-b0dd-319b84e0f5cc)


## 破解

### 第一步

进入这个路径
```
\resources\page-dist\static\js
```
找到名为Licenseindex的js文件
![image](https://github.com/user-attachments/assets/194f789c-f894-42ea-a9d7-cf768fd7414c)

用VScode打开，**Ctrl+F**查找**e.hasActivated**
![image](https://github.com/user-attachments/assets/04a24fde-5c1d-4cab-bc5f-6fc15b6e4be2)

将这段
```
e.hasActivated="true"==e.hasActivated
```
替换为
```
e.hasActivated="true"=="true"
```
然后关闭

### 第二步

用VScode打开这个文件
```
\resources\page-dist\license.html
```
![image](https://github.com/user-attachments/assets/3b89388f-f8db-4d8e-8ebd-e99b6e085d9d)

右键选择**格式化代码**

![image](https://github.com/user-attachments/assets/f4898a18-dacc-4e4a-a7d0-d94547f0d663)

翻到最下面，找到如下代码
```html
</body>

</html>
```

在"/body"的上一行加上
```html
<script>window.οnload = function () { setTimeout(() => { window.close(); }, 5); }</script>
```

### 第三步

用VScode打开这个文件
```
\resources\locales\zh-Hans.lproj\Panel.json 
```
![image](https://github.com/user-attachments/assets/b939f8f7-be14-4592-824a-044977243353)

**Ctrl+F**查找
```json
"UNREGISTERED":"未激活"
```

替换为
```json
"UNREGISTERED":" "
```

*就这样，是不是很简单~*
