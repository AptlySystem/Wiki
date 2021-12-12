# Docker Images

Coursera has base Docker images that you can use for labs. You can create your own image but you won't be able to use the built-in grader.

## Modifying Docker Image

You can pass in additional commands to modify the image. Docker commands are the same as that would go in a Dockerfile but won't include the first commands such as the `FROM` command.