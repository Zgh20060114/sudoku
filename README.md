# sudoku
C++ 实现的跨平台数独游戏和扫雷游戏（fork了大佬的数独游戏，然后使用相同的代码风和操作界面，添加了扫雷玩法），命令行操作易上手，可以在开发间隙用来放松身心。数百行代码，初学者也可以轻松掌握。
欢迎通过pull request的方式来添加功能或修复缺陷。

## 感谢贡献者
<a href="https://github.com/mayerui/sudoku/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=mayerui/sudoku" />
</a>

## 特性
1. 跨平台/编译器 : Linux/Windows/macOS [![Linux](https://github.com/mayerui/sudoku/actions/workflows/ci-linux.yml/badge.svg)](https://github.com/mayerui/sudoku/actions/workflows/ci-linux.yml) [![Windows](https://github.com/mayerui/sudoku/actions/workflows/ci-windows.yml/badge.svg)](https://github.com/mayerui/sudoku/actions/workflows/ci-windows.yml) [![macOS](https://github.com/mayerui/sudoku/actions/workflows/ci-macos.yml/badge.svg)](https://github.com/mayerui/sudoku/actions/workflows/ci-macos.yml)
2. 多语言：English/中文
3. 无第三方库依赖
4. 控制台运行

## 依赖
1. cmake 3.12及以上
2. C++17

## 构建
``` shell
cmake -B build -S .
cmake --build build
```

## 运行
构建步骤生成的 `sudoku` 可执行文件在 `bin` 目录下
``` shell
./sudoku  # 直接启动
./sudoku -l filename  # 读取游戏进度文件
./sudoku -h  # 获取帮助信息
```

## 操作说明
- 0 删除已填入数字
- u 撤销上一步操作
- enter 尝试通关
- esc 退出游戏

### 普通模式
- w 光标上移↑
- a 光标左移←
- s 光标下移↓
- d 光标右移→

### VIM模式
- k 光标上移↑
- h 光标左移←
- j 光标下移↓
- l 光标右移→

## 项目结构
```bash
│--.gitignore  
│--build.bat        // Windows 一键编译脚本  
│--build.sh         // Linux/macOS 一键编译脚本  
│--CMakeLists.txt   // CMake 项目文件  
│--README.md     
└--src              // 源代码目录  
   │--block.cpp     // 数独格子组合类，可代表行、列、九宫格  
   │--block.h  
   │--color.h       // 颜色类  
   │--command.cpp   // 命令类，实现了撤销功能  
   │--command.h     
   │--common.h      // 公共头文件  
   │--input.cpp     // 输入类  
   │--input.h   
   │--main.cpp      // 入口文件  
   │--scene.cpp     // 游戏场景类  
   │--scene.h   
   │--test.cpp      // 测试文件  
   │--test.h  
   └--utility.inl   // 一些实用的全局函数  
```
