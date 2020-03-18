# jiuyuntu
这是一个用于九云图API的node.js版本的SDK
# 安装
 npm install jiuyuntu
 
# 使用方法
 # 认证秘钥根据实际使用平台填写
var { Convert } = require('jiuyuntu');

var convert = new Convert({

appCode:'xxxx', //阿里云认证code

yuntuKey:'xxxx',//九云图自营平台认证key

appKey:'xxx',

appSecret:'xxx'// 华为云认证 appkey与appSecret

});


convert.convertLocalFile("local-file", { outputType: "" })
.then(res => {

    if(res&&res.retCode==0）{ 
    
    convert.getOutputResult().then(outputURLs=>{
    
             console.log(outputURLs)
    })
    }
})

convert.convertUrl("docurl", { outputType: "" }) 
 .then(res => {
 
    if(res&&res.retCode==0）{
    
    convert.getOutputResult().then(outputURLs=>{
    
             console.log(outputURLs)
    }) 
    }
})

 # outputType 可选参数有 webview pdf longimage svgs 详细说明可查看九云图使用说明
 # outputURLs 为最后获取的结果是一个长度大于0的数组
