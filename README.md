# 几种C++调用C# DLL的方法例子  

## 1. C#通过导出函数由C++用LoadLibrary加载dll.  

## 2. Clr引入C# DLL后直接调用.  

## 3. c++通过CLR托管接口从内存中加载.NET程序集.   

具体代码看源码。
这里强烈推荐第三种方法，你可以将DLL转成字节数组变成C++的一个变量，这样就不用落地直接调用。至于安全方面，可以将dll的数组分段切割或者将dll的数组加密后再放进去，调用时重新拼成正常PE或者解密dll数组后再调用。或者直接在将C++宿主混淆加密加壳等。  
