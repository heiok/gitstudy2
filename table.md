|id|name|
|:-:|:-:|
|1|A1|
|2|A2|
|3|A3|
start=>start: 开始
isLogin=>condition: 是否已登录？
login=>operation: 登陆
selectPic=>operation: 选择一张图片
isPic=>condition: 格式是否正确？
doIt=>operation: 完成资料
isRight=>condition: 资料是否符合要求？
end=>end: 完成

start->isLogin
isLogin(yes)->selectPic
isLogin(no)->login->selectPic
selectPic->isPic
isPic(yes)->doIt->isRight
isPic(no)->selectPic
isRight(yes)->end
isRight(no)->doIt
