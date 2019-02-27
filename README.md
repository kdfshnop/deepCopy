# 深拷贝
```
1. function deepCopy(obj){
        let result = Array.isArray(obj)?[]:{};  
        if(obj && typeof obj === 'object'){ 
            for(let key in obj){
                if(obj.hasOwnProperty(key)){
                    if(obj[key]&&typeof obj[key]==='object'){
                        result[key]=deepCopy(obj[key]);
                    }else{
                        result[key]=obj[key];
                    }
                }
            }
        }
        return result;
    };
  2. JSON.parse(JSON.stringfy(obj));
```