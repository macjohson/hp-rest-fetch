##restful api fetch请求
####工具特点
1. 错误统一处理，并对服务器及网络错误进行处理
2. 支持loading
3. 支持async await

####使用说明
    import restFetch from 'hp-rest-fetch'
      
    const testFetch = async ()=>{
       
        try{
        const result = await restFetch({
               //请求接口
              api:"/api/test",
              
              //请求方式
              method:"PUT",
              
              //请求参数
              opts:{param1:"123"},
              
              //loading状态处理
              loading:bool => {
              
              }
           })
           //处理返回数据
        }catch(e){
            //处理错误信息
        }
    } 
    
###参数说明
>api string 请求接口

>method string 请求方式，默认为`GET`，非必填

>opts Object 请求参数，非必填

>loading fun 处理，回调函数 (boolean)=>{}，非必填

>body boolean 请求参数是否在body中,默认为false,非必填

