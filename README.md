# TypeScript
对TypeScript的学习及应用在React Native中...
官网地址：https://www.tslang.cn/docs/handbook/basic-types.html

## 9.17 基础类型,变量声明，接口
### 布尔值（boolean）, 数字（number）:支持二进制、八进制、十进制、十六进制，字符串（string）,数组（array），元组（Tuple），枚举（enum）,Any（any）,Void(当函数没有返回值时)，Null和Undefined，Never
   
```
let name:string = "Monica";   //字符串

let list:number[] = [1,2,3];   //数组

let list2:Array<number> = [2,3,4];  //数组

let x:[string, number];    //元组（第一个为字符串，第二个数字）

enum Color {Red = 1, Green, Blue}  //枚举
let c: Color = Color.Green;   

let someValue: any = "this is a string";

let strLength: number = (<string>someValue).length;

let strLength: number = (someValue as string).length;



```
### substr 和substring的区别：

  * 相同：只写一个参数的时候，substr和substring都是从截取字符串开始下标到结尾的字符串；
  
  * 不同：第一个参数都是代表截取字符串开始的下标，第二个参数substr是代表截取的长度/substring是代表截取字符串结束的下标
   
```
"Hello World!".substr(3,7)   //lo Worl
"Hello World!".substring(3,7)   //lo Wo
```
### 接口：可选属性和只读属性
* 带有可选属性的接口与普通的接口定义差不多，只是在可选属性名字定义的后面加一个?符号。
* 可选属性的好处之一是可以对可能存在的属性进行预定义，好处之二是可以捕获引用了不存在的属性时的错误。
```
interface SquareConfig {
  color?: string;
  width?: number;
}
```
* 只读属性
```
interface Point {
    readonly x: number;
    readonly y: number;
}
let ro: ReadonlyArray<number> = a;
let mySquare = createSquare({ width: 100, opacity: 0.5 } as SquareConfig);
```
* readOnly 和 const区别
  最简单判断该用readonly还是const的方法是看要把它做为变量使用还是做为一个属性。 做为变量使用的话用 const，若做为属性则使用readonly。

* search方法： 查找字符串中的子字符串的下标
```
var str="Visit Runoob!"; 
var n=str.search("Runoob"); //6
所以若存在子字符串，n>-1; 否则n=-1

```

  
  
