# 工程：物联网事件监控系统（github内容补充）  
## error 
在编译IoTEventMonitorPlatform时出现错误提示：  
错误1：“QApplication: 没有那个文件或目录。  
解决办法：  
下载安装Qt5.11.1并在～/.bashrc中配置环境变量。  

错误2：fatal error: GL/gl.h: No such file or directory  
 include <GL/gl.h>   
 解决办法：   
I've seen some previous posts that suggest doing  
sudo apt-get install libglu1-mesa-dev freeglut3-dev mesa-common-dev   

注意：  
在导入event工程时，Build Build - Build Artifasts - Build File - Project Structure - Libraries - "+" - Java - linux_x64.jar中的Linux—x64.jar是工程中的lib/rxtx/RXTXcomm.jar

## 执行  
在执行IoT工程时需要在终端执行sudo命令运行CLionProject/IoT/bin/IoT工程：  
sudo ./IoTEventMonitorPlatform  
在虚拟机端运行Event工程时，命令：sudo java -Djava.library.path=pathof/RXTX -jar -Xint pathof/EventSimulation4Java.jar  
注：在.jar文件所在目录下执行sudo java -Djava.library.path=/home/vm/EventSimulation4Java/lib/ -jar -Xint EventSimulation.jar