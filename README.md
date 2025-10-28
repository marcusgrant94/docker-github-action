
This repo builds a Docker image on each push to `main` and pushes to Docker Hub as:
`marcusg2/is436:<github run number>`
docker pull marcusg2/is436:<tag>
docker run -d -p 8080:80 --name is436 marcusg2/is436:<tag>
