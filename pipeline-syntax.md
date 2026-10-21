# jenkins pipeline

- file name should start with **Jenkinsfile**

```
        pipeline {
            agent any

            stages {
                stage('Hello') {
                    steps {
                        echo 'Hello World'
                    }
                }
            }
        }
```

## jenkins plugins

**settings -> plugins -> install from here**

- stage view -> show piplelines in stages
- Pipeline Utility Steps
- aws steps
- sonarqube scanner
- ansicolor (add under options in jenkins pipeline only then we can access)
**Note** - for some plugins after installing restart jenkins using ***systemctl restart jenkins***