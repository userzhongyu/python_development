# gx_day11项目相关

## 1.快速开发网站

安装环境

`conda insatll flask`

web.py

```python
from flask import Flask, render_template

app = Flask(__name__)


# 创建网址 /show/info 和 函数 index 的对应关系
# 以后用户在浏览器上访问 /show/info ，网站自动执行 inde1x
@app.route("/show/info")
def index():
    # return "Hello World"

    # Flask内部会自动打开这个文件，并读取其中的内容，将内容给用户返回
    # 默认：去当前项目目录的 templates 文件夹中找 index.html 文件
    # app = Flask(__name__, template_folder='xxx') 指定到 xxx 文件夹中去寻找 index.html 文件
    return render_template("index.html")

if __name__ == '__main__':
    # 自定义主机名和端口号 app.run(host=, port=)
    app.run()

```

index.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
    <h1>Hello World</h1>
</body>
</html>
```



## 2.HTML

https://www.runoob.com/html/html-tutorial.html

- 编码

- title

- 标题

- `div`和`span`

- 超链接

