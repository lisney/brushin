NodeJs A
========

1. Nodemon 설치

``npm i -g nodemon(글로벌로 설치, 실행 'nodemon start' - package.json main에 등록한 js파일 ``

2. VScode Autocomplition
 
``npm install --save-dev @types/node``

3. package.json 

``npm init -y``

4. express - NodeJs 서버 프레임워크, handlebars - 템플릿엔진

``설치 - npm install express-handlebars``

5. express 가 bodyParser 모듈 내장 urlencoded, json 파서

.. code-block::

    // app.use(bodyParser.urlencoded({extended:true} bodyParser 모듈 불러올 필요없이
    app.use(express.urlencoded({extended:true}
    app.use(express.json(


 * flash - 사용자에게 메시지 띄워주는 미들웨어
 express-flash: connect-flash와 같은기능을 하는 


6. ES6 이상 문법 사용 - require 대신 import

.. code-block:: console


 * import {}

 - ap.js
 const a = 1;
 const b = 2;
 export { a }; //a와 c는 {}로 import해야한다. 변수명이 같게 써야한다.
 export const c = 3; //선언과 동시에 할당한 한 변수는 import 시 {}안에 써야한다
 export default b; // b는 기본 변수, {}없이 받으며...변수명이 달라도(d 괜찮다 

 - main.js
 import d, { a, c as e } from "./ap.js";
 console.log(a, d, e;

.. code-block::

   require 대신 ES6 import 사용하기 package.json 에  "type":"module" 추가
   기존 require 방식 사용 시 "type": "commonjs"로 명기할 수 있다.

  'babel-node' 에러시 - npm i @babel/node -g 설치
  
   ES6에는 __dirname 변수가 없다
    import path from 'path';
    const __dirname = path.resolve(;
    
 * Require 사용하기 
 import { createRequire } from "module";
 const require = createRequire(import.meta.url;
 const db_config = require("./db-config.json";

 * __dirname 사용하기
 import path from 'path';
 const __dirname = path.resolve(;

 * dotenv
 import "dotenv/config.js";
 또는
 // loadEnv.js
 import dotenv from 'dotenv';
 dotenv.config(

 // index.js
 import './loadEnv';
 import express from 'express';
 let x = process.env.David;
 console.log(x;

 * import router file
 export const myRouteHandler = async (req, res => {
   ...
 };
 import { myRouteHandler } from "./myModule";
 app.post('/exampleroute', myRouteHandler
 ----------------------------------------
 또는
 //router.js
 import express from 'express';
 export const router = express.Router(;

 router.get("/", async (req, res => {
  res.render("login";
 };
 //app.js
 import { router } from "./router.js"; // .js 붙여줘야 인식?
 app.use("/", router;


7. handldbars 신버전 데이터 전달

.. code-block::

 - 구버전을 사용하던가 Original JSON을 반환하는 '.lean('옵션을 추가한다

 router.get('/list',(req,res=>{
    Employee.find((err,docs=>{
        if(!err{
            res.render('employee/list',{
                list: docs
            }
        }
    }.lean( //lean 옵션 추가
 }


8. Prettier Handlebars 파일에 적용하지 않기

.. code-block::

  "[handlebars]": {
    "editor.formatOnSave": false,
    "editor.formatOnPaste": false
  }
  
 -특정 파일에 적용하지 않기 
  "prettier.disableLanguages": [
    "css"
]



손잡이 기초
----------

.. image:: https://user-images.githubusercontent.com/30430227/150886419-134eed43-46d9-4789-9fe2-4fb7dafe8488.png

1. app.js 

.. code-block:: console

 import express from 'express';
 import { engine } from 'express-handlebars';

 const app = express(;

 app.engine('handlebars', engine(;
 app.set('view engine', 'handlebars';
 app.set('views', './views';

 app.get('/', (req, res => {
    res.render('home';
 };

 app.listen(3000;


2. main.handlebars

.. code-block:: console

 <!DOCTYPE html>
 <html>
 <head>
    <meta charset="utf-8">
    <title>Example App</title>
 </head>
 <body>

    {{{body}}}

 </body>
 </html>



3. home.handlebars

.. code-block:: console

 <h1>Example App: Home</h1>



이전 버전 갱신
--------------

.. image:: https://user-images.githubusercontent.com/30430227/150892194-3f63963c-acc6-4715-b7ff-2d417762262a.png


.. code-block:: console

 ``app.js``

 import express from 'express';
 import { engine } from 'express-handlebars';
 import path from 'path'

 const __dirname = path.resolve(
 //ES6부터는 __dirname 변수가 없다. path.resolve(는 현재 경로의 절대경로 반환, path.join(은 상대경로
 const port = 3000

 const app = express(;

 app.engine('hbs', engine({
    extname: 'hbs',
    defaultLayout:'layout', //기본 레이아웃인 main.hbs 대신 사용할 레이아웃명 
 };
 app.set('view engine', 'hbs';
 app.set('views', './views'; //기본 views폴더 대신 사용할 경로 지정시 사용

 app.use(express.static(__dirname
 app.use((req,res,next=>{
    next(
 }

 app.get('/', (req, res => {
    res.render('index',{
        name:'Brush'
    };
 };

 app.listen(port, "192.168.0.21",(=>{
    console.log(``The server is running on Port ${port}``
 };

.. code-block:: console

 ``index.hbs``

 <h1>Example App: {{name}} </h1>



MySQL
------

1. 설치

``npm i mysql``

2. 연결하기 

.. code-block:: console

 import mysql from "mysql";

 const con = mysql.createConnection({
  host: "localhost",
  user: "root",
  password: "brush",
 };

 con.connect((err => {
  if (err throw err;
  console.log("Connected";
 };

 * 암호보안
 //db-config.json
 {"host":"localhost", "user":"root", "password":"brush","database":"express_db"}

 //require 사용하기 - JSON 파일 import 지원안한다(assert 로 잘 안된다
 import { createRequire } from "module";
 const require = createRequire(import.meta.url;

 const db_config = require("./db-config.json";

 //사용하기 - 2.연결하기 내용 수정 
 const con = mysql.createConnection({ //con = connection
  host: db_config.host,
  user: db_config.user,
  password: db_config.password,
 };


3. 쿼리 사용하기 - .query 메소드

.. code-block:: console

 * db 생성 - 생성 후 생성코드는 삭제
 con.connect((err => {
  if (err throw err;
  console.log("Connected";
  con.query("create database express_db", (err, result => {
    if (err throw err; //throw - 강제 예외처리
    console.log("database created";
  };
 };

 * db 연결
 const con = mysql.createConnection({
  host: db_config.host,
  user: db_config.user,
  password: db_config.password,
  database: "express_db",
 };

 * 테이블 생성 
 con.connect((err => {
  if (err throw err;
  console.log("Connected";
  const sql =
    "create table users (id int not null primary key auto_increment, name varchar(255 not null, email varchar(255 not null";
  con.query(sql, (err, result => {
    if (err throw err;
    console.log("table created";
  };
 };

 * MySQL 워크벤치를 이용해 데이터 입력

 * 데이터 추출
 con.connect((err => {
  if (err throw err;
  console.log("Connected";
  const sql = "select * from users";
  con.query(sql, (err, result => {
    if (err throw err;
    console.log(result;//인덱스 0의 email만 보기 > console.log(result[0].email;
  };
 };

 * 브라우저로 보내기 
 app.get("/", (req, res => {
  const sql = "select * from users";
  con.query(sql, (err, result, fields => {
    if (err throw err;
    console.log(result;
    res.send(result;
  };
  
 * 데이터 입력해보기
 con.connect((err => {
  if (err throw err;
  console.log("Connected";
  const sql = "insert into users(name,email values('Kevin','k@ke.com'";
  con.query(sql, (err, result, fields => {
    if (err throw err;
    console.log(result;
  };
 };


4. 입력폼 작성

.. code-block:: console

 * index.hbs
 <h1>입력폼</h1>
 <form action="/" method="POST">
    <label for="">이름</label>
    <input type="text" name="name">
    <label for="">메일</label>
    <input type="text" name="email">
    <button type="submit">보내기</button>
 </form>


 * 브라우저에서 들어온 데이터 처리 미들웨어 - body-parser 기능 내장
 app.use(express.urlencoded({extended:true};
 // app.js 이렇게 수정
 app.get("/", (req, res => {
  res.render("index", {};
 };

 app.post("/", (req, res => {
  res.send(req.body;
 };


 * 데이터베이스에 Insert하기
 //INSERT INTO table (a, b, c VALUES (1,2,3를 INSERT INTO table SET a=1, b=2, c=3 로 대체할 수 있다

 app.post("/", (req, res => {
  const sql = "insert into users set ?";//물음표 (? 삽입하면 값 배열로 대체됨
  con.query(sql, req.body, (err, result, fields => {
    if (err throw err;
    console.log(result;
    res.send("등록이 완료"; //res.redirect("/" 해당 경로로 되돌아감
  };
 };



 * 템플릿 엔진 사용 - lean( 안써도 에러안난다^^
 app.get("/", (req, res => {
  const sql = 'select * from users';
  con.query(sql, (err,result,fields=>{
    if(err throw err;
    res.render('index',{users:result}
  }
 };


 //index.hbs
 <table>
    <tr>
        <th>이름</th>
        <th>이메일</th>
        <th>수정</th>
        <th>삭제</th>
    </tr>
    {{#each users}}
    <tr>
        <td>{{this.name}} </td>
        <td>{{this.email}} </td>
        <td><a href="/edit/{{this.id}}">수정</a> </td>
        <td><a href="/delete/{{this.id}}">삭제</a> </td>
    </tr>
    {{/each}}
 </table>

.. image:: https://user-images.githubusercontent.com/30430227/152928825-c5306584-89e0-4af3-8b5b-8bd0f5a20053.png


5. 수정과 삭제

.. code-block:: console

 app.get("/delete/:id", (req, res => {
  const sql = "delete from users where id = ?";
  con.query(sql, [req.params.id], (err, result, fields => {
    if (err throw err;
    console.log(result;
    res.redirect("/";
  };
 };

 * edit.hbs
 <h1>업데이트 폼</h1>

 <form action="/update/{{user.0.id}}" method="POST">
    <label for="">이름</label>
    <input type="text" name="name" value="{{user.0.name}}">
    <label for="">메일</label>
    <input type="text" name="name" value="{{user.0.email}}">
    <button type="submit">업데이트</button>
 </form>


6. 전체 코드

.. code-block:: console

 import express from "express";
 import { engine } from "express-handlebars";
 import path from "path";
 import mysql from "mysql";

 import { createRequire } from "module";
 const require = createRequire(import.meta.url;
 const db_config = require("./db-config.json";

 const con = mysql.createConnection({
  host: db_config.host,
  user: db_config.user,
  password: db_config.password,
  database: "express_db",
 };

 con.connect((err => {
  if (err throw err;
  console.log("Connected";
 };

 const __dirname = path.resolve(;

 const port = 3000;

 const app = express(;

 app.engine(
  "hbs",
  engine({
    extname: "hbs",
    defaultLayout: "main",
  }
 ;

 app.set("view engine", "hbs";
 app.set("views", "./views";

 app.use(express.urlencoded({ extended: true };
 app.use(express.json(;
 app.use(express.static(__dirname;
 app.use((req, res, next => {
  next(;
 };

 app.get("/", (req, res => {
  const sql = "select * from users";
  con.query(sql, (err, result, fields => {
    if (err throw err;
    res.render("index", { users: result };
  };
 };

 app.get("/delete/:id", (req, res => {
  const sql = "delete from users where id = ?";
  con.query(sql, [req.params.id], (err, result, fields => {
    if (err throw err;
    console.log(result;
    res.redirect("/";
  };
 };

 app.get("/edit/:id", (req, res => {
  const sql = "select * from users where id = ?";
  con.query(sql, [req.params.id], (err, result, fields => {
    if (err throw err;
    console.log(result;
    res.render("edit-user", { result };
  };
 };

 app.post("/update/:id", (req, res => {
  const sql = ``update users set ? where id = ${req.params.id}``;
  con.query(sql, req.body, (err, result, fields => {
    if (err throw err;
    console.log(result;
    res.redirect("/";
  };
 };

 app.post("/", (req, res => {
  const sql = "insert into users set ?";
  con.query(sql, req.body, (err, result, fields => {
    if (err throw err;
    console.log(result;
    res.redirect("/";
  };
 };

 app.listen(port, ( => {
  console.log(``The Server is Running on Port ${port}``;
 };



`부트스트랩<https://getbootstrap.com/docs/5.1/getting-started/introduction>`_

`부트스트랩 아이콘CDN<https://icons.getbootstrap.com/#usage>`_


Dependencies Installation
----------------------

.. code-block:: 

 npm install express dotenv express-handlebars body-parser mysql
 //dotenv - 단일 상황에 대한 보안값을 담은 단일 파일 .env
 npm install --save-dev nodemon //nodemon start 로 실행한다 하지만
 //노드몬을 npm start로 실행하기 위해 package.json를 다음과 같이 설정할 수 있다.
  "scripts": {
    "start": "nodemon app.js",
    "test": "echo \"Error: no test specified\" && exit 1"
  },


 * package.json
  "type": "module"


.. image:: https://user-images.githubusercontent.com/30430227/153152900-0ce070ab-1a32-410b-b1a4-dfa5a1a4c2a4.png

.. image:: https://user-images.githubusercontent.com/30430227/153152957-b7a1fd98-a780-41e2-80cc-4b261c47a6eb.png


전체코드 
--------

.. code-block:: console

 *  .env
 DB_HOST = localhost
 DB_NAME = express_db
 DB_USER = root
 DB_PASS = brush


.. code-block:: console

 * app.js

 import express from "express";
 import { engine } from "express-handlebars";
 import path from "path";
 import mysql from "mysql";
 import dotenv from "dotenv";
 dotenv.config(;

 import { createRequire } from "module";
 const require = createRequire(import.meta.url;
 const db_config = require("./db-config.json";

 const con = mysql.createConnection({
  host: process.env.DB_HOST,
  user: process.env.DB_USER,
  password: process.env.DB_PASS,
  database: process.env.DB_NAME,
 };

 con.connect((err => {
  if (err throw err;
  console.log("Connected";
 };

 const __dirname = path.resolve(;

 const port = 3000;

 const app = express(;

 app.engine(
  "hbs",
  engine({
    extname: "hbs",
    defaultLayout: "main",
  }
 ;

 app.set("view engine", "hbs";
 app.set("views", "./views";

 app.use(express.urlencoded({ extended: true };
 app.use(express.json(;
 app.use(express.static(__dirname;
 app.use((req, res, next => {
  next(;
 };

 app.get("/", (req, res => {
  const sql = "select * from users";
  con.query(sql, (err, result, fields => {
    if (err throw err;
    res.render("home", { result };
  };
 };

 app.get("/adduser", (req, res => {
  res.render("add-user";
 };

 app.get("/viewuser/:id", (req, res => {
  const sql = "select * from users where id = ?";
  con.query(sql, [req.params.id], (err, result, fields => {
    if (err throw err;
    console.log(result;
    res.render("view-user", { result };
  };
 };

 app.post("/adduser", (req, res => {
  const sql = "insert into users set ?";
  con.query(sql, req.body, (err, result, fields => {
    if (err throw err;
    console.log(result;
    res.redirect("/";
  };
 };

 app.get("/delete/:id", (req, res => {
  const sql = "delete from users where id = ?";
  con.query(sql, [req.params.id], (err, result, fields => {
    if (err throw err;
    console.log(result;
    res.redirect("/";
  };
 };

 app.get("/edit/:id", (req, res => {
  const sql = "select * from users where id = ?";
  con.query(sql, [req.params.id], (err, result, fields => {
    if (err throw err;
    console.log(result;
    res.render("edit-user", { result };
  };
 };

 app.post("/update/:id", (req, res => {
  const sql = ``update users set ? where id = ${req.params.id}``;
  con.query(sql, req.body, (err, result, fields => {
    if (err throw err;
    console.log(result;
    res.redirect("/";
  };
 };

 app.post("/", (req, res => {
  const sql = "insert into users set ?";
  con.query(sql, req.body, (err, result, fields => {
    if (err throw err;
    console.log(result;
    res.redirect("/";
  };
 };

 app.listen(port, ( => {
  console.log(``The Server is Running on Port ${port}``;
 };


.. code-block:: console

    * views/layouts/main.hbs
    <!DOCTYPE html>
    <html lang="ko">
    <head>
    <meta charset="UTF-8">
    <title>Document</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.8.1/font/bootstrap-icons.css">
    </head>
    <body>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container-fluid">
        <a href="/" class="navbar-brand">User Management system</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" area-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
                <a href="/" class="nav-link active" aria-current="page" >Home</a>
            </li>
            </ul>

            <form action="/" class="d-flex" method="POST" novalidate>
            <input type="search" class="from-control me-2" placeholder="Search" name="search" aria-label="Search">
            <button class="btn btn-outline-light" type="submit">Search</button>
            </form>
        </div>
        </div>
    </nav>

    <div class="container pt-5 pb-5">
        {{{body}}}
    </div>
    </body>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p" crossorigin="anonymous"></script>
    </html>

    * views/partials/user-form.hbs
    <div class="col-6">
        <div class="form-floating mb-3">
        <input type="text" class="form-control" id="floatingInput" value="{{this.id}}" placeholder="Id" name="id">
        <label for="floatingInput">아이디</label>
        </div>
    </div>
    <div class="col-6">
        <div class="form-floating mb-3">
        <input type="text" class="form-control" id="floatingInput" value="{{this.name}}" placeholder="Name" name="name">
        <label for="floatingInput">이름</label>
        </div>
    </div>
    <div class="col-6">
        <div class="form-floating mb-3">
        <input type="email" class="form-control" id="floatingInput" value="{{this.email}}" placeholder="email@email.com" name="email">
        <label for="floatingInput">이메일</label>
        </div>
    </div>

    <div class="col-12 d-grid">
        <button class="btn btn-primary" type="submit">Submit</button>
    </div>
    
    * views/home.hbs
    {{#if removedUser}}
    <div class="alert alert-success alert-dismissible fade show" role="alert">
        User has been removed.
        <button class="btn-close" data-bs-dismiss="alert" aria-label="Close"></button>
    </div>
    {{/if}}

    <div class="row">
        <div class="col-6">
            <h1>Users</h1>
        </div>
        <div class="col-6 d-flex justify-content-end">
            <a href="/adduser" class="btn btn-primary align-self-center" type="button">+add user</a>
        </div>
    </div>

    <table class="table table-bordered">
        <thead class="thead-dark">
            <tr>
                <th scope="col">#</th>
                <th scope="col">Name</th>
                <th scope="col">Email</th>
                <th scope="col" class="text-end">Action</th>
            </tr>
        </thead>
        <tbody>
            {{#each result}}
            <tr>
                <th scope="row">{{this.id}}</th>
                <td>{{this.name}} </td>
                <td>{{this.email}} </td>
                <td class="text-end">
                    <a href="/viewuser/{{this.id}} " type="button" class="btn btn-light btn-small">
                        <i class="bi bi-eye"></i>View
                    </a>
                    <a href="/edit/{{this.id}} " type="button" class="btn btn-light btn-small">
                        <i class="bi bi-pencil"></i>Edit
                    </a>
                    <a href="/delete/{{this.id}}" type="button" class="btn btn-light btn-small">
                    <i class="bi bi-person-x"></i>Delete</a>
                </td>
            </tr>
            {{/each}}
        </tbody>
    </table>

    * views/add-user.hbs
    <nav aria-label="breadcrumb">
    <ol class="breadcrumb">
        <li class="breadcrumb-item"><a href="/">Home</a></li>
        <li class="breadcrumb-item active" aria-current="page">New User</li>
    </ol>
    </nav>

    {{#if alert}}
    <div class="alert alert-success alert-dismissible fade show" role="alert">
    {{alert}}
    <button type="button" class="btn-close" data-bs-dismiss="alert" aria-label="Close"></button>
    </div>
    {{/if}}

    <form class="row g-3 needs-validation" method="POST" action="/adduser" novalidate>
    {{> user-form}}
    </form>

    * views/edit-user.hbs
    <nav aria-label="breadcrumb">
    <ol class="breadcrumb">
        <li class="breadcrumb-item"><a href="/">Home</a></li>
        <li class="breadcrumb-item active" aria-current="page">Edit User</li>
    </ol>
    </nav>

    {{#if alert}}
    <div class="alert alert-success alert-dismissible fade show" role="alert">
        {{alert}}
        <button type="button" class="btn-close" data-bs-dismiss="alert" aria-label="Close"></button>
    </div>
    {{/if}}

    {{#each result}}
    <form class="row g-3 needs-validation" method="POST" action="/update/{{this.id}}" novalidate> 
    {{> user-form}}
    </form>
    {{/each}}

    * views/view-user.hbs
    <nav aria-label="breadcrumb">
    <ol class="breadcrumb">
        <li class="breadcrumb-item"><a href="/">Home</a></li>
        <li class="breadcrumb-item active" aria-current="page">View User</li>
    </ol>
    </nav>

    <div class="view-user p-5">
    {{#each result}}
    <div class="row mb-5">
        <div class="col text-center">
        <h3>{{this.id}} {{this.name}}</h3>
        </div>
    </div>
    <div class="row">
        <div class="col">
        <table class="table">
            <thead>
            <tr>
                <th scope="col">ID</th>
                <th scope="col">Name</th>
                <th scope="col">Email</th>
            </tr>
            </thead>
            <tbody>
            <tr>
                <th scope="row">{{this.id}}</th>
                <td>{{this.name}}</td>
                <td>{{this.email}}</td>
            </tr>
            </tbody>
        </table>
        </div>
        <div class="row">
        <div class="col">
            <b>Comments</b>
        </div>
        </div>
        <div class="row">
        <div class="col">
            {{this.comments}}
        </div>
        </div>
    </div>
    {{/each}}
    </div>




Nodejs-UserManagement-Express-Hbs-MySQL-main 샘플 사용법
------------------------------------------

`깃허브<https://github.com/RaddyTheBrand/Nodejs-UserManagement-Express-Hbs-MySQL>`_

`튜토<https://www.raddy.dev/blog/simple-user-management-system-nodejs-express-mysql-handlebards>`_

.. code-block:: console


    * a.env
    DB_HOST = localhost
    DB_NAME = usermanagement_tut
    DB_USER = root
    DB_PASS = password

    * install
    $ npm install
    $ npm start



회원가입, 로그인
--------------

`참조사이트<https://codeshack.io/basic-login-system-nodejs-express-mysql>`_

.. image:: https://user-images.githubusercontent.com/30430227/153364585-74bccbce-b8a4-4a73-a321-1bedfa33bf71.png

1. SQL

.. image:: https://user-images.githubusercontent.com/30430227/153357837-07dc307a-7902-4327-bdb5-23bdc246a530.png

.. code-block:: console

    CREATE DATABASE IF NOT EXISTS ``nodelogin`` DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci;
    USE ``nodelogin``;

    CREATE TABLE IF NOT EXISTS ``accounts`` (
    ``id`` int(11 NOT NULL AUTO_INCREMENT,
    ``username`` varchar(50 NOT NULL,
    ``password`` varchar(255 NOT NULL,
    ``email`` varchar(100 NOT NULL,
    PRIMARY KEY (``id``
    ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8;

    INSERT INTO ``accounts`` (``id``, ``username``, ``password``, ``email`` VALUES (1, 'test', 'test', 'test@test.com';



2. .env

.. code-block:: console

    DB_HOST = localhost
    DB_NAME = nodelogin
    DB_USER = root
    DB_PASS = brush



3. app.js, router.js(/routers/router.js

.. code-block:: console

    import express from "express";
    import { engine } from "express-handlebars";
    import path from "path";
    import { createRequire } from "module";

    const require = createRequire(import.meta.url;
    const __dirname = path.resolve(;
    const port = 3000;

    const app = express(;

    app.engine(
    "hbs",
    engine({
        extname: "hbs",
    }
    ;

    app.set("view engine", "hbs";

    app.use(express.static(__dirname;
    app.use((req, res, next => {
    next(;
    };

    import { router } from "./routers/router.js";
    app.use("/", router;

    app.listen(port, ( => {
    console.log(``The Server is Running on Port ${port}``;
    };

.. code-block:: console

    import mysql from "mysql";
    import session from "express-session";
    import dotenv from "dotenv";
    import express from "express";
    export const router = express.Router(;

    dotenv.config(;

    const connect = mysql.createConnection({
    host: process.env.DB_HOST,
    user: process.env.DB_USER,
    password: process.env.DB_PASS,
    database: process.env.DB_NAME,
    };

    router.use(
    session({
        secret: "secret",
        resave: true,
        saveUninitialized: true,
    }
    ;

    router.use(express.urlencoded({ extended: true };
    router.use(express.json(;

    router.get("/", async (req, res => {
    res.render("login";
    };

    router.post("/auth", (req, res => {
    let username = req.body.username;
    let password = req.body.password;
    if (username && password {
        connect.query(
        "select * from accounts where username = ? and password = ?",
        [username, password],
        (err, results, fields => {
            if (err throw error;
            if (results.length > 0 {
            req.session.loggedin = true;
            req.session.username = username;
            res.redirect("/home";
            } else {
            res.send("Incorrect Username and/or Password!";
            }
            res.end(;
        }
        ;
    } else {
        res.send("Please enter Username and Password!";
        res.end(;
    }
    };

    router.get("/home", (req, res => {
    if (req.session.loggedin {
        res.send("Welcome back, " + req.session.username + "!";
    } else {
        res.send("Please login to view this page!";
    }
    res.end(;
    };



4. login.hbs

.. code-block:: console

    <div class="login">
        <h1>Login</h1>
        <form action="/auth" method="post">
            <label for="username">
                <i class="bi bi-alarm"></i>
            </label>
            <input type="text" name="username" placeholder="Username" id="username" required>
            <label for="password">
                <i class="bi bi-mailbox2"></i>
            </label>
            <input type="password" name="password" placeholder="Password" id="password" required>
            <input type="submit" value="Login">
        </form>
    </div>



5. style.css

.. code-block:: console

    * {
    box-sizing: border-box;
    }

    body {
    background: slategray;
    }

    .login {
    width: 400px;
    background: white;
    box-shadow: 0 0 9px 0 rgba(0, 0, 0, 0.3;
    margin: 100px auto;
    }
    .login h1 {
    text-align: center;
    color: slategray;
    font-size: 24px;
    padding: 20px 0;
    border-bottom: 1px solid lightblue;
    }
    .login form {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    padding-top: 20px;
    }
    .login form label {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 50px;
    height: 50px;
    background: dodgerblue;
    color: white;
    }
    .login form input[type="password"],
    .login form input[type="text"] {
    width: 310px;
    height: 50px;
    margin-bottom: 20px;
    padding: 0 15px;
    }

    .login form input[type="submit"] {
    width: 100%;
    padding: 15px;
    margin-top: 30px;
    background: dodgerblue;
    border: 0;
    cursor: pointer;
    font-weight: bold;
    color: white;
    transition: 0.2s;
    }
    .login form input[type="submit"]:hover {
    background: deepskyblue;
    }


Passport
----------

1. app.js

.. image:: https://user-images.githubusercontent.com/30430227/154609195-70360437-5383-404b-b61d-cb656ec0d78d.png
.. image:: https://user-images.githubusercontent.com/30430227/154609224-f06ddeab-fe47-43d0-ba73-048835199b14.png

.. code-block:: console

    import express from "express";
    const app = express(;
    import { router } from "./router.js";

    import expressSession from "express-session";
    import passport from "./passport.js";
    import flash from "express-flash";

    import { engine } from "express-handlebars";
    app.engine(
    "hbs",
    engine({
        extname: "hbs",
    }
    ;

    const port = 3000;

    app.set("view engine", "hbs";

    app.use(express.urlencoded({ extended: true };
    app.use(express.json(;

    //expressSession 미들웨어는 passport.session미들웨어 앞에 있어야한다
    app.use(
    expressSession({
        secret: "my Key",//필수옵션, 세션 암호화
        resave: true,//변경사항 없어도 요청마다 세션 다시 저장
        saveUninitialized: true,//저장할 내용이 없더라도 uninitialized 상태의 세션을 저장
    }
    ;

    app.use(passport.initialize(;
    app.use(passport.session(;
    app.use(flash(;// 내부적으로 session을 이용하기 때문에 session미들웨어 아래에 위치

    app.use("/", router;

    app.listen(port, ( => {
    console.log(``The server is running on port ${port} ``;
    };



2. /passport.js, /router.js 

.. code-block:: console

    import passport from "passport";

    import { Strategy as LocalStrategy } from "passport-local";

    passport.use(
    "local-login",
    new LocalStrategy(
        {
        usernameField: "username",//요청정보를 req.body.username 대신 username 로 받는다
        passwordField: "password",
        passReqToCallback: true,
        },
        (req, username, password, done => {
        //done( 함수를 이용해서 로그인 성공/실패 상태를 처리한다
        console.log("passport의 local-login :", username, password;

        if (username != "kang" || password != "12345" {
            console.log("입력정보 불일치!";
            return done(null, false, req.flash("loginMessage", "비밀번호 불일치!";
        }
        console.log("로그인 성공!";
        return done(null, {
            username: username,
            password: password,
        };
        }
    
    ;

    // (2 - 로그인 인증 성공 시 한 번만 실행
    passport.serializeUser((user, done => {
    console.log("serializeUser( 호출됨";
    console.log(user;//세션에 사용자 정보인 user를 저장, 보통은 user.id를 사용한다

    done(null, user;
    };

    // (3 - 로그인 인증이 되어있는 경우, 요청할 때마다 실행
    passport.deserializeUser((user, done => {
    //로그인 한 사용자가 들어올 때마다 deserializeUser가 실행된다(반복, 사용자는 user 정보로 사용자 식별한다
    console.log("deserializeUser( 호출됨";
    console.log(user;

    done(null, user;
    };

    export default passport;

.. code-block:: console


    import express from "express";
    export const router = express.Router(;

    import passport from "./passport.js";

    router.get("/login", (req, res => {
    res.render("login", { title: "인덱스" };
    };

    router.post(
    "/login",
    passport.authenticate("local-login", {
    //"local" - 로컬 전략을 쓰겠다.(페이스북/구글 전략...
        successRedirect: "/loginSuccess",
        failureRedirect: "/loginFail",
        failureFlash: true,
    }
    ;

    router.get("/loginSuccess", (req, res => {
    res.render("loginsuccess";
    };

    router.get("/loginFail", (req, res => {
    res.render("loginFail";
    };


인증 
--------

1. MySQL Workbench

.. image:: https://user-images.githubusercontent.com/30430227/153522325-099819f6-a94d-41f8-9f1f-c07fc5ad69f1.png
.. image:: https://user-images.githubusercontent.com/30430227/153522344-c095c648-e92a-4e6d-ab0e-ce57e79a18a8.png

.. image:: https://user-images.githubusercontent.com/30430227/153522392-db35f09a-72c8-4c99-8131-12c8b1df0b59.png
.. image:: https://user-images.githubusercontent.com/30430227/153522436-b9746fd8-0b1e-41ad-9777-4d19bf531452.png

.. image:: https://user-images.githubusercontent.com/30430227/153522531-c5e747ec-fb1d-4ae0-8ae4-70b295606cca.png
.. image:: https://user-images.githubusercontent.com/30430227/153522583-54084354-b543-4624-abe6-56f358a69356.png

2. Session 기반 인증 방식

.. code-block:: 

    - 일반적으로 웹 서버는 HTTP. 즉, stateless 프로토콜을 사용하기 때문에 웹사이트에서 사용자가 로그인한 회원인지에 대한 인증을 관리하는 방안이 필요하다.
    - 세션이란 일정 시간 동안 같은 사용자(정확하게 브라우저를 말한다로 부터 들어오는 일련의 요구를 하나의 상태로 보고 그 상태를 일정하게 유지시키는 기술이라고 한다.
    즉, 방문자가 웹서버에 접속해 있는 상태를 하나의 단위로 보고 세션이라고 칭한다.


.. code-block:: 

    * Session과 Cookie의 차이점
    - 쿠키의 경우는 방문자의 정보를 방문자 컴퓨터의 메모리에 저장
    - 정보를 방문자 메모리에 저장하는 것이 아닌 웹 서버가 세션 아이디 파일을 만들어 서비스가 돌아가고 있는 서버에 저장
    - 세션은 Stateful 서버이다.
    - Session 저장 위치는 Memory, File, DB 다(Memory가 속도가 가장 빠르다..

.. code-block:: 

    * 작동방식
    브라우저. 사용자가 로그인을 요청하고(id, pw 전달
    서   버. 유효하다면, 세션이 서버의 메모리 상에 저장(SessionId 저장, sessionId를 cookie에 담아 브라우저로 전달
    브라우저.  모든 request에 cookie(sessionId를 함께 전송
    서   버. 브라우저가 보낸 sessionId를 키로 session 정보를 식별하고 유효하다면, 원하는 응답을 제공


    * 장점
    - 서버에서 클라이언트의 상태 확인이 용이, 클라이언트가 임의로 정보 변경 불가
    * 단점
    - 서버에서 클라이언트의 상태를 모두 유지하고 있어야 하므로 클라이언트 수에 따른 부하가 심하다.(확장성 떨어짐
    - 사용자가 많아지는 경우 세션의 관리가 어려워진다
    - 멀티 디바이스 환경(모바일, 브라우저 공동 사용 등에서 로그인 시 중복 로그인 처리가 되지 않음


3. JWT - Javascript Web Token

.. code-block:: 

    * 작동방식
    - 서버는 클라이언트의 정보를 저장하지 않고, JWT의 발급과 매 요청마다 header에 넘어오는 access token의 유효성 검사만 진행한다.
    - 클라이언트는 JWT를 local storage에 저장
    - 서버가 클라이언트의 정보를 저장하지 않으므로 Stateless 서버이다.


4. OAuth 2.0

``OAuth 2.0은 로그인하지 않고도 제삼자에게 서비스를 제공할 수 있도록 하는 표준 사용자 인증 프로토콜이다.``

.. code-block::

    - google, facebook 등과 같은 서비스의 계정으로 제3의 서비스에 로그인하여 등록되어 있는 정보나 해당 사이트들(google, facebook 등의 기능을 사용할 권한을 부여받는 표준 프로토콜이다.
    - OAuth 2.0은 HTTPS 환경에서만 작동한다.
    - token 인증 방식을 사용


Session 인증
------------

`참고사이트`<https://millo-l.github.io/Nodejs-passport-session-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0>`_

``npm install express-session memorystore session-file-store express-mysql-session``

1. Memory 세션

.. image:: https://user-images.githubusercontent.com/30430227/153786786-d2b858ad-61c2-47e6-a463-272763c11315.png

.. code-block:: console

    import express from "express";
    import { engine } from "express-handlebars";
    import path from "path";
    import { createRequire } from "module";

    const require = createRequire(import.meta.url;

    const session = require("express-session"; 
    const MemoryStore = require("memorystore"(session;

    // ES6 방식
    // import session from 'express-session' 해도 된다
    // import memorystore from 'memorystore'; const memoryStore = memorystore(session 해도 된다


    const __dirname = path.resolve(;
    const port = 3000;

    const app = express(;

    app.use(
    session({
        secret: "secret key",
        resave: false,
        saveUninitialized: true,
        store: new MemoryStore({
        checkPeriod: 86400000,
        },
        cookie: { maxAge: 86400000 },
    }
    ;

    app.use(express.static(__dirname;
    app.use((req, res, next => {
    next(;
    };

    app.get("/", (req, res => {
    console.log(req.session;
    if (req.session.num === undefined {
        req.session.num = 1;
    } else {
        req.session.num += 1;
    }
    res.send(``View: ${req.session.num}``;
    };

    app.listen(port, ( => {
    console.log(``The Server is Running on Port ${port}``;
    };



2. File 세션

.. image:: https://user-images.githubusercontent.com/30430227/153786933-fb1d8456-4580-42d9-8ca5-21ff5c711e41.png

.. code-block::

    - session의 데이터를 파일 형태로 디스크에 저장
    - DB보다는 속도가 빠르지만 memory 방식보다는 속도가 느리다. memory에 비해 디스크가 저장 공간이 훨씬 여유롭다는 장점
    - session.save( 세션이 저장된 후에 실행되는 함수(파일 저장 속도가 느려 반응이 늦을 경우

    const FileStore = require("session-file-store"(session;

    app.use(
    session({
        secret: "secret key",
        resave: false,
        saveUninitialized: true,
        store: new FileStore(,
    }
    ;

    // ES6 방식
    // import filestore from "session-file-store";
    // const FileStore = filestore(session;



``MySQL 세션``

.. code-block:: console

    import express from "express";
    const app = express(;

    import { engine } from "express-handlebars";

    import session from "express-session";

    // import filestore from "session-file-store";
    // const FileStore = filestore(session;

    import mysqlstore from "express-mysql-session";
    const MySQLStore = mysqlstore(session;

    // import { createRequire } from "module";
    // const require = createRequire(import.meta.url;

    // const FileStore = require("session-file-store"(session;

    import path from "path";
    const __dirname = path.resolve(;

    const port = 3000;

    import dotenv from "dotenv";
    dotenv.config(;

    app.engine(
    "hbs",
    engine({
        extname: "hbs",
    }
    ;

    const options = {
    host: "localhost",
    port: 3306,
    user: "root",
    password: "brush",
    database: "session_test",
    };

    app.set("view engine", "hbs";

    app.use(express.urlencoded({ extended: false };
    app.use(express.json(;

    app.use(express.static(__dirname;

    app.use(
    session({
        key: "session_cookie_name",
        secret: "283hehksfuse7@dfd", // 쿠기 정보, 알아보기 힘들게 작성한다
        resave: false, // true하면 변경사항이 없을 시에도 세션을 저장한다
        saveUninitialized: false, // 새로 생성된 세션에 아무 작업이 없을 경우도 저장한다
        store: new MySQLStore(options,
    }
    ;

    app.get("/count", (req, res => {
    if (req.session.count {
        req.session.count++;
    } else {
        req.session.count = 1;
    }
    res.send(``count : ${req.session.count}``;
    };

    app.get("/welcome", (req, res => {
    if (req.session.displayName {
        res.send(``
        <h1>Hello, ${req.session.displayName} </h1>
        <a href='/logout'>logout</a>
        ``;
    } else {
        res.render("home";
    }
    };

    app.get("/logout", (req, res => {
    console.log(req.session.displayName;
    //delete req.session.displayName;
    req.session.destroy(; // delete 와 같은 기능
    res.redirect("welcome";
    };

    const users = [];

    app.post("/register", (req, res => {
    const user = {
        username: req.body.username,
        password: req.body.password,
        displayName: req.body.displayName,
    };
    users.push(user;
    req.session.displayName = req.body.username;
    req.session.save(( => {
        //session.save( 세션이 저장된 후에 실행되는 함수
        console.log(users;
        res.redirect("/welcome";
    };
    };

    app.get("/register", (req, res => {
    res.render("register";
    };

    app.post("/login", (req, res => {
    const uname = req.body.username;
    const pwd = req.body.password;
    for (let i = 0; i < users.length; i++ {
        if (uname === users[i].username && pwd === users[i].password {
        req.session.displayName = users[i].displayName;
        return res.redirect("/welcome";
        }
    }
    res.send('Who are you? <a href ="/login">login</a>';
    };

    app.get("/login", (req, res => {
    res.render("login";
    };

    app.listen(port, ( => {
    console.log(``The Server is Running on Port ${port}``;
    };



3. Passport 세션

``sequelize 시퀄라이즈- nodejs에서 mysql을 쉽게 다룰 수 있도록 도와주는 라이브러리,ORM(Object-relational Mapping-SQL없이 DB사용``

.. code-block:: 

    특별한 점이 있다면 passport를 app.use(passport.initialize(해서 반드시 초기화를 해야 한다는 점이다. 물론 세션을 사용하기 때문에 app.use(passport.session(도 반드시 초기화해야 한다.
    - serializeUser란 로그인을 성공한 user의 정보를 session에 저장하는 함수이고,
    - deserializeUser는 페이지에 방문하는 모든 client에 대한 정보를 req.user 변수에 전달해주는 함수이다. 따라서, req.user로 해당 user가 로그인을 한 유저인지 또한 어떤 user인지에 대한 정보를 각각의 요청들에서 넘겨받을 수 있게 된다.


.. code-block:: console

    import express from "express";
    const app = express(;

    import passport from "passport";
    import localstrategy from "passport-local";
    const LocalStrategy = localstrategy.Strategy;
    import crypto from "crypto";

    import { engine } from "express-handlebars";

    import mysql from "mysql";
    import session from "express-session";
    import mysqlstore from "express-mysql-session";
    const MySQLStore = mysqlstore(session;
    //페이스북, 트위터 같은 소셜 로그인이 아니라 local에서 로그인 기능 구현을 위해 사용

    // import { createRequire } from "module";
    // const require = createRequire(import.meta.url;

    import path from "path";
    const __dirname = path.resolve(;

    const port = 3000;

    import dotenv from "dotenv";
    dotenv.config(;

    const connection = mysql.createConnection({
    host: process.env.DB_HOST,
    user: process.env.DB_USER,
    password: process.env.DB_PASS,
    database: process.env.DB_NAME,
    multipleStatements: true,
    };
    connection.connect((err => {
    if (!err {
        console.log("Connected";
    } else {
        console.log("Connection Failed";
    }
    };

    app.engine(
    "hbs",
    engine({
        extname: "hbs",
    }
    ;

    app.set("view engine", "hbs";

    // 사용자 쿠키 생성, 다음에 사용자가 사이트를 방문할 때 쿠키를 확인하고 세션ID와 유효한지 검사
    app.use(
    session({
        key: "session_cookie_name",
        secret: "session_cookie_secret",
        store: new MySQLStore({
        host: process.env.DB_HOST,
        port: port,
        user: process.env.DB_USER,
        database: "cookie_user",
        },
        resave: false,
        saveUninitialized: false,
        cookie: {
        maxAge: 1000 * 60 * 60 * 24,
        },
    }
    ;

    // Passport  초기화 및 session 연결
    app.use(passport.initialize(;
    app.use(passport.session(;

    app.use(express.urlencoded({ extended: true };
    app.use(express.json(;

    app.use(express.static(__dirname;

    // passport.serializeUser((user, done => done(null, user;

    // passport.deserializeUser(function (id, done {
    //   done(null, id;
    // };

    const customFields = {
    usernameField: "uname",
    passwordField: "pw",
    };

    //사용자 유효성 판단(사용자 로그인 시 호출, validPassword메서드 사용 해 MySQL id/pass와 비교한다
    const verifyCallback = (username, password, done => {
    connection.query(
        "select * from users where username =?",
        [username],
        (err, results, fields => {
        if (err return done(err;

        if (results.length == 0 {
            return done(null, false;
        }
        const isValid = validPassword(password, results[0].hash, results[0].salt;
        user = {
            id: results[0].id,
            username: results[0].username,
            hash: results[0].hash,
            salt: results[0].salt,
        };
        if (isValid {
            return done(null, user;
        } else {
            return done(null, false;
        }
        }
    ;
    };

    const strategy = new LocalStrategy(customFields, verifyCallback;
    passport.use(strategy;

    // serializeUser - 사용자의 정보 객체를 세션에 아이디로 저장
    passport.serializeUser((user, done => {
    console.log("inside serialize";
    done(null, user.id;
    };

    // deserializeUser - 세션에 저장한 아이디를 통해 사용자 정보 객체를 불러옴
    passport.deserializeUser(function (userId, done {
    console.log("deserializeUser" + userId;
    connection.query(
        "select * from users where id =?",
        [userId],
        (err, results => {
        done(null, results[0];
        }
    ;
    };

    //로그인 시 입력한 암호를 암호화하여 DB암호와 비교, 같으면 true 반환
    function validPassword(password, hash, salt {
    var hashVerify = crypto
        .pbkdf2Sync(password, salt, 10000, 60, "sha512"
        .toString("hex";
    return hash === hashVerify;
    }

    //암호화(사용자 등록 시 호출, 먼저 암호패키지를 사용해 암호 salt를 생성한다>암호salt를 사용해 암호에 대한 hash를 생성
    function genPassword(password {
    var salt = crypto.randomBytes(32.toString("hex";
    var genhash = crypto
        .pbkdf2Sync(password, salt, 10000, 60, "sha512"
        .toString("hex";
    return { salt: salt, hash: genhash };
    }

    // 사용자가 인증되었는지 여부 확인, false를 반환하면 '/notAuthorized' 경로로 리디렉션된다
    function isAuth(req, res, next {
    if (req.isAuthenticated( {
        next(;
    } else {
        res.redirect("/notAuthorized";
    }
    }

    // 사용자가 관리자인지 여부 확인
    function isAdmin(req, res, next {
    if (req.isAuthenticated( && req.user.isAdmin == 1 {
        next(;
    } else {
        res.redirect("/notAuthorizedAdmin";
    }
    }

    // 사용자 이름이 이미 데이터베이스에 있는지 확인, 존재하면 '/userAlreadyExists'로 그렇지 않으면 사용자를 등록한 다음'/login' 경로로 리디렉션
    function userExists(req, res, next {
    connection.query(
        "select * from users where username=?",
        [req.body.uname],
        (err, results, fields => {
        if (err {
            console.log("Error";
        } else if (results.length > 0 {
            res.redirect("/userAlreadyExists";
        } else {
            next(;
        }
        }
    ;
    }

    app.get("/", (req, res, next => {
    res.send("<h1>Home</h1><p>Please <a href='/register'>register</a>";
    };

    app.get("/login", (req, res, next => {
    res.render("login";
    };

    app.get("/logout", (req, res, next => {
    req.logout(;
    res.redirect("/protected-route";
    };

    app.get("/login-success", (req, res, next => {
    res.send(
        '<p>You successfully logged in. --> <a href="/protected-toute">Go to protected route</a></p>'
    ;
    };

    app.get("/login-failure", (req, res => {
    res.send("You entered the wrong id/password.";
    };

    app.get("/register", (req, res => {
    console.log("inside get";
    res.render("register";
    };

    app.post("/register", userExists, (req, res, next => {
    console.log("Inside post";
    console.log(req.body.pw;
    const saltHash = genPassword(req.body.pw;
    console.log(saltHash;
    const salt = saltHash.salt;
    const hash = saltHash.hash;

    connection.query(
        "insert into users(username,hash,salt,isAdmin values(?,?,?,0",
        [req.body.uname, hash, salt],
        (err, results, fields => {
        if (err {
            console.log("Error";
        } else {
            console.log("Successfully Entered";
        }
        }
    ;
    res.redirect("/login";
    };

    app.post(
    "/login",
    passport.authenticate("local", {
        failureRedirect: "/login-failure",
        successRedirect: "/login-success",
    }
    ;

    app.get("/protected-route", isAuth, (req, res, next => {
    res.send(
        '<h1>You are authenticated</h1><p><a href="/logout">Logout and reload</a></p>'
    ;
    };

    app.get("/admin-route", isAdmin, (req, res, next => {
    res.send(
        '<h1>You are admin</h1><p><a href="/logout">Logout and reload</a></p>'
    ;
    };

    app.get("/notAuthorized", (req, res, next => {
    console.log("Inside get";
    res.send(
        '<h1>You are not authorized to view the resource</h1><p><a href="/login">Retry Login</a></p>'
    ;
    };

    app.get("/notAuthorizedAdmin", (req, res, next => {
    console.log("Inside get";
    res.send(
        '<h1>You are not authorized to view the resource as you are not the admin of the page </h1><p><a href="/login">Retry to Login as admin</a></p>'
    ;
    };

    app.get("/userAlreadyExists", (req, res, next => {
    console.log("Inside get";
    res.send(
        '<h1>Sorry This username is taken</h1><p><a href="/register">Register with different username</a></p>'
    ;
    };

    app.listen(port, ( => {
    console.log(``The Server is Running on Port ${port}``;
    };


.. code-block:: console

    * register.hbs

    <div class="login">
        <h1>Register</h1>
        <form action="/register" method="post">
            <label for="username">
                <i class="bi bi-alarm"></i>
            </label>
            <input type="text" name="uname" placeholder="UserID" id="id">
            <label for="password">
                <i class="bi bi-mailbox2"></i>
            </label>
            <input type="password" name="pw" placeholder="Password" id="password">
            <small>Already a member ? <a href="/login">Go and log in</a> </small>
            <input type="submit" value="Register">
        </form>
    </div>

    * login.hbs
    <div class="login">
        <h1>Login</h1>
        <form action="/login" method="post">
            <label for="username">
                <i class="bi bi-alarm"></i>
            </label>
            <input type="text" name="uname" placeholder="UserID" id="id">
            <label for="password">
                <i class="bi bi-mailbox2"></i>
            </label>
            <input type="password" name="pw" placeholder="Password" id="password">
            <small>Not a member yet <a href="/register">Join us</a> </small>
            <input type="submit" value="Login">
        </form>
    </div>



Egoing Session
---------------

1. MultiUser 세션

``app.js``

.. code-block:: console

    import express from "express";
    const app = express(;

    import { engine } from "express-handlebars";

    import session from "express-session";

    // import filestore from "session-file-store";
    // const FileStore = filestore(session;

    import mysqlstore from "express-mysql-session";
    const MySQLStore = mysqlstore(session;

    // import { createRequire } from "module";
    // const require = createRequire(import.meta.url;

    // const FileStore = require("session-file-store"(session;

    import path from "path";
    const __dirname = path.resolve(;

    const port = 3000;

    import dotenv from "dotenv";
    dotenv.config(;

    app.engine(
    "hbs",
    engine({
        extname: "hbs",
    }
    ;

    const options = {
    host: "localhost",
    port: 3306,
    user: "root",
    password: "brush",
    database: "session_test",
    };

    app.set("view engine", "hbs";

    app.use(express.urlencoded({ extended: false };
    app.use(express.json(;

    app.use(express.static(__dirname;

    app.use(
    session({
        key: "session_cookie_name",
        secret: "283hehksfuse7@dfd", // 쿠기 정보, 알아보기 힘들게 작성한다
        resave: false, // true하면 변경사항이 없을 시에도 세션을 저장한다
        saveUninitialized: false, // 새로 생성된 세션에 아무 작업이 없을 경우도 저장한다
        store: new MySQLStore(options,
    }
    ;

    app.get("/count", (req, res => {
    if (req.session.count {
        req.session.count++;
    } else {
        req.session.count = 1;
    }
    res.send(``count : ${req.session.count}``;
    };

    app.get("/welcome", (req, res => {
    if (req.session.displayName {
        res.send(``
        <h1>Hello, ${req.session.displayName} </h1>
        <a href='/logout'>logout</a>
        ``;
    } else {
        res.render("home";
    }
    };

    app.get("/logout", (req, res => {
    console.log(req.session.displayName;
    delete req.session.displayName;
    // req.session.destroy(;
    res.redirect("welcome";
    };

    const users = [];

    app.post("/register", (req, res => {
    const user = {
        username: req.body.username,
        password: req.body.password,
        displayName: req.body.displayName,
    };
    users.push(user;
    req.session.displayName = req.body.username;
    req.session.save(( => {
        //session.save( 세션이 저장된 후에 실행되는 함수
        console.log(users;
        res.redirect("/welcome";
    };
    };

    app.get("/register", (req, res => {
    res.render("register";
    };

    app.post("/login", (req, res => {
    const uname = req.body.username;
    const pwd = req.body.password;
    for (let i = 0; i < users.length; i++ {
        if (uname === users[i].username && pwd === users[i].password {
        req.session.displayName = users[i].displayName;
        return res.redirect("/welcome";
        }
    }
    res.send('Who are you? <a href ="/login">login</a>';
    };

    app.get("/login", (req, res => {
    res.render("login";
    };

    app.listen(port, ( => {
    console.log(``The Server is Running on Port ${port}``;
    };


``register.hbs, home.hbs``

.. code-block:: console

    <div class="login">
        <h1>Register</h1>
        <form action="/register" method="post">
            <label for="username">
                <i class="bi bi-alarm"></i>
            </label>
            <input type="text" name="username" placeholder="UserID" id="id">
            <label for="password">
                <i class="bi bi-mailbox2"></i>
            </label>
            <input type="password" name="password" placeholder="Password" id="password">
            <input type="text" name="displayName" placeholder="displayName">
            <small>Already a member ? <a href="/login">Go and log in</a> </small>
            <input type="submit" value="Register">
        </form>
    </div>


.. code-block:: console

    <h1>Welcome</h1>
    <ul>
    <li><a href='/login'>Login</a></li>
    <li><a href='/register'>Register</a></li>
    </ul>

  <a href="/logout">logout</a>



암호화 
------

.. code-block::

    * 해시 - 암호를 암호화된 데이터로 변환
    * 다이제스트digest - 해시에 의해 암호화된 데이터
    * 단방향 해시 - 다이제스트의 복호화 즉 원본데이터를 구할 수 없는 해시함수(SHA, MD, HAS, WHIRLPOOL...
    * 동일한 암호명에는 동일한 다이제스트가 생성된다(단점
    * 단방향 해시 함수 보완 기법 - 키-스크레칭(다이제스트를 여러번 해싱한다, 솔트(해시함수를 돌리기 전에 임의 문자를 뿌리는 것


1. 비밀번호 암호화 하기(기본 - 같은 결과가 나온다(레인보우 방식

.. code-block:: console

    import crypto from "crypto";

    const createHashedPassword = (password => {
    return crypto.createHash("sha512".update(password.digest("base64";
    };
    //createHash: 알고리즘, update: 암호화할 비밀번호, digest: 인코딩방식
    console.log(createHashedPassword("1234";
    console.log(createHashedPassword("1234";
    console.log(createHashedPassword("1234";


2. 암호에 소금 뿌리기
