# WordPress-GCP-DockerCompose-Nginx
Aim - To deploy a Wordpress Site, On Docker and GCP
1. Create a VM instance on GCP for project named wordpress(choose your own name). I chose the free tier version the micro instance because of limited needs.
2. Changed the OS from default Debian to Ubuntu and make the disk size atleast 20gb.
3. Allow the HTTP and HTTPS request and create the instance.
4. now the instance is created, connect with SSH link
5. Since we created a micro instance we have very less ram, we can create a swap disk (its not recommended for the websites but for this project isnce the traffic will be low)
6. to create a swap file of 4GB
7. sudo fallocate -l 4G /swapfile
8. you can check it by command
9. ll
10. we need to use this as actual swap memory, so we need to change some permissions on this
11. sudo chmod 600 /swapfile
12. now if you do ll, you can see under the rw(read/write) coloum total allocated space
13. now we need to tell the system it is a swap
14. sudo mkswap /swapfile
15. to turn it on
16. sudo swapon /swapfile
17. since the VM doesnt have any text editors installed, so we need to install VIM
18. sudo apt install -y vim
19. now to make the swapfile permanent
20. sudo vi /etc/fstab
21. inside this file
22. /swapfile none swap sw 0 0
23. to check if it is working, close the terminal and restart the instance and connect again via SSH and run
24. top
25. you will see the swap space is still in the place 
