
# 读取local.properties中的配置

```
Properties properties = new Properties()
File propertyFile = new File(rootDir.getAbsolutePath() + "/local.properties")
properties.load(propertyFile.newDataInputStream())

gradle.ext.testString = properties.getProperty('test_string')
gradle.ext.testBool = Boolean.parseBoolean(properties.getProperty('test_bool'))
gradle.ext.testInt = Integer.parseInt(properties.getProperty('test_int'))
gradle.ext.testFloat = Float.parseFloat(properties.getProperty('test_float'))
gradle.ext.testDouble = Double.parseDouble(properties.getProperty('test_double'))
```
