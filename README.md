# bootloader
Module Dependency Loader with bundlify

##define

```
define({
  module : "my.module",
  extend : "my.parent",
  using : ["mod1","mod2","mod3"]
}).as(function(MyModule,mod1,mod2,mod3){
  
  return {
    _define_ : function(){
    },
    _instance_ : function(){
    },
    _extended_ : function(){
    },
    _ready_ : function(){
    
    }
  };
  
})
```
##module
```
module(["module1","module2"], function(module1,module2){
  
});
```

##importStyle 
Import StyleSheets packages recursively as mentioned in module.json

```
__importStyle__("style/package/name");
```

##Hooks

```
bootloader.onmodulenotfound =  function(moduleName, callback){
  //this is fallback for module not found 
};

bootloader.module404 =  function(moduleName){
  //finally raise alert when module not found
};

```
