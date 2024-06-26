计算机硬件课设：使用IIC协议实现Max30205.（语言为Verilog）
Max30205用于获取环境或人体温度，提供读写功能，本课设所实现的IIC协议只提供最基本的读取温度功能。
所有文件均在zip文件中，压缩后在文件夹下找到   max30205531.xpr 文件，使用Vivado打开即可实现硬件部分。
重要的代码在额外的txt文件中标注，软件部分（使用Xilinx SDK）代码也在里面。
<font color = red>各txt中代码情况如下：</font>
design5_26_wrapper.txt 中为封装IP后的模块部分
design5_26_i-init.txt 中为封装IP后的模块具体实现部分
IIC_ctrl.txt 中为IIC的实现代码（**注意：这个IIC只适用于Max30205硬件，各种硬件的IIC实现起来有差别，套在其他硬件上大概率行不通（时序、从机地址、读取的寄存器地址均有差别）**）
IIC_sim.txt 中为IIC的仿真代码

上面四个代码均在Vidado中编译

PrintMax30205.txt为软件部分，实现将温度打印到电脑屏幕上，需要使用XilinxSDK编译，注意要把代码里面 XPAR_MAX30205539L_0_S00_AXI_BASEADDR 更换为实际的元器件寄存器地址（"xparameters.h"头文件中有） 
