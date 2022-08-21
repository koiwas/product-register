This is my learning content for CI/CD pipeline.

# product-register

“product-register” is a tutorial of CI/CD Pipeline with Docker, Github, Travis CI, and HEROKU.

![CI_CD Pipeline](https://user-images.githubusercontent.com/111184429/185740408-436cfefb-f5e5-48a8-8403-4297433e2309.png)

# Description

* **What is CI/CD Pipeline?** - CI/CD is a widely used software engineering practice that combines continuous integration (CI) processes with continuous delivery (CD) or continuous deployment (CD) processes to accelerate the development and deployment of software applications. CI/CD practices help development and operations teams accelerate time-to-market, improve quality and reduce costs by automating the software build, test, delivery and deployment functions and eliminating manually intensive, error-prone processes.

* **Advantages of Docker in CI/CD** - With the help of a Docker, we can build a container image and can further use that same image over every step of the deployment process. The advantage of it is the ability to separate non-dependent steps and also run them in parallel. In addition, the duration of time it takes from build to production may speed up notably.


# Useage

## Github

1. Clone this repository

```
$ git clone https://github.com/koiwas/product-register.git
```

2. Create new repository on GitHub and get URL

3. Change Remote Repo URL & Push
```
$ git remote set-url origin {new_repo_url}
```
```
$ git remote -v
```
```
$ git push origin master
```

## Local

1. Go into the Local Repo
```
$ cd product-register
```

2. Create & Run Container
```
$ docker-compose up --build -d
```
```
$ docker-compose ps
```

3. Go into the Container
```
$ docker-compose exec web bash
```

4. Start Rails Server
```
$ rails s -b 0.0.0.0
```

5. If you want to check or modify the code
```
$ code .
```

6. Exit the Container
```
$ exit
```

7. If you want to terminate the Container
```
$ docker-compose down
```

## Travis CI

1. Sync with Github account

## HEROKU

1. Create new app, for example {name}-product-register

2. Add Heroku Postgres

3. Connect to Github

4. Enable Automatic deploys (Wait for CI to pass before deploy)

5. ADD Config Vars
```
SECRET_KEY_BASE：master.key
```

6. Install HEROKU CLI

7. ADD Environment Variables
```
HEROKU_USERNAME：_
HEROKU_API_KEY： result of $heroku authorizations:create
HEROKU_APP_NAME：{name}-product-register
```
