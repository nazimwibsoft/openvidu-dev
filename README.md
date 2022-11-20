# openvidu-dev
OpenVidu Dev Container Implementation and Configuration

OpenVidu On Premises mentions a dev container which developers can use to setup a dev instance for development of openvidu app.
https://docs.openvidu.io/en/stable/deployment/ce/on-premises/

I have summarized a docker compose config which would use the openvidu dev container and the openvidu calling app to setup an instance to get started.

## Setting up the container
1. Clone the repo in a folder
2. Use folloing commands to start or stop the containers
3. Start Container: docker-compose up -d
4. Stop and Remove Containers: docker-compose down

## Testing the instance
1. In your browser hit: http://localhost:4443/ to get the openvidu server page
2. Go to http://localhost:4443/dashboard/ to access the openvidu server dashboard for testing the instance
3. Go to http://localhost:5442/ to access the openvidu calling app, which will allow creating sessions and joining for realtime calls
