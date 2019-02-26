## leetcode
  
  - 艾特群友（微信昵称：天色渐晚）加github私有仓库权限，告知github账号(username)
  - **接下来就需要熟悉git的基本用法，请熟悉之后才继续操作吧！！！git技巧是软件开发必备技巧之一，建议不要强撸**
  - **本仓库的建议旨在相互监督，采用每个人一个目录形式管理；对他人目录仅有只读权限，发现问题可提交issue，并@他/她（目录即用户名哦）**
  - 小分队github仓库地址：https://github.com/tianser/leetcode.git
  - ==============
  - 第一次执行：git clone 到本地； 
  - 第N次执行：git checkout master && git pull && git branch -d {github帐户}  //删除存在的分支
  - ===============
  - cd leetcode 
  - **以下是核心,务必按步骤操作**
  - git branch {github帐户}     //创建自己的开发分支
  - git checkout {github帐户}   //切换到自己的分支上，**以后增删改等操作都在自己的分支上进行，新手切记, 老鸟忽略**
  - mkdir {github帐户}          //创建与自己githbub帐户同名的目录，用来存放自己的代码
  - //愉快的刷题
  - git add . && git commit -s -m "{提交注解}"
  - git push origin {github帐户}:{github帐户}      //提交到远端仓库
  - 进入https://github.com/tianser/leetcode页面; 选择New pull request;
  
  ![avatar](https://github.com/tianser/leetcode/blob/master/tianser/img/113.png）
  - 然后create pull request，自行merge；也可以指定别人帮你review代码，在右边
  
  ![avatar](https://github.com/tianser/leetcode/blob/master/tianser/img/115.png）
  
  ![avatar](https://github.com/tianser/leetcode/blob/master/tianser/img/116.png）
  
  ![avatar](https://github.com/tianser/leetcode/blob/master/tianser/img/118.png）
  
  ![avatar](https://github.com/tianser/leetcode/blob/master/tianser/img/119.png）
  - 备注：更新冲突导致无法merge的问题，请自行google
  
