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

sudo growpart /dev/nvme0n1 4
sudo lvextend -L +15G /dev/mapper/RootVG-rootVol
sudo lvextend -L +15G /dev/mapper/RootVG-homeVol
sudo xfs_growfs /
sudo xfs_growfs /home

## triggers

GITHUB SCM Trigger
http://<domain/ip>:8080/github-webhook/


## docker
dnf -y install dnf-plugins-core
dnf config-manager --add-repo https://download.docker.com/linux/rhel/docker-ce.repo
dnf install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y
systemctl start docker
systemctl enable docker
usermod -aG docker ec2-user