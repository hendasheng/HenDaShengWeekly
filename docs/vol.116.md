# 很大声周刊-vol.116
很大声周刊，在这里记录日常工作、生活所见，每周一发布。

![Title_116 1](https://github.com/hendasheng/HenDaShengWeekly/assets/20842136/6dacca7a-2cf0-4cdc-8b64-28b9e2f5cbbb)




# Git Clone 下载文件的时候出现连接超时
```
//“1080” 替换成你的电脑端口数字
git config --global http.proxy http://127.0.0.1:1080
git config --global https.proxy http://127.0.0.1:1080
```