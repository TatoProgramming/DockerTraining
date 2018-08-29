# Run Command 
This covers the different args that can be used with the run command.
## -p: exposing ports

```bash
docker run -d -p 3030:80 nginx
```
*Break Down*:
 * -d: ran it in detatched
 * -p 3030:80: 3030 is the exposed port out side container and 80 is the port inside the container. The port 80 inside the container is exposed to the outside through port 3030
 * nginx: the container image

If you didn't have the image nginx then the image will be pulled from the docker repository. Example:

![port example](images/ce1.PNG)

using our container list command both of these command do the same thing
```bash
docker ps -a
docker container ps -a
```
![port example2](images/ce2.PNG)

When a name is not given to the container then it is given a random one like **priceless_goldwasser**

Then in a browser type in [http://localhost:3030/](http://localhost:3030/). You should be seeing this.

![port example3](images/ce3.PNG)

So lets stop the container then remove it, you can use the name or the ID of the container.
When using the ID you don't have to use the full ID just enough for it to know which container to stop.

```bash
// these do the same thing.
docker stop priceless_goldwasser // or
docker stop 685
```
By listing our containers we can see that priceless_goldwasser was stopped.
![port example4](images/ce4.PNG)

Now lets remove it.
```bash
docker rm 68
```
![port example5](images/ce5.PNG)

And if you list the containers again you should not see the container.

![port example6](images/ce6.PNG)

### Tip 
You can stop and remove multiple containers in one command.
![port example6](images/ce7.PNG)

Stop multiple

![port example6](images/ce8.PNG)

Remove  multiple

![port example6](images/ce9.PNG)

## --rm 
This will remove the container once it is stopped.
```bash
docker run -d -p 8080:80 --rm nginx 
```
then stop the container and list all containers. The one you made should be gone.do

![port example6](images/ce10.PNG)
![port example6](images/ce11.PNG)
![port example6](images/ce12.PNG)

## --name
This gives the container a name.
```bash
docker run -d --name frank nginx
```
![port example6](images/ce13.PNG)

## -it
This command connects the container to the terminal. I am using the --rm command to keep my containers clean.

```bash
docker run --rm -it ubuntu
```

You can now interact with the container and execute linux commands.
![port example6](images/ce14.PNG)

# Exec Command

