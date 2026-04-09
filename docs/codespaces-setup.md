# codespace_jenkins
Install Jenkins on Github Codespace:
Install Jenkins :

1. **Check the java version**: `java --version`
2. **Update the package**: `sudo apt update`
3. **If java is not install then install it**: `sudo apt instal default-jdk`
4. **Download Jenkins Package (from jenkins docs)**: 
```bash
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \\
  <https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key>
echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \\
  <https://pkg.jenkins.io/debian-stable> binary/ | sudo tee \\
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins

```
5. **Install Dependencies**: If there are any missing dependencies, install them. `sudo apt-get install -f`
6. **Start the jenkins service**: sudo service jenkins start
7. **Enable the jenkins**: sudo service jenkins enable
8. **Check status**: sudo service jenkins status

<aside>
💡 On git codespace , to start the jenkins server we have to forward the port to 8080 to make it accessible
</aside>
