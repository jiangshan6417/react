# react
有关于react的知识

##一、React历史
        1、简介
        React是较早使用JavaScript构建大型、快速应用程序的技术方案，React 由 Facebook 的软件工程师 Jordan Walke 开发的一款JS库，
        最早应用于Facebook公司的内部项目，在2013年成为开源框架，2015年在F8大会上发布了React Native，一款针对于手机端的开源框架；
        
        2、开发原因
        在当时的市场中Facebook认为市场上的MVC无法满足他们的扩展需求，由于他们非常巨大的代码库和庞大的组织，每当添加一项新的功能
        或者特性的时候，系统的复杂度就成级数增长，以至于代码变得脆弱和不可预测。所以自己写了一款UI框架，所以就有了React框架；
##二、设计思想
        1、React框架不是一个MVC框架，而是用于构建组件化UI的库，主要是一个前端界面的开发工具，很多人认为是MVC中的V部分,主要解决
        问题：构建随着时间不断变化的大规模应用程序。
        2、编写可预测的代码
        既编写易于理解的代码，在react发布会上，React项目经理React项目经理TomOcchino进一步阐述React诞生的初衷，在演讲中提到，
        React最大的价值究竟是什么？是高性能虚拟DOM、服务器端Render、封装过的事件机制、还是完善的错误提示信息？尽管每一点都
        足以重要。但他指出，其实React最有价值的是声明式的，直观的编程方式。这样的编码方式让使用者能够更容易的阅读、编写和修
        改代码。
        3、简化可复用的组件
        React构建UI是使用组件化的方式，而不是常见的模板。组件并不是一个新概念，它是某个独立功能或者界面的封装，达到复用或者UI
        和业务松耦合的目的。
##三、学习内容
        1、基本数据展示，可以下载React官网上入门压缩包
        新建一个HTML页面：
        <!DOCTYPE html>
                <html>
                  <head>
                    <title>Hello React</title>
                    <script src="http://fb.me/react-0.14.7.js"></script>  //引入react核心库
                    <script src="http://fb.me/JSXTransformer-0.14.7.js"></script> //引入将jsx文件转换为Js文件的包
                  </head>
                  <body>
                    <div id="example"></div>
                    <script type="text/jsx">//React独有的jsx语法，与JavaScript不兼容
                
                      // ** 在这里替换成你的代码 **
                
                    </script>
                  </body>
                </html>
        在注释位置处，写入下面的代码：        
                var HelloWorld = React.createClass({//创建一个组件类
                          render: function() {//返回一个React方法组件树，最终渲染成HTML
                            return (
                              <p>//不是真正的DOM节点，而是React的实例，是一种标签或者是数据，react对其进行处理，避免XSS攻击
                                Hello, <input type="text" placeholder="Your name here" />!
                                It is {this.props.date.toTimeString()}
                              </p>
                            );
                          }
                        });
                        
                        setInterval(function() {
                          React.render(//实例化根组件
                            <HelloWorld date={new Date()} />,
                            document.getElementById('example')
                          );
                        }, 500);
        主要功能：1、模块化、可组装的组件，组件可以复用
                  2、行为与形态的分离
        
        
        
        
