# LEARN-WEB
Visual Studio Code、Markdown、Git、Bower、Github、React、Semantic UI

## 2018-05-30

### Markdown
* 标题
    > #### 标题
* 无序列表
    > * 第一项
    > * 第二项
* 有序列表
    > 1. 第一项
    > 2. 第二项
* 区块引用
    > 解释说明
* 分割线
    > ---
* 链接
    > [百度](https://www.baidu.com/)
* 图片
    > ![图片](https://www.baidu.com/img/bd_logo1.png)
* 代码框
    > * 单行代码 `printf("Hello World!");`
    > * 多行代码
    ```
    for(int i = 0; i < 2; i++)
    {
        printf("Hello World!");
    }
    ```
* 表格
| ID | 姓名 | 年龄 | 
| :- | :-: | -: |
| 1 | Miaokit | 29 | 
| 2 | Utopiatek | 2 |
* 强调
    > _倾斜_，__加粗__
* 转义
    > \\ \' \~ \* \_ \- \+ \. \!
* 删除线
    > ~~删除~~

### Git
* 克隆仓库到本地
    > git clone repository-url local-path
* 配置GIT用户信息
    > git config --global user.name "name"

    > git config --global user.email "email"
* 修改文件
    > 被修改文件会有“M”已修改标志，点击“M”显示修改前后对比
* 暂存更改
    > 点击放弃更改相当于撤销
    
    > 点击“+”号暂存更改，点击“-”号取消暂存更改
* 提交更改
    > 点击“√”提交更改
* 同步
    > 点击同步，输入账号密码，代码同步到GitHub
* 配置.gitignore文件
```
/.vscode/
/lib/
```

### Bower
* 类似于NuGet，用于管理各种依赖库
* 在已经安装Git的前提下安装Bower插件
* 新建.bowerrc文件，设置包管理路径
```
{
    "directory": "lib"
}
```
* 新建bower.json文件，配置依赖项
```
{
    "name": "learn-web",
    "private": true,
    "dependencies": {
        "react": "latest",
        "babel": "latest",
        "babel-standalone": "latest",
        "jquery": "latest",
        "semantic-ui": "latest"
    }
}
```
* 安装依赖项 `Bower Install`

## 2018-05-31

### index.html
* 输入html，选择Simple HTML5 starting point，生成页面模板
* 引用脚本
```
<link rel="stylesheet" href="../lib/semantic-ui/dist/semantic.min.css" />
<script src="../lib/jquery/dist/jquery.min.js"></script>
<script src="../lib/semantic-ui/dist/semantic.min.js"></script>
``` 
* 调试配置文件Chrome: Launch
```
{
    "version": "0.2.0",
    "configurations": [
        {
            "type": "chrome",
            "request": "launch",
            "name": "Launch Chrome",
            "url": "http://localhost:8080",
            "file": "${workspaceRoot}/src/index.html",
            "webRoot": "${workspaceFolder}"
        }
    ]
}
```
