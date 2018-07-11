# editor
vue + wangeditor
1、在vue的项目中引用的 wangeditor ^3.1.1 富文本编辑器 需要先 npm install 
2、用的时候直接js引入 import Editor from 'Editor.vue' 
3、模版里 <editor v-model="detail" class="editor" :menus="menus"/> 【detail为编辑器输入的值，menus为菜单配置】
   工具参考 https://www.kancloud.cn/wangfupeng/wangeditor3/332599 使用手册
    
