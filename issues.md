## Jenkins issues

* Built node offline
    
    - if space less than 1 gb, where jenkins present i.e /var/lib/jenkins
    - extend volume of var vol to more than 1ogb or higher
    - restart jenkins service
    - again refresh jenkins dashboard

* docker sock issue
- pipeline failed with error **ERROR: permission denied while trying to connect to the docker API at unix:///var/run/docker.sock**
 fix - 
    ``` 
    sudo usermod -aG docker jenkins
    sudo systemctl restart jenkins
    ```
    ```
    sudo chmod 666 /var/run/docker.sock
    ```
