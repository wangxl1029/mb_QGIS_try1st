mb_QGIS_try1st
==============
Compile and probe QGIS for the first try.

INDEX
-----
[TOC]

### Overview

### 填坑日志
:sunny: 2018-6-18 端午节，周一


> Error	721	error LNK1112: module machine type 'x64' conflicts with target machine type 'X86'	D:\Documents\Downloads\QGIS-final-2_18_20\build\src\core\spatialindex-64.lib(spatialindex-64.dll)	qgis_core


:umbrella: 2018-6-17 周日 :smile:

我们本地的<https://github.com/wangxl1029/QGIS_final-2.18.20>是:fork_and_knife:fork自
https://github.com/qgis/QGIS/tree/final-2_18_20

:cry:更早的坑
+ 第一个要编译的工程是qgis_core
  - 编译的Configure一定要选`RelWithDebugInfo`，不要用默认的`Debug`的Configure，否则有606个链接错误。这坑爬了两三天，有木有:confounded:。
  - 请在预编译定义里加`Q_WS_WIN`，否则编译会使用Linux下的Socket接口。
