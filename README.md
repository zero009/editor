# editor<br/>
vue + wangeditor富文本编辑器<br/>
1、在vue的项目中引用的 wangeditor ^3.1.1 富文本编辑器 需要先 npm install <br/>
2、用的时候直接js引入 import Editor from 'Editor.vue' from存放的地址 <br/>
3、模版里 “<editor v-model="detail" class="editor" :menus="menus"/>” 【detail为编辑器输入的值，menus为菜单配置】<br/>
   工具参考 https://www.kancloud.cn/wangfupeng/wangeditor3/332599 使用手册<br/>
    
4、遇到难点：<br/>
   &nbsp;图片在进行本地上传的时候需要对图片的宽高进行限制，但由于该工具是简洁版并为针对这块进行设置，只能获取到图片大小size<br/>
   &nbsp;在提供的自定义上传图片事件中引入了ES2017的新特性 async function 异步函数 通过 await 处理异步 async 计算的结果和错误 
   &nbsp;await（只允许在 async(异步) 函数内部使用）等待其操作对象 Promise 返回：<br/>
   &nbsp;如果 Promise 是完成状态，await 的结果是完成态的值。
   &nbsp;如果 Promise 是拒绝状态，await 会抛出拒绝值。<br/>
5、未做处理：<br/>
   网络链接图片地址无法进行限制，仅能获取到宽高，没想到好的解决方案，只能在插入前进行限制，唯一想到的就是需要对源码进行修改，后面需求被砍了就没细做了。<br/>
6、知识点：<br/>
   &nbsp;XMLHttpRequest 对象用于在后台与服务器交换数据。   
