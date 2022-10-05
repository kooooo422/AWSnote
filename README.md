# AWSnote
https://oranwind.org/-aws-macos-chuan-song-dang-an-dao-aws-ec2-jiao-xue/
# travis ci
https://www.travis-ci.com/
# node express
https://medium.com/cs-note/setup-node-and-express-on-aws-ec2-windows-7-8cb499ab14eb
node express架好 安全群組要加．．． 切記
https://andy6804tw.github.io/2019/09/23/ubuntu-indtall-nodejs/
https://coderwall.com/p/plejka/forward-port-80-to-port-3000

# install
```cmd
sudo apt-get update
sudo apt-get install -y nodejs
sudo apt-get install npm
npm i express
sudo iptables -t nat -I PREROUTING -p tcp --dport 80 -j REDIRECT --to-ports 3000
```
＃ node express
```js
var express = require('express');
var app = express();
app.get('/',function(req,res){
  res.send('Hello world(test2)!\n');
})
var port = 80;
app.listen(port);
console.log('Listening on port', port);
```
