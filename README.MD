## Create folder to save configuration and data
* for example we will save it in `~/gitlab-docker`

* then assign the path to .bashrc/.zshrc depending on your shell

```
# setup gitlab docker home
export GITLAB_HOME=~/gitlab-docker
```

* restart terminal or type `source ~/.zshrc` or `source ~/.bashc`

* confirm with `echo $GITLAB_HOME` should output the path to gitlab-docker folder

## Spin up the docker compose
* run `docker compose up` and let it sit for a while before the apps is ready

* open browser and go to `http://localhost:5080` the gitlab instance should display a login screen

## Generate initial root password
* for the initial login use username `root` and use the password that is generated from the below command

`docker exec -it gitlab grep 'Password:' /etc/gitlab/initial_root_password`