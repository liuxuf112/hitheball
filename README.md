frontend page
https://github.com/liuxuf112/hitheball-backend

backend page
https://github.com/liuxuf112/hitheball-backend



## frondend:

frontend is using flutter as development tool. The map is using google map api, and the api key is from previous CTF team.

#### To run frontend, 
1. download code from github and open in visual studio
2. download android emulator from android studio, flutter, download anything that visual studio remind
3. select any file in /lib/pages press f5 



#### To edit,
1. /lib contain all design screen, class, and helper function. 
2. the backend is host in heroku, after you create you own host on heroku, change the host name in /lib/utils/services/get_hostname.dart
3. some important page is create_game_screen, home_screen, in_game_screen, map_screen.
4. there are lost of un-used code from previous, you can remove them all.
5. most async functon is sending request to backend to receive, update from the database.
6. new backend function is update in the /utlis/services http_request.dart




## Backend:

backend is hosting on the heroku, using sql as database. All the code is to receive frontend http call and execute in sql. It takes github repo and hosting it. 

####set up backend environment
1. create account and project, link with backend github repo, then change the hostname in frontend
2. download procfile, https://devcenter.heroku.com/articles/procfile
3. follow this website setup sql on local https://devcenter.heroku.com/articles/heroku-postgresql
4. this link may help when you set up https://devcenter.heroku.com/articles/getting-started-with-nodejs
5. after everything setup, in command line enter "heroku pg:psql" will start the database on local mechine.
6. there may have some bug because the orignal sql table in create_tables.sql, you can update databse on you local 
 
#### To edit,
1. in /db, create or find function that you need
2. to exports a function, add into /db/dbExports.js so the backend can get frontend message
3. in the README in backend repo, theres document explain most of the function from the previous CTF team

# overvall
if there enough time, I strongly suggest start from the begining because there too much un-used code from previous team, and the code is really messy. there are some tip to start from begining
1. the whole process is fronend get, send, update from backend, the way keep them communicate is the hostname on heroku, and the http calls.
2. about google map api, reading document from google is the best way. https://developers.google.com/maps/documentation
3. the code is really messy, because there are too many verification, you can skip in the begin.
4. it will be the best if you taken cs492 and cs493
5. use andorid studio to development frontend is a good option 
6. keep everything simply