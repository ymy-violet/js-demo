###jsץȡ��ҳ�з�������
  ���ݲ�Ʒ��һ������ǰ����jsץȡ��������ҳ�����з�������

#### �����
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
     //ȥ������ո�ͻ��з�
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
> ������ https://b2b.baidu.com/ �����վ��ҳmenuΪ����һ�����н��

>![QQͼƬ20200325172414.png](https://i.loli.net/2020/03/25/wdKpnTGY8qar6A4.png)

-------------------

> ��ͼ�����н�� ��

> ![QQͼƬ20200325172948.png](https://i.loli.net/2020/03/25/Zb2UeHvz3t589mu.png)
