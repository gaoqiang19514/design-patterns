# 单例模式

总结下来就是一个要点
> 用一个变量判断这个目标是否已经创建过一次，如果是，直接返回目标的缓存，否则就创建这个目标

````
viewLoginView = (function(){
    var singleton;

    return function(func){
        if(!singleton){
            return singleton || (singleton = func.apply(this, arguments));
        }

        return singleton; 
    }
})();
````

[![简书](http://cdn2.jianshu.io/assets/web/logo-58fd04f6f0de908401aa561cda6a0688.png  "测试一下")](http://www.jianshu.com/p/1e402922ee32/)
