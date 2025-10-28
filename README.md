This project demonstrates automated Docker deployment using GitHub Actions.  
Every time I push to the `main` branch, GitHub Actions:

1. Logs into Docker Hub using encrypted secrets
2. Builds a Docker image from the Dockerfile
3. Tags the image using the GitHub run number
4. Pushes the image automatically to Docker Hub

The image can then be pulled onto any machine running Docker.

## Result
Docker Hub: https://hub.docker.com/r/marcusg2/is436  
Tag pushed: `1`

To run locally:
```bash
docker pull marcusg2/is436:1
docker run -d -p 8080:80 --name is436 marcusg2/is436:1

