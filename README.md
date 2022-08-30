# Setup collaborative MLflow with PostgreSQL as Tracking Server and MinIO as Artifact Store using docker containers
This is the repo for these blog posts:

* [My Website: Setup collaborative MLflow with PostgreSQL as Tracking Server and MinIO as Artifact Store using docker containers](http://www.sefidian.com/2022/08/30/setup-collaborative-mlflow-with-postgresql-as-tracking-server-and-minio-as-artifact-store-using-docker-containers/)
* [Medium](http://www.sefidian.com/2022/08/30/setup-collaborative-mlflow-with-postgresql-as-tracking-server-and-minio-as-artifact-store-using-docker-containers/)

## Preparing the environment

**Note**: I have tested the codes on __Linux__. It can certainly be run on Windows and MacOS with small modifications.

1. Clone the repository, and navigate to the downloaded folder.

```
git clone https://github.com/iamirmasoud/mlflow_postgres_minio.git
cd mlflow_postgres_minio
```

2. Create (and activate) a new environment, named `mlflow_env` with Python 3.7. If prompted to proceed with the
   install `(Proceed [y]/n)` type y.

   ```shell
   conda create -n mlflow_env python=3.7
   source activate mlflow_env
   ```

   At this point your command line should look something like: `(mlflow_env) <User>:mlflow_postgres_minio <user>$`.
   The `(mlflow_env)` indicates that your environment has been activated, and you can proceed with further package
   installations.
3. Install the prerequisites for building the `psycopg2` package from source on Ubuntu:

```shell
sudo apt install libpq-dev python3-dev
```

3. Install requirements for the environment:

```shell
pip install -r requirements.txt
```

4. Navigate back to the repo. (Also, your source environment should still be activated at this point.)

```shell
cd mlflow_postgres_minio
```
