# Docker Images

Coursera has base Docker images that you can use for labs. You can create your own image but you won't be able to use the built-in grader.

## Modifying Docker Image

You can pass in additional commands to modify the image. Docker commands are the same as that would go in a Dockerfile but won't include the first commands such as the `FROM` command.

### Considerations for Customizing Docker Image

When customizing the base Docker image, there are some hangups that you might want to consider.

#### Any additional files must downloaded via a link

There doesn't seem to be a way to include files that can be referenced for the additional Docker commands (customization from the base Docker image). The files can be downloaded via a URL however.

> NOTE: If you recreate/edit the image with the same URL, the Docker image will likely cache the URL download. If the files from the URL are different from another run but the URL is the same, the (new) files won't be downloaded if the Docker image build uses a cache.
> 
> You can check the build logs if the command used a cache. One solution is to delete the image and rerun. Another is modifying the command so that Docker doesn't use the cached command.