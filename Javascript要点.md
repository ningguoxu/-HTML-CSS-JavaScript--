# JavaScript要点
**变量**
- 
 - `var 变量名;` 声明一个变量
 - `var = 1;` 给var这个变量赋值为1
 ```
 var age;
 age = 15;
 ```
 - 输出变量到控制台 : `console.log(变量名);`
    - 输出多个变量
        ```
        console.log(age, my)
        ```
 - 变量的初始化:
 ```
 var age = 15 //声明变量并赋值为15
 ```
 - `prompt`:
    - prompt在JavaScript是一个方法,用于显示一个对话框,让用户输入一些信息
        ```
        var 变量名 = prompt('请输入: ')
        ```
- `alert`:
    - `alert`用于在浏览器中弹出一个带有消息和确定按钮的警告框.`alert`这个方法的特点是它会阻塞当前窗口的执行，直到用户点击确定按钮才会继续执行后面的代码
        ```
        alert("Hello, world!"); // 弹出一个警告框，显示"Hello, world!"这句话
        ```