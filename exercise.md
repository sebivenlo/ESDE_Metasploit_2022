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


First try finding all open ports and the corresponding services:

<details>
  <summary>Spoiler warning</summary>
  
  Spoiler text. Note that it's important to have a space after the summary tag. You should be able to write any markdown you want inside the `<details>` tag... just make sure you close `<details>` afterward.
  
  ```javascript
  console.log("I'm a code block!");
  ```
  
</details>
