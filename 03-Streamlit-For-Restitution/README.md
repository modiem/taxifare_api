# Streamlit

We will learn how to simply setup an app for Data visualisation and restitution.
this will be usefull for you projects on the weeks to come.

# Introduction

## Exercice
Before everything let us install the requirements provided inside `requirements.txt`
```bash
pip install -r requirements.txt
```
Now run:
```bash
streamlit run app_streamlit.py
```
Now inspect `app_streamlit.py`  and check what is being done inside

# Deploy
Now that you checked your app works locally, you might want it to run free on a remote server.

## Create folder outside data-challenges
Here as heroku is based on git, we will create a folder outside our gitted `data-challenges` folder.
```bash
mkdir -p ~/code/<user.github_nickname>/taxifare_streamlit
cp -rf * ~/code/<user.github_nickname>/taxifare_streamlit
cd ~/code/<user.github_nickname>/taxifare_streamlit
```
Version it for future heroku use:
```bash
cd ~/code/<user.github_nickname>/taxifare_streamlit && git init
```

## Deploy to heroku
You'll see once again how heroku is easy to use, here you simply need to:
- Create a `Procfile` with following line inside it:
```bash
web: sh setup.sh && streamlit run app_streamlit.py
```
```bash
git add . && git commit -am "add streamlit app"
```

- login to heroku
```bash
heroku login
```

- create app on heroku
```bash
heroku create YOUR_APP_NAME
```

- Build it on heroku servers using git
```bash
git push heroku master
```
- Then deploy
```bash
heroku ps:scale web=1
```
click on the link `https://YOUR_APP_NAME.herokuapp.com/` to visualize your app

# Useful links

- [Altair](https://altair-viz.github.io/gallery/)


