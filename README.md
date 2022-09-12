# nonebot_plugin_cave

适用于 Nonebot2 的 cave（回声洞）插件  
    _version:3.3_    
## 使用方法：  
用户投稿回声洞后，会自动推送给审核人（白名单B成员）进行审核，通过审核后，才能加入库中。  
## env配置：   
`WHITE_B_OWNER=["qq号","qq号"]` #设置可 __更改白名单B__ 的人员，个数不限。   
## 注意：
1.白名单B中的成员必须为bot好友，否则无法推送审核消息！  
2.（待补充）
## 目前 __cave__ 指令总览：  
以下命令需要加 __命令前缀__（默认为/），可自行设置为空  
### *群聊中*：  
#### __命令__： `/cave`  
不含参数，正常获取cave（无权限限制）  

`-g+id`：查看当前id的回声洞内容  

`-r+id`：移除该id的回声洞  

`-a+内容（支持图片，文字）`：添加回声洞（需审核） 

`-c+cd+unit`：更改当前群的冷却时间，cd：数字，unit：单位（hour，min，sec）,**____中间以空格分隔____**   

`-h`：获取cave参数帮助菜单和各项的用法（X）  

`-m`：获取新增的投稿的审核情况，时间截至到上次获取  
#### 群聊指令权限：  
白名单A：可执行`-g`，`-r`命令   

白名单B：投稿审核人  

`-c`设置cd时间：超管   
### *私聊中*：  
#### 命令：`/setcave`  
`-t+id`：通过审核    

`-f+id`：不通过审核    

`-l`：查看当前未处理的审核序号列表    

`-e+id`：以审核方式查看该id内容（X）  
#### 私聊权限：
**__所有私聊仅白名单B 审核人可用__**
### 冷却：
**__冷却时间长短、上次获取cave的时间，均为分群的存储，各群冷却互不影响__**


## 历代版本  
>cave1.0    
增加了.cave，可召唤回声洞  
------------------------------  
>cave2.0  
增加了.cave-a和.cave-s还有.cave-r作用分别是投稿、查看、删除、  
------------------------------  
>cave2.1  
修复了cave投稿时图片和文字位置错误的bug  
------------------------------  
>cave3.0  
增加了cave投稿审核，添加了-s和-r的权限（白名单A），添加了分群冷却，添加了.cave-h（以后可能会有吧？）/.cave-m/.cave-wAa/.cave-wAr/.cave-wAs/.cave-wBa/.cave-wBr/.cave-wBs
新增了私聊指令.setcave-t/.setcave-f/.setcave-e（不存在）  
------------------------------
>cave3.1  
修复了.cave-s可查看已删除的回声洞或.setcave-f不通过的回声洞、.cave-s可查看投稿的未审核内容的bug  
------------------------------  
>cave3.2  
将.cave-s改为了.cave-g同时也将.cave-wAs和.cave-wBs改为了.cave-wAg和.cave-wBg  
------------------------------  
>cave3.3   
修复：修复了-m分群显示错误的bug；修复了当此群未进行.cave-c初始化时使用其他指令引发的错误；   
更改：将白名单A分群存储；  
优化：-wAg，-wBgQQ号前面加昵称；在添加白名单时可以使用at  
新增：.cave-v获取当前cave版本，更新时间，更新日志。  
  

