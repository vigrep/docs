
# Android项目重命名

## 更改项目文件夹名称
1. 关闭Android Studio 
2. 重命名项目文件夹名称 (OldName -> NewName)
3. 用Android Studio打开修改后的项目
4. 修改根目录下的 `settings.gradle` 修改 `rootProject.name` 为新项目名称，点击Sync Now即可(.idea下的.iml就会变成新项目名称.iml)

最后可执行：clean project 清理一下项目

## 更改包名

选中包名，右键->Refactor->Rename...->Rename package->输入新包名，点击Refactor->确认修改影响范围，确认无误后点击Do Refactor即可

涉及：
1. 目录/包名
2. 代码中包声明
3. 代码中xml中的包名引用
4. 代码中import
5. `AndroidManifest.xml` 中的包名

最后可执行：clean project 清理一下项目

## 更改applicationId

在 `build.gradle` 中修改 `applicationId`

## 更改应用名称

在 `strings.xml` 中修改 `app_name`

## 最后清理

1. 全局搜索`OldName` 修改为 `NewName`
2. clean project
3. rebuild project
