# Web Application for deploying neural net model on [Render](https://render.com)

The repository can be used as a starting point to deploy any model on Render.



The guide for production deployment :

*Fork this repository or clone the app/ folder into your Github account.
*Upload your trained model file
*Upload the trained model file created with learner.export (for example export.pkl) to a cloud service like Google Drive or Dropbox. *Copy the download link for the file.

*Note : the download link should start the file download directly—and is typically different from the share link (which presents you with a view to download the file).

Google Drive: [Use this link generator].(https://www.wonderplugin.com/online-tools/google-drive-direct-link-generator/)
Dropbox: [Use this link generator].(https://syncwithtech.blogspot.com/p/direct-download-link-generator.html)

*Edit the file server.py inside the app directory and update the export_file_url variable with the URL copied above. In the same file, update the line "classes" with the classes you expect from your model.

*Create a new Web Service on Render and use the repo you created above. 

Local testing
To run the app server locally, run this command in your terminal:
```
python app/server.py serve
```

If you have Docker installed, you can test your app in the same environment as Render’s by running the following command at the root of your repo:

Changes can be tested locally by installing Docker and using the following command:

```
docker build -t "repo-name" . && docker run --rm -it -p 5000:5000 "repo-name"
```

Go to http://localhost:5000/ to test your app.

Officially time to shift from Heroku to Render :

* Although being expedient, moving from AWS to Render eliminated a lot of infrastructure complexity.
* GCP recommended for students but compares nothing against AWS Services.

Choose wisely
