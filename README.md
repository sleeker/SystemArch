SystemArch
Docker compose file for;

Sabnzbd
Sonarr v4 (Development
Radarr
Lidarr

This will create 4 docker containers under 1 service. They can be started and stopped all at once.

Please note the shared paths. Please change accordingly or create paths. These should all be made and owned by the default user 
and have the corrosponding UID and GID reflected under the environment variable. 

Once installed the programs will be installed on the following ports

Sabnzbd  port 8080
Sonarr   port 8989
Radarr   port 7878
Lidarr   port 8686

Directory Structure

I have created /opt/htpc where I have placed this YAML file and all the config files for the listed programs


Program Directories

/opt/htpc..
/opt/htpc/docker-compose.yml                 This file
/opt/htpc/sonarr                             Linked to the sonarr Config Directory /config
/opt/htpc/radarr                             Linked to the radarr Config Directory /config
/opt/htpc/lidarr                             Linked to the lidarr Config Directory /config
/opt/htpc/sabnzbd                            Linked to the sabnzbd Config Directory /config


Media Directories 

In my case these are NFS shares mounted to the machine in the following directories

/mnt/store/tv
/mnt/store/movies
/mnt/store/music
/mnt/store/downloads/complete
/mnt/store/downloads/incomplete

On Ubuntu install docker compose and docker desktop

create directories as above or change this YAML file to suit and copy the docker-compose.yml into /opt/htpc
then;

cd /opt/htpc
docker compose pull
docker compuse up -d

Then log into the machine on the above ports and start your configuration. 
