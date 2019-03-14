---
title: Unity小技巧
date: 2019-03-14 21:39:22
tags: [Unity, Tips]
categories: Unity
---
<!-- toc -->

# Unity小技巧
<!--More-->
## 安卓手机连接Unity Profiler
>adb forward tcp:54999 localabstract:Unity-com.tencent.tmgp.ztj

## 文件默认打开方式
```C#
#if UNITY_EDITOR
using System.Collections;
using System.Collections.Generic;
using UnityEditor;
using UnityEditor.Callbacks;
using UnityEngine;

public class OpenFileEx {

    [OnOpenAsset]
	public static bool OpenShaderAsset(int instanceID, int line)
    {
        if (EditorUtility.InstanceIDToObject(instanceID) is Shader)
        {
            string assetPath = AssetDatabase.GetAssetPath(instanceID);
            System.Diagnostics.Process.Start(Application.dataPath + "/../" + assetPath);
            return true;
        }
        return false;
    }
}
#endif
```

## 脚本生命周期
![Unity脚本生命周期](http://ww1.sinaimg.cn/large/006Q2Ktwly1g12npt63m5j30sl13yad2.jpg)