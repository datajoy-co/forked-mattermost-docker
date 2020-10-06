# Getting Started

1. Get the ID of your current shell user with this command `id -u $(whoami)`
2. In docker-compose.yml under the app service replace 502 with the ID of your current shell user.
3. Run `docker-compose build`
4. Run this command to create folders that will be shared with the virtual machines that Mattermost is running on `mkdir -pv ./volumes/app/mattermost/{data,logs,config,plugins,client-plugins}`
5. Run this command `sudo chown -R $(whoami) ./volumes` to make your current shell user the owner of the shared folders you just created.
6. Run `docker-compose up -d` to start Mattermost.
