# HarmonicVirtualLights

这是一个使用C++和Vulkan图形API开发的项目，实现了谐波虚拟光照效果。

## 在VSCode下编译项目

### 前提条件

1. 安装Visual Studio 2022（或2019）并选择"C++桌面开发"工作负载
2. 安装Vulkan SDK，并确保环境变量`VULKAN_SDK`已设置
3. 安装GLFW库
4. 安装GLM数学库
5. 安装ImGui库
6. 安装glslangValidator工具（通常随Vulkan SDK一起安装）

### VSCode扩展安装

在VSCode中安装以下扩展：
- C/C++扩展包 (Microsoft)
- C++ Intellisense扩展

### 编译项目

1. 在VSCode中打开项目文件夹
2. 按下`Ctrl+Shift+B`执行默认构建任务（Debug配置）
3. 或者，通过命令面板（`Ctrl+Shift+P`）选择"Tasks: Run Task"，然后选择"Build Debug"或"Build Release"

### 调试项目

1. 按下`F5`启动调试（默认为Debug配置）
2. 或者，通过调试面板选择"Debug HarmonicVirtualLights"或"Release HarmonicVirtualLights"配置

### 编译着色器

项目中的GLSL着色器需要编译为SPIR-V格式。您可以：

1. 右键单击着色器文件（.vert, .frag, .comp等），然后选择"Compile Shaders"任务
2. 或者，通过命令面板（`Ctrl+Shift+P`）选择"Tasks: Run Task"，然后选择"Compile Shaders"

### 清理项目

通过命令面板（`Ctrl+Shift+P`）选择"Tasks: Run Task"，然后选择"Clean"

## 项目结构

- `Engine/` - 核心引擎代码
  - `Application/` - 应用程序相关代码（输入、窗口、场景管理等）
  - `Graphics/` - 图形渲染相关代码（Vulkan封装、渲染器、相机等）
  - `Dev/` - 开发辅助工具（日志、字符串处理等）
- `Scenes/` - 场景定义
- `Resources/` - 资源文件（着色器、纹理、模型等）
- `Linking/` - 外部库和头文件

## 注意事项

1. 确保Vulkan SDK已正确安装并配置环境变量
2. 确保所有依赖库（GLFW、GLM、ImGui）的路径正确
3. 项目使用预编译头文件(pch.h)，确保在添加新文件时包含它
