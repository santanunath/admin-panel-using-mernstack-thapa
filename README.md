### created by: thapa

## Tech stack (client/frontend)

- "react": "^18.2.0",
- "react-dom": "^18.2.0",
- "react-icons": "^4.12.0",
- "react-router-dom": "^6.20.0",
- "react-toastify": "^9.1.3"


## Tech stack (server/backend)
- "bcryptjs": "^2.4.3",
- "cors": "^2.8.5",
- "dotenv": "^16.3.1",
- "express": "^4.18.2",
- "jsonwebtoken": "^9.0.2",
- "mongoose": "^7.6.3",
- "nodemon": "^3.0.2",
- "zod": "^3.22.4"

## How to run the server (backend) application

```bash
$ cd server
$ cp dot-env .env
$ npm install   
$ npm run start    
   
now the backend application is running at 
http://localhost:5000 (or)
http://host-ip:5000   
    
(my RPi host-ip is 192.168.0.102)
it may be different for your system.
```
(Note: always run the backend application first. here 'server.js' is the main program which defines the PORT number,eg.5000)    
all api routes are defined in folder 'router'.    
all api busuness logic are defined in folder 'controllers'.   
> WARNING!! u have to specify frontend URLs in cors allowedOrigin in file 'server.js', otherwise frontend cannot access the backend.
      
## How to run the client (frontend) application

```bash
$ cd client   
$ cp dot-env .env    
$ npm install   
$ npm run dev     
```
(Note: frontend is created using 'vite')   
the main program file is /client/src/App.jsx    
     
----
## How to run the application inside Docker container


First, clone the repository:   
(private repo requires username, password)

```bash
$ git clone <repository url>
$ cd server
$ cp dot-env .env
$ cd ..
$ cd client
$ cp dot-env .env
$ cd ..
```



Start the application 

```bash
$ sudo docker-compose up -d
$ sudo docker ps (list running containers)
$ sudo docker logs <container-name> (it is optional)
```

for server(backend)app Open    
http://localhost:5000    
(or)     
http://host-ip:5000    
with your browser to see the result.
   
    
for client(frontend)app Open    
http://localhost:5173    
(or)     
http://host-ip:5173    
with your browser to see the result.

    
## How to Stop/remove the application

```bash
$ sudo docker-compose down
$ sudo docker ps
$ sudo docker system prune -a 
$ cd ..
$ sudo rm -r <application-directory-name>
$ ls -l
```
