### Docker

App name
```
APP_NAME=my-django-app
```


tag and push the built image to IBM’s icr registry:
 ```
 REGISTRY=us.icr.io
docker tag ${APP_NAME}:latest ${REGISTRY}/${SN_ICR_NAMESPACE}/${APP_NAME}:latest
docker push ${REGISTRY}/${SN_ICR_NAMESPACE}/${APP_NAME}:latest
```

run the following command to deploy your app to Code Engine.

```
ibmcloud ce application create --name ${APP_NAME} --image ${REGISTRY}/${SN_ICR_NAMESPACE}/${APP_NAME}:latest --registry-secret icr-secret --port 8000
```

log
```
ibmcloud ce app logs --application ${APP_NAME}
ibmcloud ce app events --application ${APP_NAME}
```
If you get the message that the "my-django-app already exists....", please use the below command to update the app:

```
ibmcloud ce application update --name ${APP_NAME} --image ${REGISTRY}/${SN_ICR_NAMESPACE}/${APP_NAME}:latest --registry-secret icr-secret --port 8000
```
