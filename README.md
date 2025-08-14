# Netdata_demo
DAY-7



# Netdata Monitoring Setup via Docker

A step-by-step guide to install and run Netdata for system resource monitoring using Docker.

## 🐳 Step 1: Run Netdata Container


        docker run -d --name=netdata \
            -p 19999:19999 \
            --cap-add SYS_PTRACE \
            --security-opt apparmor=unconfined \
            netdata/netdata

🌐 Step 2: Access the Dashboard

Open in browser:

        http://localhost:19999

📦 Step 3: Check if the Container is Running

        docker ps -a | grep netdata

🔁 Step 4: Restart Container if Already Exists

        docker start netdata

📝 Step 5: View Netdata Logs

Enter the container:

        docker exec -it netdata bash

Then run:

        cd /var/log/netdata
        ls -l
        cat error.log

🧪 Step 6: Explore Real-time Metrics

CPU, Memory, Disk Usage
Docker Container Stats
Network I/O and more

🚫 Step 7: Stop & Remove the Container (If Needed)

        docker stop netdata
        docker rm netdata

