# Creating the Docker images for the E4S project from ECP

## Building the Docker images
To build the Docker images from these files for the CPU based E4S image, type the following command in this directory:

```
docker-compose build
```

This will create two Docker images:
- e4s-spack-bricks:cpu
- e4s-spack-bricks:cuda

If you wish to use a different image name you may use the Docker "tag" command:

```
docker tag e4s-spack-bricks:<variant> <your-new-image-name>
```

This is necessary only if you expect to push your image build to Docker Hub. If you don't expect to push this image, stick with the default image names.

## Using the Docker image
You can start a Docker container using your new image with this command:

```
docker run -it --name=<your-container-name> e4s-spack-bricks:<variant>
```

This will put you at a command prompt where you may begin using the Bricks library as built by Spack!

Have fun!
