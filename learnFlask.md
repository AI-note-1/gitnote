 # Flask的基础使用方法：
    Flask 是一个用 Python 编写的轻量级 Web 应用框架。

 ## Flask 特点
    1.轻量级和简洁：Flask 是一个微框架，提供了最基本的功能，不强制使用任何特定的工具或库。它的核心是简单而灵活的，允许开发者根据需要添加功能。

    2.灵活性：Flask 提供了基本的框架结构，但没有强制性的项目布局或组件，开发者可以根据自己的需求自定义。

    3.可扩展性：Flask 的设计允许你通过插件和扩展来添加功能。许多常见的功能，如表单处理、数据库交互和用户认证，都可以通过社区提供的扩展来实现。

    4.内置开发服务器：Flask 内置了一个开发服务器，方便在本地进行调试和测试。

    5.RESTful 支持：Flask 支持 RESTful API 的开发，适合构建现代的 Web 服务和应用程序。

 ## Flask 第一个应用与代码分析
    from flask import Flask
    app = Flask(__name__)
    @app.route('/')
    def hello_world():
        return 'Hello, World!'
        
    if __name__ == '__main__':
        app.run(debug=True)

    **注意：python是靠代码之间的缩进来表达层次关系的**

    1.**from flask import Flask**： 这行代码从 flask 模块中导入了 Flask 类。Flask 类是 Flask 框架的核心，用于创建 Flask 应用程序实例。

    2.**app = Flask(__name__)**： 这行代码创建了一个 Flask 应用实例。__name__ 是一个特殊的 Python 变量，它在模块被直接运行时是 '__main__'，在被其他模块导入时是模块的名字。传递 __name__ 给 Flask 构造函数允许 Flask 应用找到和加载配置文件。

    3.**@app.route('/')**： 这是一个装饰器，用于告诉 Flask 哪个 URL 应该触发下面的函数。在这个例子中，它指定了根 URL（即网站的主页）。

    4.**def hello_world()**:： 这是定义了一个名为 hello_world 的函数，它将被调用当用户访问根URL时。

    5.**return 'Hello, World!'**： 这行代码是 hello_world 函数的返回值。当用户访问根 URL 时，这个字符串将被发送回用户的浏览器。

    6.**if __name__ == '__main__'**:：这行代码是一个条件判断，用于检查这个模块是否被直接运行，而不是被其他模块导入。如果是直接运行，下面的代码块将被执行。

    7.**app.run(debug=True)**：这行代码调用 Flask 应用实例的 run 方法，启动 Flask 内置的开发服务器。debug=True 参数会启动调试模式，这意味着应用会在代码改变时自动重新加载，并且在发生错误时提供一个调试器。
