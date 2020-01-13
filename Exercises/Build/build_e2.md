# Exercise #2

## Developing code and leaveraging docker to do it!

### Preface: Most dev's like to be able to write code and rapidly test it or debug it in "near real time". This write then run, write then run; may work well on there local system but it can get complacated when new dependancys get added or the dev system is not the same as prod or even user etc. Containers can be used to "set up" the execution envirnment as it's percieved by the process. This means a dev can setup a dev env "within a container" and use it to write then run; write then run vwery rappidly and be confident that the same container and code will "run" correctly in another envirnment.
### In this exercise you have a small webapp you are building for Kernelcon, we are going to use [Docker Compose](https://docs.docker.com/compose/compose-file/) to start our dev env. so we can easily do our work. This is a VERY common setup (way more common then you may think!).

If you have not already done so. make sure to _login_ to the class docker registry
```
# echo "Roxx3znazUWqjL56yoSz" | docker login --username denver.cfman@gmail.com --password-stdin registry.gitlab.com
```
Note: Yes thats a read-only user token (we will talk about this later)

#### Here we go ...

- Change directory so you are in the __<REPO_ROOT>/Exercises/Build/Files/build_e2/__ directory.
- do a ```ls``` command to make sure, should see:
```
about.html      build_e2.yml    dsvw.py     index.html
```
this is your development directory, "you know where you keep your code"; now we can make use of [Docker Compose](https://docs.docker.com/compose/compose-file/) to "spin up" our development envirnment.
- run the docker-compose command with our defnition file.
```
docker-compose -f build_e2.yml up -d
```
This will start up a docker container with our app running inside it, now go navagate your web browser to view it.
You can do this in many ways, but two come to mind. Use either your "host" browser or make use of the firefox browser within kali linux.

TO use your host browser, you will need to find your kali linux IP with a command comething like this:
![ifconfig eth0](Files/images/kali_ifconfig.jpg)
or just find it via the ```ifconfig eth0``` command.
Or again make use of the firefox browser within kali linux:
![kali firefox](Files/images/kali_firefox.jpg)