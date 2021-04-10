> 利用border调节盒子的大小

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div {
            width: 140px;
            height: 70px;
            border-width: 2px 2px 72px 2px;
            background-color: pink;
            border-style: solid;
            border-color: black;
            margin: 100px auto;
        }
    </style>
</head>

<body>
    <div>这里是盒子content</div>
</body>

</html>
```

<img src="C:\Users\a\AppData\Roaming\Typora\typora-user-images\image-20210410125628276.png" alt="image-20210410125628276"  />



> 在使用border-radius(圆角边框)时，无论是content-box还是border-box盒模型下，都是作用于包括边框大小在内的盒子区域

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div {
            width: 300px;
            <!-- height设置为300px，border-box盒模型 -->
            height: 300px;
            background-color: pink;
            box-sizing: border-box;
            border-bottom: 150px;
            border-style: solid;
            border-color: black;
            border-radius: 50%;
        }
    </style>
</head>

<body>
    <div></div>
</body>

</html>
```

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div {
            width: 300px;
            <!-- height设置为150px，content-box盒模型 -->
            height: 150px;
            background-color: pink;
            
            box-sizing: content-box;
            border-bottom: 150px;
            border-style: solid;
            border-color: black;
            border-radius: 50%;
        }
    </style>
</head>

<body>
    <div></div>
</body>

</html>
```

![image-20210410130503492](C:\Users\a\AppData\Roaming\Typora\typora-user-images\image-20210410130503492.png)

> 使用伪类元素(::before与::after)，减少盒子使用，简化HTML结构

