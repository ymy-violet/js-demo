### js抓取网页中分类内容
  根据产品的一个需求，前端用js抓取第三方网页的所有分类内容

#### 代码块
``` javascript
function GrabDate(){
     const FirstMenu = document.getElementById("menu");
     const FirstTxt = FirstMenu.getElementsByTagName("a");
     const SecMenu = document.getElementById("sub-menu");
     const SecTxt = SecMenu.getElementsByTagName("a");
     let arrList = [];
     let resultStr = [];

      for(let i = 0 ; i < FirstTxt.length ; i++){        
          let val = FirstTxt[i].text;
          arrList.push(val);         
      }
	
     for(let j = 0 ; j < SecTxt.length ; j++){
         let val = SecTxt[j].text;
         arrList.push(val);

     }
     //去除数组空格和换行符
     arrList.forEach(function (value) {
           value = value.replace(/\s+/g,'');
           value = value.replace(/[\r\n]/g,"");
           resultStr.push(value);
           //console.log(value);
         })
     console.log(resultStr);
 }
 GrabDate()
```
-------------------
> 我们以 https://b2b.baidu.com/ 这个网站首页menu为例看一下运行结果

>![QQ图片20200325172414.png](https://i.loli.net/2020/03/25/wdKpnTGY8qar6A4.png)

-------------------

> 下图是运行结果 ：
 
> ![QQ图片20200325172948.png](https://i.loli.net/2020/03/25/Zb2UeHvz3t589mu.png)
