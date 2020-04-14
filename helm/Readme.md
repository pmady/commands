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


```
Available Commands:
  completion  Generate autocompletions script for the specified shell (bash or zsh)
  create      Create a new chart with the given name
  delete      Given a release name, delete the release from Kubernetes
  dependency  Manage a chart's dependencies
  fetch       Download a chart from a repository and (optionally) unpack it in local directory
  get         Download a named release
  help        Help about any command
  history     Fetch release history
  home        Displays the location of HELM_HOME
  init        Initialize Helm on both client and server
  inspect     Inspect a chart
  install     Install a chart archive
  lint        Examines a chart for possible issues
  list        List releases
  package     Package a chart directory into a chart archive
  plugin      Add, list, or remove Helm plugins
  repo        Add, list, remove, update, and index chart repositories
  reset       Uninstalls Tiller from a cluster
  rollback    Rollback a release to a previous revision
  search      Search for a keyword in charts
  serve       Start a local http web server
  status      Displays the status of the named release
  template    Locally render templates
  test        Test a release
  upgrade     Upgrade a release
  verify      Verify that a chart at the given path has been signed and is valid
  version     Print the client/server version information

```
