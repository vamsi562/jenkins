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