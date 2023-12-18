# CMakeTemplate
A CMake Template for microproject by Hamster King

CMake个人模板，适合cpp的微型项目，局限性很大，后面会继续完善（如果仓鼠还记得的话..）

## 使用说明

### 文件目录

- `./include`:头文件目录
- `./src`:源文件目录
- `./build`:CMake项目

### 项目编译+运行

Windows的CMake默认用的编译器是MSVC（VS2022）

```bash
cmake -B build
```

生成出来的没有Makefile文件，用的VS那一套

如果想用$gcc$编译器请使用以下指令(推荐)

```bash
cmake -B build "MinGW Makefiles"
```

会生成Makefile，注意千万不要改Makefile文件！！

然后生成二进制可执行文件

```
cmake --build build
```

执行完这条命令连接成功后会提示exe文件目录，各个编译器生成的exe文件目录可能不一致

Linux默认编译器一般就是gcc了，直接使用上述命令就好
