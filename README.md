# with
js中的with 语句

## 说明
with语句是对象的快捷应用方式，用来避免书写重复代码。可以方便地用来引用某个特定对象中已有的属性，但是不能用来给对象添加属性。要给对象创建新的属性，必须明确地引用该对象。  
## 格式 
with(object instance) 
{  
        //coding
}  
       有时候，我在一个程序代码中，多次需要使用某对象的属性或方法，照以前的写法，都是通过:对象.属性或者对象.方法这样的方式来分别获得该对象的属性和方法，着实有点麻烦，学习了with语句后，可以通过类似如下的方式来实现：  
with(objInstance)  
{  
       var str = 属性1;  
        .....  
} 去除了多次写对象名的麻烦。  
## 举例  
```
<script language="javascript">  ·
<!--  
function Lakers() {  
       this.name = "kobe bryant";  
       this.age = "28";  
       this.gender = "boy";  
}  
var people=new Lakers();  
with(people)  
{  
       var str = "姓名: " + name + "<br>";  
       str += "年龄：" + age + "<br>";  
       str += "性别：" + gender;  
       document.write(str);  
}  
//-->  
</script>  
```
代码执行效果如下:  
```
姓名: kobe bryant  
年龄：28  
性别：boy 
```
#### 提示：with 语句是运行缓慢的代码块，尤其是在已设置了属性值时。大多数情况下，如果可能，最好避免使用它。
