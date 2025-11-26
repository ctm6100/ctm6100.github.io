# CTM6100 GitHub.io Docker Setup

This repository contains a Hexo-based static site, configured to run in a Docker container using `docker-compose`.

## Prerequisites
- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Usage

### 1. Clone the repository
```sh
git clone https://github.com/ctm6100/ctm6100.github.io.git
cd ctm6100.github.io
```

### 2. Start the Hexo server
```sh
docker-compose up
```
This will:
- Build and start a container using the official Node.js 18 image
- Mount your repository into the container at `/app`
- Expose port 4000 for local access

### 3. Access the site
Open your browser and go to:
```
http://localhost:4000
```

### 4. Stop the server
Press `Ctrl+C` in the terminal, or run:
```sh
docker-compose down
```

## Development
Any changes made to the files in your local repository will be reflected inside the running container, thanks to the volume mount in `docker-compose.yml`.

## Customization
- To change the port, edit the `ports` section in `docker-compose.yml`.
- To install additional Node.js packages, use `docker-compose exec hexo npm install <package>`.

## Troubleshooting
- If you encounter permission issues, try running Docker with elevated privileges.
- For more advanced configuration, refer to the [Hexo documentation](https://hexo.io/docs/) and [Docker Compose docs](https://docs.docker.com/compose/).
