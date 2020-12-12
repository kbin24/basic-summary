### CSS背景图片

#### background-image属性 设置背景图片

``` css
div {
    width: 300px;
    height: 300px;
    border: 1px solid gray;
    background-image: url(image/logo.png);
    /*背景图片默认平铺*/
}
```

![1](image/默认背景图片.png)

<hr>    

#### background-repeat属性 设置背景图片平铺情况

* no-repeat 背景图片不平铺
* repeat-x 背景图片沿X轴平铺
* repeat-y 背景图片沿Y轴平铺

<hr >   
背景图片不平铺  

``` css
 div {
     width: 300px;
     height: 300px;
     border: 1px solid gray;
     background-image: url(image/logo.png);
     background-repeat: no-repeat;
 }
```

![1](image/no-repeat.png)

<hr>
背景图片沿X轴平铺       

``` css
 div {
     width: 300px;
     height: 300px;
     border: 1px solid gray;
     background-image: url(image/logo.png);
     background-repeat: repeat-x;
 }
```

![1](image/repeat-x.png)

<hr>
背景图片沿Y轴平铺       

``` css
 div {
     width: 300px;
     height: 300px;
     border: 1px solid gray;
     background-image: url(image/logo.png);
     background-repeat: repeat-y;
 }
```

![1](image/repeat-y.png)

<hr>

#### background-position 属性 设置背景图片的位置

background-position: x y; X和Y可以是精确单位，也可以是top，right，bottom，left。这些名词单位

``` css
/*设置背景图片水平靠右下角显示*/
div {
    width: 300px;
    height: 300px;
    border: 1px solid gray;
    background-image: url(image/logo.png);
    background-repeat: no-repeat;
    background-position: right bottom;
}
```

![1](image/position.png)

<hr>    
使用精确单位设置背景图片的位置  

``` css
 div {
     width: 300px;
     height: 300px;
     border: 1px solid gray;
     background-image: url(image/logo.png);
     background-repeat: no-repeat;
     /*背景图片距离X轴50px 距离Y轴100px*/
     background-position: 50px 100px;
 }
```

<hr>

#### background-attachment 属性 设置背景是否固定

* scroll 背景图片随着页面的滚动而滚动，这是默认的
* fixed 背景图片不会随着页面的滚动而滚动

<hr>

#### 背景色半透明

``` css
div {
    /*取值为0-1 0为透明 1不透明*/
    background: rgba(0, 0, 0, 0.3)
}
```

<hr>  

#### 精灵图的使用

精灵图的使用就是为了有效减少服务器接收和发送请求的次数，提高页面的加载速度 

使用精灵图核心总结： 

1. 精灵图主要针对小的背景图片使用
2. 主要借助于背景位置来实现--background-position
3. 一般情况下精灵图都是负值。（千万注意网页中的坐标：X轴右边走是正值，左边走是负值，y轴同理）

``` css
.box {
    width: 30px;
    height: 30px;
    background: url(image/sprite.png) no-repeat -30px 0;
    margin: 100px auto;
}
```
```html
<div class="box"></div>
```
![1](image/sprite.png) <br>
![1](image/精灵图使用.png)
