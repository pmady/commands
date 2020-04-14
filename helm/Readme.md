To get the repos 
``` helm repo list ```

To search repos
``` helm search <keyword> ```

To inspect chart
``` helm inspect <chartname> ```

``` helm fetch <chartname> ```

To package helm files
``` helm package <foldername> ```

To install helm chart
``` helm install <foldername> ```

To upgrade existing helm chart
``` helm upgrade <releasename> <chartfoldername> ```

To get the release name
``` helm list```

Rollback
``` helm rollback <releasename> <revision> ```

To get revision
``` helm history <releasename> ```

To check the status of helm release
``` helm status <releasename> ```

``` helm get <releasename> ```

To delete helm
``` helm delete <releasename> ```
