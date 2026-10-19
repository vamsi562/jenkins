# Jenkins Installation
```
        # Add the clean repo configuration file
    sudo curl -o /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/rpm-stable/jenkins.repo

    # Import the official Jenkins signing key
    sudo rpm --import https://pkg.jenkins.io/rpm-stable/jenkins.io-2026.key
    sudo yum install fontconfig java-21-openjdk -y

    # Install Jenkins
    sudo yum install jenkins -y

    sudo systemctl daemon-reload
    # Enable the service to start automatically on system boot
    sudo systemctl enable jenkins

    # Start the Jenkins engine
    sudo systemctl start jenkins

```

growpart /dev/nvme0n1 4
lvextend -L +15G /dev/mapper/RootVG-rootVol
lvextend -L +15G /dev/mapper/RootVG-homeVol
xfs_growfs /
xfs_growfs /home

## triggers

GITHUB SCM Trigger
http://<domain/ip>:8080/github-webhook/
