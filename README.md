# offer

// 04 js题目：实现一个方法，把数组里所有到值加和。即SUM(1,2,3)=6
var arr = [1,2,3]
function sum(arr) {
  var s = 0;
  for (var i=arr.length-1; i>=0; i--) {
    s += arr[i];
  }
  return s;
}

// 05 实现一个js方法appendParams，可以给url加上多个新的参数，多考虑兼容性。
var appendParams('http://url', {a:1,b:2})返回http://url?a=1&b=2。
function appendParams(url,data) {
 if(data.length) {
  return data
 }  else {}
}

// 06 js题目：给一个时间戳，计算出这个时间戳对应当月的最后一天最后一秒的时间戳。
function times(time) {
  var date = new Date(time * 1000);
  var Y = date.getFullYear() + '-';
  var M = (date.getMonth()+1 < 10 ? '0'+(date.getMonth()+1) : date.getMonth()+1) + '-';
  var D = date.getDate() + ' ';
  var h = date.getHours() + ':';
  var m = date.getMinutes() + ':';
  var s = date.getSeconds();
  return Y+M+D+h+m+s;
}
    
// 07 js题目：实现一个js方法，判断两个对象是否一样。（请在输入框填写答案git链接）
function isEqual(a, b) {   
  var aProps = Object.getOwnPropertyNames(a);
  var bProps = Object.getOwnPropertyNames(b); 
  if (aProps.length != bProps.length) { 
   return false;
  }
  for (var i = 0; i < aProps.length; i++) {
    var propName = aProps[i];
    if (a[propName] !== b[propName]) {
      return false;
    }
   }
   return true;
 }

// 08 js题目：实现一个方法求输出字符串的所有唯一字符（即去掉重复）。比如：输入"abbcdcefgh"输出"abcdefgh"。
function removeRepeatStr(str){
  var newStr = '';
  var len = str.length;
  for(var i=0; i<len; i++){
    if(newStr.indexOf(str[i])==-1){
      newStr = newStr + str[i];
    }
  }
  return newStr;
}

// 09 js题目：请使用闭包的方式，写一段JS程序实现如下功能：函数每调用一次则该函数的返回值加1（注：要求使用ES6箭头函数实现）
var foo = () => {
  var num = 0
  return num+1
}





