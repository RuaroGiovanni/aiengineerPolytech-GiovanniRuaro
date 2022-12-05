# Data Platform Foundation


## 0. Tooling

### 0.1 Kubeflow

Atos provides you some resources for this course

[Kubeflow](https://www.kubeflow.org/) is an open-source end to end ML orchestration toolkit. Cloud Native, it handles most of the ML practice  / frameworks and allow to create strong and reliable workflows to operate the entire lifecycle of ML applications.

For this course, you will accès Kubeflow UI, and uses the Kubeflow API's remotly.

Our focus will be on Kubeflow's subparts :

- Notebooks, that will be your workspace for the course
- [Kubeflow pipelines](https://www.kubeflow.org/docs/components/pipelines/v1/introduction/) --> **KFP**, the orchestrator. It creates and links containers (called components) to create a workflow (called pipeline).

- [Kserve](https://github.com/kserve/kserve) the model serving tool. It creates api endpoint and make a ML model accessible and queryable behind it

### 0.2 Other tools you will use 

Kubeflow is currently in integration in a bigger opensource ecosystem 
which is called **Atos Codex Data Platform - Atos CDP**

![codex](./images/codex.png)


### 1.0 Access Kubeflow UI

You will accès the platform UI with this URL [kubeflow.course.aiengineer.sandbox-atos.com](kubeflow.course.aiengineer.sandbox-atos.com). You will access it thru a personal profile `firstname-lastname`.

Clicking on the link you should be redirected to `iam.course.aiengineer.sandbox-atos.com`, where the identities are managed. Here you have to log in using : 

```
username : firstname-lastname 
mp : aiengineer-lastname
```

![iam](./images/iam.png)

Once you logged in, you will see Kubeflow home. Upper left your profile space (green on the screenshot), the **KFP - Kubeflow Pipeline** menu headings (red on the screenshot) and the **Model (Kserve)** menu heading (orange in the screenshot)

![home](./images/home.png)

### 1.1 Create a Notebook server

Click on "Notebooks" menu and "create" button, name it `nameInitials-aiengineer-labs  ex: Guillaume ETEVENARD --> ge-aiengineer-labs`, let the default ressources and in the "configuration" step, **check the "allow accès to kubeflow pipeline" box**.

Launch it, wait until it's available and connect to it.


Then, clone the [https://github.com/A709509/aiengineercourse](https://github.com/A709509/aiengineercourse) repo

```bash
git clone https://github.com/A709509/aiengineercourse
```

At this point, you will begin to write some code to interract with the platform.

**begin with the notebook** [0_data_get_analyse_and_ingest.ipynb](0_data_get_analyse_and_ingest.ipynb)

**For this notebook 0 you will need :**

- [https://min.io/docs/minio/linux/developers/python/API.html](https://min.io/docs/minio/linux/developers/python/API.html)
- [https://seaborn.pydata.org/](https://seaborn.pydata.org/)
- [https://pandas.pydata.org/docs/reference/index.html](https://pandas.pydata.org/docs/reference/index.html)

It will cover interactions between workspace and storage



**Once it's done and you learnt how to store data to minio, continue with**[1_empower_analysis_with_db_and_viz.ipynb](1_empower_analysis_with_db_and_viz.ipynb)

**For this notebook 1 you will need :**

 - [https://clickhouse.com/docs/en/sql-reference](https://clickhouse.com/docs/en/sql-reference)
 - [https://www.postgresql.org/docs/current/index.html](https://www.postgresql.org/docs/current/index.html)
 - [https://kafka-python.readthedocs.io/](https://kafka-python.readthedocs.io/)

 In this lab you will use different types of cold and hot storages. Also you will access an interface to vizualize data from those storages.