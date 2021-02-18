# Conda env demo

A small project to demonstrate how to manage conda environments using a
`environment.yml` file to enable easily reproducible environments.

## Demo

1. `conda env list`
1. `conda env create -f environment.yml`
1. `conda env list`
  * Note that a new environment has been created called `flask_server`, which
    is the name of the environment defined in `environment.yml`.
1. `conda activate flask_server`
1. `FLASK_APP=app.py flask run`
1. `curl localhost:5000`
  * Alternatively open `localhost:5000` in your web browser of choice
1. Kill the flask server with `ctrl + c`
1. `conda deactivate` to switch back out of `flask_server` to the default conda
   environment.

## Relevant Docs
* [Conda environments][condaEnvs]
* [Managing environments][managingEnvs]
* [Creating an environment file manually][createEnvFile]
* [Conda channels][condaChannels]


[condaChannels]: https://docs.conda.io/projects/conda/en/latest/user-guide/concepts/channels.html
[condaEnvs]: https://docs.conda.io/projects/conda/en/latest/user-guide/concepts/environments.html
[createEnvFile]: https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#create-env-file-manually
[managingEnvs]: https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html
