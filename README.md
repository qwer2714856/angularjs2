# angularjs2
知识点
angularjs2新特性
组件（最核心概念）、元数据、模板、数据绑定、服务、指令、依赖注入、模块
其它内容都是为组件提供服务的。

组件有点像CSS的DIV多个组件之间的嵌套生成一个大组件，大组件的嵌套生成产品。
组件树的概念。

组件有组成 (html, js, css)

组件和组件之间有一套完善的通讯机制（这个和纯DOM不同不是鼓励存在的）
每个组件可以定义自己的输入输出接口 通外接口进行通讯


组件的生命周期
构造器初始化  第一次出发数据变化钩子 组件初始化 运行期发生变化钩子 组件销毁
Constructor->OnChanges->OnInit(业务逻辑放这)->OnChanges->OnDestroy 

构造器解释
@Component({//装饰器8大核心的地方，放这
    selector : 'hello', //元数据
    template : ''// 模板
});//休息下面的类 

export class HelloComponent{//组件的业务逻辑在这

}
两部分组成

装饰器是一个丰富一个组件类的


selector 是一个css 选择器 他能匹配里面所写的选择器。
最终模板里面是
<选择器>模板</选择器>
index.html

多个组件之间串联，组件树。
父子组件
子组件的selector定义的可以在父组件的template里面调用。

父组件调用子组件需要借助于模块的导入来实现。

父组件
< [data]="item"><>

class Con....Compentent{
    @Input() data:IContact(某个类型);//子组件的输入接口。接口来自父组件的数据,这里接受父组件模板转过来的值。
}

@Input 获得父的输入
@Output 向父输出。

angular2不支持原生的数据双向绑定。

它本身也是单向数据绑定，可以借助输入输出实现双向数据绑定


指令分属性指令和结构指令


大漠清秋  
生成component 结构图
https://github.com/compodoc/ngd


