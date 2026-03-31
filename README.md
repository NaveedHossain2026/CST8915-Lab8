# CST8915 Lab 8

**Student Name**: Naveed Hossain
**Student ID**: 0410818822 
**Course**: CST8915 Full-stack Cloud-native Development
**Semester**: Winter 2026

---

## Demo Video

🎥 [Watch Demo Video](https://youtu.be/0JBXmPROaMk)

---

### 1. MongoDB Persistence & Replica Set

To ensure MongoDB data persists even during pod failures, a StatefulSet with a volumeClaimTemplate was implemented. Each MongoDB pod has its own PersistentVolume (Azure Disk). If a pod is deleted its disk is not lost and is reattached when the pod comes back , ensuring that no data is lost. The deployment uses 3 replicas. This allows the database to run as a cluster. If one node fails, the remaining nodes continue serving requests, ensuring high availability therefore there should be zero downtime for the Pet Store application.

### 2. RabbitMQ Persistence

RabbitMQ also uses a StatefulSet with persistent storage. Data is stored in /var/lib/rabbitmq on a PersistentVolume. ​​Because data is stored on an external Azure Managed Disk, messages will not be lost during pod failures and any queued orders will be recovered as soon as the RabbitMQ application restarts. 




## Acknowledgments

I used Gemini to troubleshoot errors and resolve technical blockers during the lab.
