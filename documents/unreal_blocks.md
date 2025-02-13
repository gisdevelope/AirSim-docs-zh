# 配置Blocks环境

Blocks environment is available in repo in folder `Unreal/Environments/Blocks` and is designed to be lightweight in size. That means its very basic but fast.

Here are quick steps to get Blocks environment up and running:

## Windows

1. Make sure you have [installed Unreal and built AirSim](build_windows.md).
2. Navigate to folder `AirSim\Unreal\Environments\Blocks` and run `update_from_git.bat`.
3. Double click on generated .sln file to open in Visual Studio 2017 or newer.
4. Make sure `Blocks` project is the startup project, build configuration is set to `DebugGame_Editor` and `Win64`. Hit F5 to run.
5. Press the Play button in Unreal Editor and you will see something like in below video. Also see [how to use AirSim](https://github.com/Microsoft/AirSim/#how-to-use-it).

### 修改代码以及重建（rebuild）

For Windows, you can just change the code in Visual Studio, press F5 and re-run. There are few batch files available in folder `AirSim\Unreal\Environments\Blocks` that lets you sync code, clean etc.

## Linux
1. Make sure you have [built the Unreal Engine and AirSim](build_linux.md).
2. Navigate to your UnrealEngine repo folder and run `Engine/Binaries/Linux/UE4Editor` which will start Unreal Editor.
3. On first start you might not see any projects in UE4 editor. Click on Projects tab, Browse button and then navigate to `AirSim/Unreal/Environments/Blocks/Blocks.uproject`. 
4. If you get prompted for incompatible version and conversion, select In-place conversion which is usually under "More" options. If you get prompted for missing modules, make sure to select No so you don't exit. 
5. Finally, when prompted with building AirSim, select Yes. Now it might take a while so go get some coffee :).
6. Press the Play button in Unreal Editor and you will see something like in below video. Also see [how to use AirSim](/#how-to-use-it).

[![Blocks Demo Video](images/blocks_video.png)](https://www.youtube.com/watch?v=-r_QGaxMT4A)

### 修改代码以及重建（rebuild）

For Linux, make code changes in AirLib or Unreal/Plugins folder and then run `./build.sh` to rebuild. This step also copies the build output to Blocks sample project. You can then follow above steps again to re-run.

## 选择模式：汽车或无人机

By default AirSim spawns multirotor. You can easily change this to car and use all of AirSim goodies. Please see [using car](using_car.md) guide.

## FAQ
#### 提示诸如 "_BuitData" 的文件不存在。

这些只是过渡文件，可以无视。
