# Time_sync_app
用于蓝牙设备的时间同步APP

## Quickstart
首先，安装仓库目录下的app-release.apk。

安装完毕后，点击首页上方的红色按钮，打开手机蓝牙和GPS，并获取必要的权限(下图中我的手机分别缺少了Blue Permission和GPS Permission)
![Alt text](./assets/e33bef58ce7f6e9ddabb23bc9ae58e2.jpg)
![Alt text](./assets/7e53f090b8dd5ecb1b6097f338f7c31.jpg)

获取权限完毕后，点击右下方的搜索按钮，获取周边的蓝牙设备。
![Alt text](./assets/3229616eb2f65b4f5892815b720acb5.jpg)
然后，点击"Connect"连接某一设备，此时会进入进阶功能界面。注意:蓝牙连接有一定的不稳定性，如果连接失败可以尝试再连接。
![Alt text](./assets/24dc65f79cf34860b1605157e0636d0.jpg)
其中，界面的蓝灰色区域为shell，输出操作信息以及返回的信息。

我们点开"Unknow Service"，并且点击"Sync Time"，可以看到，shell中返回了写数据成功的信息以及数据内容(一个256bit的时间戳数据,可以在`./device_control`中的`generateTimestampData()`函数中修改输出怎样格式的时间戳数据)。
![Alt text](./assets/853b3d779904838be393664a0229f1f.jpg)
![Alt text](./assets/62e131dd2e974db4d9e95f2e7b23835.jpg)