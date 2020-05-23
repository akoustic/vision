# Web Application for deploying neural net model on [Render](https://render.com)

The repository can be used as a starting point to deploy any model on Render.

Guide for production deployment :

* Fork this repository or clone the app/ folder into your Github account.
* Upload your trained model file.
* Upload the trained model file created with learner.export (for example export.pkl) to a cloud service.
* Edit the file server.py inside the app directory and update the export_file_url variable with the URL copied above. In the same file, update the line "classes" with the classes you expect from your model.
* Create a new Web Service on Render and use the repo you created above. 

Local testing : 
  To run the app server locally, run this command in your terminal:
```
python app/server.py serve
```

  Changes can be tested locally by installing Docker and using the following command:

```
docker build -t "repo-name" . && docker run --rm -it -p 5000:5000 "repo-name"
```

Officially time to shift from Heroku to Render :

* Although being expedient, moving from AWS to Render eliminated a lot of infrastructure complexity.
* GCP recommended for students but compares nothing against AWS Services.

Choose wisely
