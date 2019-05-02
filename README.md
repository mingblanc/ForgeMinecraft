<h1>这是一个我的世界forge版本。</h1><br>
  使用了官方版和forge版解压jar包后，合并在一起的jar包。<br>

<h2>文件属性</h2><br>
server.properties--服务器具体配置，具体参数wiki <a href="https://minecraft.gamepedia.com/Server.properties">server.properties。</a><br>
withelist.json--服务器白名单，在白名单内才可以进入服务器。<br>
ops.json--管理员名单。<br>
eula.txt--需要同意这个协议。<br>
bkrun.sh--自己写的后台运行脚本。<br>
connectbkrun.sh--自己写的脚本，离开screen窗口后用来重连的。<br>
cleanworld.sh--自己写的脚本，运行后可以清理地图存档。<br>
  其他的我也不知道了。
  

<h2>运行方式：</h2>    
<h3>检查是否安装java环境</h3>

    yum list java*
    
查看yum源中的所有java包
    
    yum install -y java-1.8.0-openjdk
    
安装java

<h3>运行</h3> 

    java -Xms256M -Xmx512M -jar forge_minecraft1.7.10.jar nogui
         最小内存  最大内存                                 不启动gui
但是运行了这个命令后会导致不能关闭服务器窗口，关闭窗口后，服务器后台也会被关闭。所以我使用了 screen工具。     
<h3>下载screen工具</h3>

    yum install -y screen

<h3>后台运行</h3>

    ./bkrun.sh  
    
ctrl+a+d 退出窗口。               
<h3>重新进入窗口运行。</h3><br>

    ./connectnkrun.sh
        
    
如果运行了后台后，无法连接到screen的窗口，可能是screen的参数运行参数有变动。进入到脚本修改即可。
