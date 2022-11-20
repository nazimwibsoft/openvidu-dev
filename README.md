# OpenVidu-dev
OpenVidu Dev Container Implementation and Configuration

OpenVidu On Premises mentions a dev container which developers can use to setup a dev instance for development of OpenVidu app.
https://docs.OpenVidu.io/en/stable/deployment/ce/on-premises/

I have summarized a docker compose config which would use the OpenVidu dev container and the OpenVidu calling app to setup an instance to get started.

## Setting up the container
1. Clone the repo in a folder
2. Use following commands to start or stop the containers
3. Start Container: docker-compose up -d
4. Stop and Remove Containers: docker-compose down

## Testing the instance
1. In your browser hit: http://localhost:4443/ to get the OpenVidu server page
2. Go to http://localhost:4443/dashboard/ to access the OpenVidu server dashboard for testing the instance
3. Go to http://localhost:5442/ to access the OpenVidu calling app, which will allow creating sessions and joining for real time calls

## Reference

https://docs.openvidu.io/en/stable/deployment/ce/on-premises/

https://hub.docker.com/r/openvidu/openvidu-dev

https://hub.docker.com/r/openvidu/openvidu-call

## Documentation on Recording

https://docs.openvidu.io/en/stable/advanced-features/recording/#for-openvidu-development-docker-container

https://docs.openvidu.io/en/stable/reference-docs/openvidu-config/#special-conditions-of-openvidu-development-container

https://docs.openvidu.io/en/stable/components/openvidu-call/#configuration-parameters-for-openvidu-call-backend

https://docs.openvidu.io/en/stable/advanced-features/recording/#2-configure-custom-layouts-in-openvidu-server

## OpenVidu Recording
When recording is enabled in the OpenVidu-dev server config as per documentation, it automatically downloads a video recording docker image openvidu/openvidu-recording on first startup.  When OpenVidu server starts a recording it will automatically launch an instance of recording container per session, so for each session a separate container is automatically started for session recording and after recording is complete it is disposed.
