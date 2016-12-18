# 12월 17일 강의 진행소스

### 1. Routing 추가
app.js (23 , 41 line)<br />
routes/posts.js

### 2. view 폴더내의 html coding

### 3. moogoose package download
<pre>
npm install --save mongodb
npm install --save mongoose
npm install --save mongoose-auto-increment
</pre>

### 4. mongodb 연결 및 mongoose app.js 셋팅<br />
app.js ( 8~18 )
<pre>
var mongoose = require('mongoose');
var autoIncrement = require('mongoose-auto-increment');

var db = mongoose.connection;
db.on( 'error' , console.error );
db.once( 'open' , function(){
    console.log("MongoDB connect");
});

var connect = mongoose.connect('mongodb://127.0.0.1/post');
autoIncrement.initialize(connect);
</pre>
