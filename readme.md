##  0.readme
- Ubuntu16.04
- cuda10.1

能够成功能编译,但是运行不了，显存不够。如果要运行需要更改CMakeLists.txt文件.
[!Alt](./doc/test.png)


This is the bundlefusion of linux version, exactly the ubuntu version. I have tested in Ubuntu16.04 + CUDA9.0 and Ubuntu 18.04 + CUDA10. I think other version is OK, maybe you should change some compile configuration!
The project archeticture:

BundleFusion_Ubuntu_V0 has the following folders and a CMakeLists.txt and two parameter configuration files:
cmake_modules
data
- [external](https://github.com/niessner/mLib/tree/ac6b9e9d1da1df00a2293da64a9f146c123fa2ca)这个有修改
FriedLiver
lib
mLibExternal
modules
scans
build
CMakeLists.txt
zParametersBundlingDefault.txt
zParametersDefault.txt
The data,lib,mLibExternal,scans you must make them yourself!
"data" folder, you put the dataset for example:sequence.sens, you can download it from the https://github.com/niessner/BundleFusion.
"lib" is empty folder just used in compilation.
- [data download](http://graphics.stanford.edu/projects/bundlefusion/)注意是下载**.sens数据集
- [mLibExternal download](http://kaldir.vc.in.tum.de/mLib/mLibExternal.zip)要做更改！
 "mLibExternal" folder you must add the files from the bundlefusion in https://github.com/niessner/BundleFusion.
"scans" folder is the mesh output! the results you are looking forward to!
##  1.make and compile
cd build
cmake ..
make -j8
now you just put the "zParametersBundlingDefault.txt" and "zParametersDefault.txt"  into build folder and just 
`./FriedLiver`
the Bundlefuson_Ubuntu is running and press "9" key you can save the mesh!

For now, no display, when I have time, I will add display, I will use imGUI and OpenGL to display and render!
If anyone have any problem you can send me a email:deansaint@126.com or qq:3171410 or join my wechat for VIO
I also R&D VIO slam!
I hope all of you will benefit from my porting project--BundleFusion_Ubuntu!
Guan Shi yuan
关士远
2019.11.26
