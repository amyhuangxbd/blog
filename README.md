# blog
## 1. 数组扁平化处理：实现一个flatten方法，使得输入一个数组，该数组里面的元素也可以是数组，该方法会输出一个扁平化的数组。
>
    // Example
    let givenArr = [[1, 2, 2], [3, 4, 5, 5], [6, 7, 8, 9, [11, 12, [12, 13, [14]]]], 10];
    let outputArr = [1,2,2,3,4,5,5,6,7,8,9,11,12,12,13,14,10]
    
    // 实现 flatten 方法使得
    flatten(givenArr)-->outputArr
递归实现
    
    function flatten(arr){
      var res = [];
      for(var i=0;i<arr.length;i++) {
        if (Array.isArray(arr[i])) {
          res = res.concat(flatten(arr[i]));
        }else{
          res.push(arr[i])
        }
      }
      return res;
    }
    
    function flatten(arr){
        return arr.reduce(function(prev,item){
            return prev.concat(Array.isArray(item)?flatten(item):item);
        },[]);
    }
  ES6拓展运算符
    
    function flatten(arr){
        while(arr.some(item=>Array.isArray(item)){
            arr = [].concat(...arr);
        }
        return arr;
    }

## 2. react 加载img 出错 使用onError事件处理。
    <img src={v.CoverUrl} onError={(e) => { e.target.onerror = null;e.target.src=require('../../../public/assets/images/course-center-detail.gif'); }} />
    
## 3. [如何用 css 或 js 实现多行文本溢出省略效果，考虑兼容性](https://github.com/Advanced-Frontend/Daily-Interview-Question/issues/246)
    [codepen 1](https://codepen.io/prettyworld/pen/GRKrMMP)
    [codepen 2](https://codepen.io/wrenchde/pen/ExYgbyM)
