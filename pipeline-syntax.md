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
- 