## Deploying on Heroku using heroku-cli
<details>
    <summary><b>Click here for more details</b></summary>

- Install [Heroku cli](https://devcenter.heroku.com/articles/heroku-cli)
- Login into your heroku account with command:
```
heroku login
```
- Create a new heroku app:
```
heroku create appname
```
- Select This App in your Heroku-cli: 
```
heroku git:remote -a appname
```
- Change Dyno Stack to a Docker Container:
```
heroku stack:set container -a appname
```
- Add Private Credentials and Config Stuff:
```
git add -f credentials.json token.pickle config.env heroku.yml
```
- Commit new changes:
```
git commit -m "Added Creds."
```
- Push Code to Heroku:
```
git push heroku master --force
```
- Restart Worker by these commands,You can Do it manually too in heroku.
- For Turning off the Bot:
```
heroku ps:scale worker=0 -a appname
```
- For Turning on the Bot:
```
heroku ps:scale worker=1 -a appname		
```

</details>
