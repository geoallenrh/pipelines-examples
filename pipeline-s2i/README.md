# Tekton Pipelines Example - S2I Build

![Pipeline Diagram](images/pipeline.png)

Install demo:
```
$ oc new-project demo
$ oc apply -f fix
$ oc create -f pipeline-s2i/petclinic-pipeline-all.yaml
```

Start pipeline
```
$ tkn p start petclinic-deploy --use-param-defaults -w name=maven-cache,claimName=maven-cache-pvc -w name=app-source,claimName=app-source-pvc -w name=maven-settings,config=maven-settings
```