<p align="center">
  <img src="" alt="Team logo"><br><br>
  <img src="" alt="aaa v7.16.0">&nbsp;
  <img src="" alt="license GPL-3.0">&nbsp;
  <img src="" alt="bbb v14.16.0">
</p>

# Team name

> 👩‍💼 Project vision... 'Team name' 👨‍💼

Project description<br>
...<br>
...<br>

[📖 Wiki 보러가기](wiki_link)



<h2>📋 Table of Contents</h2>
<details>
  <summary> </summary>
  <ul>
    <li><a href="#getting-started">Getting started</a></li>
    <ul>
      <li><a href="#prerequisites">Prerequisites</a></li>
      <li><a href="#installation-and-run">Installation & Run</a></li>
      <li><a href="#initial-configuration">Initial configuration</a></li>
    </ul>
    <li><a href="#project-architecture">Project architecture</a></li>
    <li><a href="#flow-chart">Flow chart</a></li>
    <li><a href="#features">Features</a></li>
    <ul>
        <li><a href="#client">Client</a></li>
        <li><a href="#manager">Manager</a></li>
    </ul>
    <li><a href="#maintainers">Maintainers</a></li>
    <li><a href="#links">Links</a></li>
    <li><a href="#license">License</a></li>
  </ul>
</details>

<h2 id="getting-started">🚀 Getting started</h2>

<h3 id="prerequisites">Prerequisites</h3>
<details>
  <summary> </summary>
- npm
  ```
  npm install npm@latest -g
  ```
- redis
  ```shell
  # Windows
  Download from https://github.com/tporadowski/redis
  # Mac
  brew install redis
  # Ubuntu
  sudo apt-get install redis-server
  ```
</details>

<h3 id="installation-and-run">Installation & Run</h3>
<details>
  <summary> </summary>
1. Clone the repository

   ```
   git clone https://github.com/coding-Benny/NTACT.git
   ```

2. Install NPM packages and run

    - 📱 client

      ```shell
      cd client
      npm install
      npm run start
      ```

    - 👔 manager

      ```shell
      cd manager
      npm install
      npm run start
      ```

    - 💻 server

      ```shell
      cd server
      npm install
      npm run start
      ```
</details>

<h3 id="initial-configuration">Initial Configuration</h3>
<details>
  <summary> </summary>
  <ul>
    <li>Client configuration: <code>client/src/config</code></li>
    <ul>
      <li>loginInfo.json</li>

```json
{
  "jwt_password": "Put your JWT password"
}
```

  <li>payment.json</li>

```json
{
  "imp_user_code": "Put your I'mport; franchisee identification code"
}
```

</ul>

<li>Manager configuration: <code>manager/src/Login</code></li>

- loginInfo.json

  ```json
  {
    "jwt_password": "Put your JWT password"
  }
  ```

<li>Server configuration: <code>server/src/config</code></li>

- db-config.json

  ```json
  {
    "development": {    
      "username": "Put your user name here",
      "password": "Put your password here",
      "database": "Put your database here",
      "host": "Put your host name here",
      "dialect": "mysql",
      "operatorsAliases": 0,
      "define": {
        "timestamps": false,
        "underscored" : true
      }  
    },  
    "test": {
      "username": "Put your username here",
      "password": "Put your password here",
      "database": "Put your database here",
      "host": "Put your host name here",
      "dialect": "mysql"
    },  
    "production": {
      "username": "Put your username here",
      "password": "Put your password here",
      "database": "Put your database here",
      "host": "Put your host name here",
      "dialect": "mysql"
    }
  }
  ```

- password-config.json

  ```json
  {
    "jwt_password" : "Put your JWT password"
  }
  ```

- payment-config.json

  ```json
  {
    "imp_key": "Put your REST API key",
    "imp_secret": "Put your REST API Secret key"
  }
  ```

- s3-config.json

  ```json
  {  
    "AWSAccessKeyId": "Put your AWS access key ID",
    "AWSSecretKey": "Put your AWS Secret key",
    "Bucket": "Put your bucket name"
  }
  ```

- Syncing database

    1. Create `server/sync-db.bat` file

       ```shell
       start cmd /c "npx sequelize-auto -h YOUR_HOST_NAME -d YOUR_DATABASE_NAME -u YOUR_USERNAME -x YOUR_PASSWORD -p YOUR_PORT_NUMBER -c YOUR_CONFIG_FILE_PATH -o YOUR_OUTPUT_DIRECTORY -C"
       @ECHO DB Sync Done!
       
       # Mac or Linux
       npx sequelize-auto -h ntactdb.c8obj2inxx2r.ap-northeast-2.rds.amazonaws.com -d ntactDB -u ntact -x qlalfqjsgh -p 3306 -c ./config/db-config.json -o ./models -C
       echo DB Sync Done!
       ```

    2. Run batch file

       ```shell
       cd server
       sync-db.bat
       
       # Mac or Linux
       cd server
       chmod u+x ./sync-db.bat
       ./sync-db.bat
       ```
    </ul>

</details>


<h2 id="project-architecture">🏗️ Project Architecture</h2>

<img src="https://github.com/coding-Benny/NTACT/blob/dev/images/NTACT-architecture.png" alt="Project Architecture" width="750">

<h2 id="flow-chart">🔍 Flow Chart</h2>

<img src="https://github.com/coding-Benny/NTACT/blob/dev/images/NTACT-flowchart.png" alt="Flow Chart" width="600">

<h2 id="features">🎈 Features</h2>
  <img src="" alt="screenshot_1">
  <img src="" alt="screenshot_2">
  ...<br><br>
  
<h2 id="maintainers">👩‍💻 Maintainers 👨‍💻</h2>

<table>
    <tr>
        <td align="center">
            <a href="https://github.com/truebliss">
                <img src="https://avatars.githubusercontent.com/u/68186349?v=4" width="75px;" alt="YeonJi Kim"/><br />
                <sub><b>김연지</b></sub>
            </a>
        </td>
        <td align="center">
            <a href="https://github.com/coding-Benny/NTACT/wiki/%5BMaintainer%5D-%EA%B9%80%EC%97%B0%EC%A7%80" title="role">📌 Role</a><br />
            <a href="https://github.com/coding-Benny/NTACT/commits/dev?author=truebliss" title="Code">📜 Commit Log</a>
        </td>
    </tr>
    <tr>
        <td align="center">
            <a href="https://github.com/jokbalkiller">
                <img src="https://avatars.githubusercontent.com/u/55704603?v=4" width="75px;" alt="JongGeun Park"/><br />
                <sub><b>박종근</b></sub>
            </a>
        </td>
        <td>
            <a href="https://github.com/coding-Benny/NTACT/commits/dev?author=jokbalkiller" title="Code">📜 Commit Log</a>
        </td>
    </tr>
    <tr>
        <td align="center">
            <a href="https://github.com/Coding-Benny">
                <img src="https://avatars.githubusercontent.com/u/51183274?v=4" width="75px;" alt="JeongHyeon Lee"/><br />
                <sub><b>이정현</b></sub>
            </a>
        </td>
        <td align="center">
          <a href="https://github.com/coding-Benny/NTACT/wiki/%5BMaintainer%5D-%EC%9D%B4%EC%A0%95%ED%98%84" title="role">📌 Role</a><br>
          <a href="https://github.com/coding-Benny/NTACT/commits/dev?author=coding-Benny" title="Code">📜 Commit Log</a>
        </td>
    </tr>
    <tr>
        <td align="center">
            <a href="https://github.com/reader-wh94">
                <img src="https://avatars.githubusercontent.com/u/68210266?v=4" width="75px;" alt="SuJin Choi"/><br />
                <sub><b>최수진</b></sub>
            </a>
        </td>
        <td align="center">
         <a href="https://github.com/coding-Benny/NTACT/wiki/%5BMaintainer%5D-%EC%B5%9C%EC%88%98%EC%A7%84" title="role">📌 Role</a><br />
         <a href="https://github.com/coding-Benny/NTACT/commits/dev?author=reader-wh94" title="Code">📜 Commit Log</a>       
        </td>
    </tr>
</table>

<h2 id="links">🔗 Links</h2>

<ul>
  <li>Repository: https://github.com/JJJJ-web/NTACT</li>
  <li>NTACT client's homepage: https://ntact.site ⛔</li>
  <li>NTACT manager's homepage: https://manager.ntact.site ⛔</li>
  <li>Video</li>
    <a href="https://www.youtube.com/watch?v=Jv8nx1BdveI&feature=youtu.be" target="_blank"><img src="http://img.youtube.com/vi/Jv8nx1BdveI/0.jpg" alt="NTACT's youtube thumbnail"></a>
</ul>


<h2 id="license">📝 License</h2>

The code in this project is licensed under [GPL-3.0](https://github.com/coding-Benny/NTACT/blob/dev/LICENSE) license.
See `LICENSE` for more information.
