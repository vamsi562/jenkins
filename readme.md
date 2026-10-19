# Jenkins Installation
```
    sudo curl -o /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/rpm-stable/jenkins.repo
    # Add required dependencies for the jenkins package
    sudo rpm --import https://jenkins.io
    sudo yum install fontconfig java-21-openjdk -y
    sudo yum install jenkins -y
    sudo systemctl daemon-reload
    sudo systemctl enable jenkins
    sudo systemctl start jenkins
    sudo systemctl status jenkins
```