# jenkins-configuration-as-code-workshop

We will learn how to use Jenkins Configuration as Code (JCasC) [plugin](https://github.com/jenkinsci/configuration-as-code-plugin/releases) in this workshop.

Important to note that the examples included in this repository used for demonstration purposes only. Therefore, the included examples should not be used for any production deployments.

[Jenkins Configuration as Code Reference](http://localhost:8080/configuration-as-code/reference) is included with Jenkins whenever JCasC plugin is installed.

Note that **YAML is indentation sensitive**.

View [Jenkins Job DSL API](http://localhost:8080/plugin/job-dsl/api-viewer/index.html) reference page provided through Jenkins. As an alternative, view the [online](https://jenkinsci.github.io/job-dsl-plugin/) version.

### commands

```bash
cd exercise-a-foundation
make compose-up
make compose-ps
```

#### Get exact version of a given plugin name


```bash
PLUGIN_NAME="configuration-as-code"
curl \
    --show-error \
    --silent \
    https://api.github.com/repos/jenkinsci/$PLUGIN_NAME-plugin/releases/latest \
    | grep "tag_name" \
    | cut --delimiter ":" --fields 2,3 \
    | tr --delete '\"' \
    | tr --delete ',' \
    | sed -e 's/^[[:space:]]*//'

```

## License

[GNU General Public License v3.0](LICENSE)
