# Typora安装教程

## 下载

[Release](https://github.com/OAOSS-CUP/Typora/releases)

点击Assets中的exe
![1](https://github.com/user-attachments/assets/0526ab76-a7ce-4432-84fa-cf131982aaaa)


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

![2](https://github.com/user-attachments/assets/4a80fb55-38d5-47e4-bb9d-6f8e502a2a0c)

用VScode打开，**Ctrl+F**查找**e.hasActivated**

![3](https://github.com/user-attachments/assets/a696a972-7ffe-4cdb-a738-ce98229f1992)

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

右键选择**格式化代码**

![4](https://github.com/user-attachments/assets/a2eadcda-d89d-4dba-b41f-778b030c873c)

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

**Ctrl+F**查找
```json
"UNREGISTERED":"未激活"
```

替换为
```json
"UNREGISTERED":" "
```

![5](https://github.com/user-attachments/assets/26e27af6-8417-4408-8529-4bf9a89ddf2e)

*就这样，是不是很简单~*
