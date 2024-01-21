## Socket.io Admin UI


>[!IMPORTANT]
>This project is taken from [socket.io-admin-ui](https://github.com/socketio/socket.io-admin-ui). But there the ui(client) side does not work locally. 
It doesn't support Node versions higher than 14.21.3 and npm versions higher than 6.14.18 . Is not compatible with higher versions of sass library.
<br>

**I have fixed dependencies and creation of the docker container.**

* ### Running in localhost

You can easily start the project by following these steps;


>[!NOTE]
>You should downgride Node version on your computer.
>
>```
>nvm install 14.21.3
>nvm use 14.21.3
>nvm list
>
>```
>

Finally, you can run the project using `npm install` and `npm run serve`

* ### Docker Container

I have update dockerfile and added nginx.conf file with help from this [pull-request](https://github.com/socketio/socket.io-admin-ui/pull/74).  
You can create a docker container using the following commands;

```
docker build -t admin-ui .

docker run -d -p 8080:8080 admin-ui 
```
<br>

![dashboard screenshot](https://github.com/socketio/socket.io-admin-ui/blob/develop/assets/dashboard.png)

