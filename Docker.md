Ubuntu:

Sure, here are step-by-step instructions to install Docker on Ubuntu:

1. Update the package index:

   ```
   sudo apt update
   ```

2. Install the dependencies to allow apt to use a repository over HTTPS:

   ```
   sudo apt install apt-transport-https ca-certificates curl gnupg lsb-release
   ```

3. Add the Docker GPG key:

   ```
   curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
   ```

4. Add the Docker repository to your system:

   ```
   echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
   ```

5. Update the package index again to include the Docker packages:

   ```
   sudo apt update
   ```

6. Install the Docker engine:

   ```
   sudo apt install docker-ce docker-ce-cli containerd.io
   ```

7. Add your user account to the `docker` group:

   ```
   sudo usermod -aG docker $USER
   ```

8. Log out of your current session and then log back in for the group membership changes to take effect.
    reboot your sudo(sudo reboot)

9. Verify that Docker is installed correctly by running the `hello-world` container:

   ```
   docker run hello-world
   ```

10. If you want to use Docker Compose to define and run multi-container Docker applications, you can install it using the following commands:

    ```
    sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
    sudo chmod +x /usr/local/bin/docker-compose
    ```

    This will install Docker Compose version 1.29.2. You can check the latest version on the Docker Compose GitHub releases page.

That's it! You should now have Docker installed and ready to use on your Ubuntu system.



create a directory with a file named dockerfile without any extension

put the below text into dockerfile
"
# Use a base image
FROM ubuntu:latest

# Set the entry point command
ENTRYPOINT echo "Hello, World!"

"

build a docker container

``` docker build -t my-app . ```


run a docker container
``` docker run -p 8080:80 my-app ```


Windows:

create a directory 
  -create a file named "Docker" without any extension
  -write into that file:
    
    FROM ubuntu:latest
    CMD ["echo","Hello World"]
 
 build conatiner:
  ```
  docker build -t image_name .
  ```
  
  execute container:
  ```
  docker run --name container_name image_name
  ```
  
  stop conatiner:
  ```
  docker stop pythoncontainer
  ```
  
  display all containers:
  ```
  docker ps -a
  ```
