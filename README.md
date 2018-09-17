# TypeScript
对TypeScript的学习及应用在React Native中...

## 9.17 基础类型
* 布尔值（boolean）, 数字（number）:支持二进制、八进制、十进制、十六进制，字符串（string）,数组（array），元组（Tuple），枚举（enum）,Any（any）,Void(当函数没有返回值时)，Null和Undefined，Never
   
```
let name:string = "Monica";   //字符串

let list:number[] = [1,2,3];   //数组

let list2:Array<number> = [2,3,4];  //数组

let x:[string, number];    //元组（第一个为字符串，第二个数字）

enum Color {Red = 1, Green, Blue}  //枚举
let c: Color = Color.Green;   


```
* substr 和substring的区别：

  相同：只写一个参数的时候，substr和substring都是从截取字符串开始下标到结尾的字符串；
  
  不同：第一个参数都是代表截取字符串开始的下标，第二个参数substr是代表截取的长度/substring是代表截取字符串结束的下标
   
```
"Hello World!".substr(3,7)   //lo Worl
"Hello World!".substring(3,7)   //lo Wo
```
