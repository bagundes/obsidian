---
share: "true"
---

### Hana Server
```bash
# Electronic Service
sudo firewall-cmd --permanent --zone=public --add-port=7299/tcp

# HANA services: 3xx15 (default value for the first tenant database) and 3xx40 to 3xx99 (for all tenant databases); 3xx13 for the system database (where xx represents the SAP HANA instance number)
sudo firewall-cmd --permanent --zone=public --add-port=30013/tcp
sudo firewall-cmd --permanent --zone=public --add-port=30015/tcp

# API Gateway Service
sudo firewall-cmd --permanent --zone=public --add-port=60000/tcp
sudo firewall-cmd --permanent --zone=public --add-port=60010/tcp

# System Landscape Directory
sudo firewall-cmd --permanent --zone=public --add-port=40000/tcp
sudo firewall-cmd --permanent --zone=public --add-port=40001/tcp

# Authentication Service
sudo firewall-cmd --permanent --zone=public --add-port=40020/tcp
sudo firewall-cmd --permanent --zone=public --add-port=40021/tcp

# SAP Start Services
sudo firewall-cmd --permanent --zone=public --add-port=50013/tcp
sudo firewall-cmd --permanent --zone=public --add-port=50014/tcp

# Web client
sudo firewall-cmd --permanent --zone=public --add-port=443/tcp

# App Framework
sudo firewall-cmd --permanent --zone=public --add-port=4300/tcp
sudo firewall-cmd --permanent --zone=public --add-port=8000/tcp

# Excel Report
sudo firewall-cmd --permanent --zone=public --add-port=39915/tcp

# Hana cockpit
sudo firewall-cmd --reload
```

