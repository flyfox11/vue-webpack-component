***hot-reload的基础---webpack-dev-server
     webpack-dev-server支持两种模式的自动刷新页面：

        iframe模式（页面嵌入一个iframe并在其中呈现页面的变化）
        inline模式（一个小型的webpack-dev-server客户端会作为入口文件打包，这个客户端会在后端代码改变的时候刷新页面）

iframe模式:使用iframe模式无需额外的配置，在终端输入命令webpack-dev-server,在浏览器中输入 http://loacalhost:8080/webpack-dev-server/index.html
inline模式:在dos下输入命令webpack-dev-server --inline --hot,启动服务器，在浏览器中打开 http://loacalhost:8080 就可以看到我们的页面，此时修改app.vue中的css，以及html中的文字，都可以看到在浏览器中立马呈现。



***export命令
export命令用于规定模块的对外接口。一个模块就是一个独立文件。该文件内的所有变量外部都无法获取。如果希望外部能够读取模块内部的某个变量，就必须使用export关键字对外暴露出该变量。例如：
//export.js
export var firstName = 'Michael';
export var lastName = 'Jackson';
export var year = 1958;
这样就可以对外输出三个变量。


***import命令
使用export对外暴露了接口后，其他js文件通过import命令加载这个模块文件。上面暴露的三个变量在另一个js文件中引入如下：
//import.js
import {firstName,lastName,year} from './export';
function setName(element){
    element.textContent = firstName + ' ' + lastName;
}