设置多账号
https://blog.csdn.net/weixin_42133116/article/details/115703540
https://blog.csdn.net/q13554515812/article/details/83506172
可能出现问题：不能自动切换密钥，被拒绝push或pull
解决方法是指定ssh密钥
https://geek-docs.com/git/git-questions/72_git_how_do_i_switch_between_different_usersgithub_accounts_when_pushing_repositories.html
```
$ git config --global core.sshCommand "ssh -i ~/.ssh/your_private_key"
```
或者由于指定http通信，现在切换
git remote rm origin
git remote add origin git@user1.github.com:xxx/xxxxx.git

可能无法clone项目
https://blog.csdn.net/qq_43546721/article/details/139506583
解决办法是先取消代理：
git config --global --unset http.proxy 
git config --global --unset https.proxy


