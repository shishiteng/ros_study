参考：
http://wiki.ros.org/pluginlib/Tutorials/Writing%20and%20Using%20a%20Simple%20Plugin

1.Getting ready
  $ catkin_create_pkg pluginlib_tutorials_ roscpp pluginlib

2.Create a Base Class
  include/pluginlib_tutorials_/polygon_base.h

3.Create the Plugins
  include/pluginlib_tutorials_/polygon_plugins.h

4.Registering the Plugins
  src/polygon_plugins.cpp

5.Building the Plugin Library
  CMakeLists.txt

6.Making the Plugins Available to the ROS Toolchain
1)The Plugin XML File
  polygon_plugins.xml
2)Exporting Plugins
  package.xml

经过以上步骤，plugin就算是建立成功了，可用以下命令验证：
  rospack plugins --attrib=plugin pluginlib_tutorials_

7.Using a Plugin
  src/polygon_loader.cpp

8.Building the Plugin exe
  CMakeLists.txt

9.Run
  ./devel/lib/pluginlib_tutorials_/polygon_loader
