# Web Application for deploying the neural net model on [Render](https://render.com)

The repository can be used as a starting point to deploy any model on Render.

Changes can be tested locally by installing Docker and using the following command:

```
docker build -t aiSight . && docker run --rm -it -p 5000:5000 aiSight
```

The guide for production deployment :
