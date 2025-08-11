# WordPress-GCP-DockerCompose-Nginx

Aim - To deploy a Wordpress Site, On Docker and GCP

1. Create a VM instance on GCP for project named wordpress(choose your own name). I chose the free tier version the micro instance because of limited needs.

2. Changed the OS from default Debian to Ubuntu and make the disk size atleast 20gb.

3. Allow the HTTP and HTTPS request and create the instance.

4. Now the instance is created, connect with SSH link.

5. Since we created a micro instance we have very less ram, we can create a swap disk (its not recommended for the websites but for this project since the traffic will be low).

6. To create a swap file of 4GB:
```bash
sudo fallocate -l 4G /swapfile
```

7. You can check it by command:
```bash
ll
```

8. We need to use this as actual swap memory, so we need to change some permissions on this:
```bash
sudo chmod 600 /swapfile
```

9. Now if you do ll, you can see under the rw(read/write) column total allocated space.

10. Now we need to tell the system it is a swap:
```bash
sudo mkswap /swapfile
```

11. To turn it on:
```bash
sudo swapon /swapfile
```

12. Since the VM doesnt have any text editors installed, so we need to install VIM:
```bash
sudo apt install -y vim
```

13. Now to make the swapfile permanent:
```bash
sudo vi /etc/fstab
```

14. Inside this file add:
```
/swapfile none swap sw 0 0
```

15. To check if it is working, close the terminal and restart the instance and connect again via SSH and run:
```bash
top
```

16. You will see the swap space is still in the place.
