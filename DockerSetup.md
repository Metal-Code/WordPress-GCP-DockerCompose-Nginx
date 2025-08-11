to install docker 
1. in the SSH terminal
2. curl https://get.docker.com > install-docker.sh
3. chmod 755 install-docker.sh
4. sudo ./install-docker.sh
5. to run docker as a non-root user
6. sudo usermod -aG docker your_name (for me it was ayush15807) so
7. sudo usermod -aG docker ayush15807
8. now close the terminal and open the SSH terminal again
9. docker container ls
10. now to install docker compose,
11. sudo curl -l "https://github.com/docker/compose/releases/download/1.23.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
12. to give executable permisson
13. sudo chmod 755 /usr/local/bin/docker-compose
14. to check the installation and version
15. docker-compose --version
16. 
