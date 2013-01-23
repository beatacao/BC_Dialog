BC_Dialog
=========

Dialog对话框插件

<h5>功能描述：</h5>
<p>
可方便的创建确认框，警示框等各种自定义弹出框;<br/>
可创建成功，报错，信息提示，警告等简介提示信息框，支持延迟时间自动关闭；
</p>
<h5>如何使用：</h5>
<ol>
    <li>引入default.css</li>
    <li>引入最新jquery库及dialog.js</li>
    <li>
        var Dialog = new BC_Dialog({设置的参数...});<br/>
        Dialog.open();  //打开Dialog<br/>
        Dialog.close(); //关闭Dialog
    </li>
</ol>
<h5>参数设置：</h5>
<dl>
    <dt>* @dropback</dt>     
    <dd>boolean 是否需要遮罩层;默认true</dd>
    <dt>* @need_close</dt>   
    <dd>boolean 是否需要关闭按钮;默认true</dd>
    <dt>* @auto_close</dt>    
    <dd>是否自动关闭dialog; <br/>
        true: 3s后自动关闭dialog; <br/>
        false:不自动关闭; <br/>
        可自行设置数值，单位ms, 如：2000;<br/>
        默认为false;</dd>
    <dt>* @buttons</dt>       
    <dd>设置dialog底部按钮，<br/>
        true: 显示按钮，需要@dialog_type来确定显示几个按钮;<br/>
        false：不显示任何按钮；<br/>
        还可自行设定需要显示的按钮，需数组形式，如：<br/>
        [<br/>
            {caption:'按钮1',id:'btn1', classes: 'class1', keyCode: 13, callback: fn1},<br/>
            {caption:'按钮2',id:'btn2', classes: 'class2', callback: fn2}<br/>
        ]<br/>
        caption: 按钮文字; id; 按钮id; classes: 按钮class名,多个class用空格隔开; keyCode: 按钮快捷键的keyCode; callback: 点击按钮的回调函数;<br/>
        默认为 true;</dd>

    <dt>* @dialog_type</dt>       
    <dd>设置dialog类型；<br/>
        confirm: 确认框, 显示‘确认’和‘取消’按钮; 需 @buttons 设置为true;<br/>
        error:错误提示；warning:警告； success：成功；info：信息；<br/>
        如果不为以上任何类型，并且 @buttons 为true, 则dialog有一个操作按钮，即‘确定’;<br/>
        默认为 confirm;</dd>
    <dt>* @id</dt>               
    <dd>字符串,设置dialog的id,默认dialog-时间戳;</dd>
    <dt>* @wrapper</dt>           
    <dd>设置dialog的外围元素, 默认为 $('body');</dd>
    <dt>* @ajaxUrl</dt>           
    <dd>设置通过ajax加载dialog内容的url;</dd>
    <dt>* @width</dt>             
    <dd>设置dialog的宽度, 默认560px</dd>
    <dt>* @height</dt>            
    <dd>设置dialog的高度,默认auto</dd>
    <dt>* @title</dt>            
    <dd>字符串,设置dialog的title, 默认为‘请确认’</dd>
    <dt>* @content</dt>           
    <dd>html或字符串,设置dialog的主体内容,默认为空</dd>
    <dt>* @ajaxUrl</dt>           
    <dd>url地址,设置此url,将通过ajax方式加载dialog主体内容</dd>
    <dt>* @keyboard</dt>         
    <dd>boolean,是否设置ESC键关闭dialog, 默认为true</dd>
    <dt>* @position</dt>          
    <dd>设置dialog定位;<br/>
        水平：left, right, center; 可设置偏移量，如： left - 20; 可直接设置数值：-20 或 -20px;<br/>
        垂直：top, bottom, middle; 可设置偏移量，如：top - 20; 可直接设置数值：-20 或 -20px;<br/>
        默认居中：['center', 'middle'], 可简写为['center']</dd>
    <dt>* @prevOpenCallback</dt>      
    <dd>设置dialog打开前的回调函数;</dd>
    <dt>* @prevCloseCallback</dt>     
    <dd>设置dialog关闭前的回调函数;</dd>
    <dt>* @openCallback</dt>      
    <dd>设置dialog打开后的回调函数;</dd>
    <dt>* @closeCallback</dt>     
    <dd>设置dialog关闭后的回调函数;</dd>
    <dt>* @okCallback</dt>      
    <dd>设置'确定'按钮回调函数;</dd>
    <dt>* @cancelCallback</dt>     
    <dd>设置'取消'按钮回调函数;</dd>
</dl>
<h5>开放接口</h5>
<dl>
    <dt>*setWidth(value)</dt>    
    <dd>设置dialog宽度</dd>
    <dt>*setHeight(value)</dt>   
    <dd>设置dialog高度</dd>
    <dt>*setTitle(msg)</dt>       
    <dd>设置dialog标题</dd>
    <dt>*setButtons(buttons)</dt>     
    <dd>添加dialog操作按钮,参数形式见@param buttons</dd>
    <dt>*setContent(content)</dt>     
    <dd>设置dialog内容</dd>
    <dt>*getAjax(url)</dt>        
    <dd>通过ajax加载dialog内容</dd>
    <dt>*open</dt>                
    <dd>打开dialog</dd>
    <dt>*close</dt>               
    <dd>关闭dialog</dd>
</dl>
