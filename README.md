# 家国梦自动卸（橙）货

PC上模拟器实现家国梦自动精准卸货，并通过重新登陆刷新火车。  
一辆火车卸货+重登需**10秒**左右，其余为等待下一辆火车的时间。目前可能仅适用于QQ登陆。  
同时支持自动收钱，自动升级建筑，自动避免家国之光打断。

适用模拟器：腾讯手游助手  
分辨率设置：1024*576  

# 所需软件
1.腾讯手游助手  
2.按键精灵手机助手  

# 使用方法
1.安装腾讯手游助手及家国梦，在模拟器中通过QQ登陆游戏会自动安装QQ  
2.安装按键精灵手机助手  
3.在按键精灵手机助手中新建脚本，切换到“源文件”，将jgm_auto_load.txt中代码内容复制进去  
![Image text](https://github.com/LSC527/jgm_auto_load/blob/master/%E6%8C%89%E9%94%AE%E7%B2%BE%E7%81%B5%E6%89%8B%E6%9C%BA%E5%8A%A9%E6%89%8B%E8%8A%82%E9%9D%A2.png)
4.连接模拟器，并会在模拟器中自动安装按键精灵  
5.连接模拟器后，打开之前创建复制的代码，在按键精灵手机助手中点击“调试”开始挂机卸货，需要停止时点击左下角“中止”  

# 功能调整
#### 1.调整只收橙色货物/全部货物  
取消代码91行处的注释（删除“//”）即可收取全部货物，重新注释（添加“//”）后只收橙色货物  
  
#### 2.更换需要升级的建筑位置  
建筑位置标号位置为  
7 8 9  
4 5 6  
1 2 3  
更改代码38行处idx的值可更换需要升级的建筑位置  
  
#### 3.调整收钱频率
更改代码130行处的iter值，iter代表每iter*1秒收取一次钱并升级一次建筑  

# 注意事项
1.如果模拟器重新登陆时较卡导致无法重登，可以调大代码中restart函数中的3个delay值（代码116-125行）  
  
2.如果碰到重登过程无法进行或不流畅，可尝试修改restart函数中几个按钮的坐标值（代码116-125行）  
![Image text](https://github.com/LSC527/jgm_auto_load/blob/master/%E6%8A%93%E6%8A%93%E6%8C%89%E9%92%AE.png)
