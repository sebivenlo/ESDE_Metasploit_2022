run both commands in seperate windows. 

To run the instance of metasploitable 

docker run \
    -it \
    --network vulnerable \
    --ip="10.0.0.3" \
    --name metasploitable \
    --hostname metasploitable2 \
    tleemcjr/metasploitable2 \
    bash


sudo docker run \
    --name parrot \
    -it \
    --hostname parrot \
    --network vulnerable \
    --ip="10.0.0.2" \
    --env DISPLAY=$DISPLAY \
    -v /dev/shm:/dev/shm \
    --device /dev/snd \
    --device /dev/dri \
    --mount type=bind,src=/tmp/.X11-unix,dst=/tmp/.X11-unix \
    parrotsec/security:latest \
    /bin/bash


First try to start the metasploit console:

<details>
  <summary>Hint</summary>
  
  ```javascript
  msfconsole
  ```
  
</details>

Now try finding all open ports and the corresponding services:

<details>
  <summary>Hint</summary>
  
  ```javascript
  nmap -sV 10.0.0.3
  ```
  
</details>

Further more try to proceed by using one or more of the found services.
To avoid further spoilers possible attack vectors will be explained in solutions.md