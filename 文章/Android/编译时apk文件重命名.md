
# 编译时apk文件重命名

在app目录下的build.gradle文件中增加如下配置：

示例1：
```
android {

    ...

    applicationVariants.all { variant ->
        variant.outputs.all {
            def fileName = "xxxx-" + versionName + "-xxxx.apk"
            outputFileName = fileName
        }
    }

}
```

示例2：
```
android {

    ...

    applicationVariants.all { variant ->
        variant.outputs.all {
            def fileName = variant.flavorName + "-Android-" + versionName + "-xxxxx.apk"
            outputFileName = fileName
        }
    }

}
```

示例3：
```
android {

    ...

    applicationVariants.all { variant ->
        variant.outputs.all {
            def fileName = variant.flavorName + "-Android-" + versionName.replace("ABC", "def") + ".apk"
            outputFileName = fileName
        }
    }

}
```
