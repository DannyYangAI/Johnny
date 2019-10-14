安裝 ubuntu librealsense SDK

https://github.com/IntelRealSense/librealsense/blob/master/doc/distribution_linux.md

https://www.itread01.com/content/1547455861.html


安裝完 ， 執行  realsense-viewer   ， 確認是否成功


安裝cmake
https://blog.csdn.net/lj402159806/article/details/76408597

安裝完 ， 執行  cmake --version， 確認是否成功

安装glfw3

sudo apt-get install libglfw3-dev


執行paper 的 Setting Up Camera System

https://github.com/andyzeng/visual-pushing-grasping


＊更新程式 ，(原始程式 ，在執行 cmake 編譯會錯誤 ， )

![image](https://github.com/jhnny009/Johnny/blob/patch-1/57359913-78b53a80-71ab-11e9-86c3-65c6b421d293.png)

https://github.com/andyzeng/visual-pushing-grasping/issues/19

realsense底下的 realsense.cpp  ，208行，

      //rs2::frame depth_colorized = color_map(aligned_depth);  原本的
     rs2::frame depth_colorized = aligned_depth.apply_filter(color_map);   //修改後的
        
