# Mobile-Web-learning-records

## 5. rem，less

### 5.1rem

1.rem是一个相对于根元素字体的大小的单位。1rem=1HTML的字号大小

2.应用场景;**使一个盒子的大小在不同分辨率下等比例缩放**

3.目前rem布局方案中，将网页等分成10份， HTML标签的字号为视口宽度的 1/10

4.在视口为375px的设备中设置一个宽度68px的盒子rem单位尺寸的确定

+ 确定设计稿中对应设备的HTML标签字号
+ N*37.5=68——N=68/37.5
+ `rem单位的尺寸=px单位数值/基准字号（1/10视口宽度`

写法：

```    css
        html {
            font-size: 14px;
        }
        
        .box {
            width: 10rem;
            height: 5rem;
            background-color: pink;
        }

```



### 5.2媒体查询

应用场景：视口不同，添加不同的根字号

+ 媒体查询能够检测视口宽度，然后编写差异化的css样式
+ 当条件成立时，执行对应的css样式

写法：

``` @media (媒体特性){选择器{css属性}}```

```css
        @media (width:1920px) {
            body {
                font-size: 200px;
                color: teal;
            }
        }
//当视口的宽度为1920px时 body里面的字体大小为200px，颜色为teal
```

### 5.3 flexible

使用flexible js配合rem实现在不同宽度的设备中，网页元素尺寸等比缩放效果

`<script src="../js/flexible.js"></script>`

+  flexible.js是手淘开发出的一个用来适配移动端的js框架.
+ 核心原理就是根据不同的视口宽度给网页中html根节点设置不同的font-size。

### 5.4 less

section标签中的h标题标签会自动降一级
