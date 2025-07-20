# 🔐 Wazuh Integration with Splunk via Universal Forwarder

This document explains how logs were forwarded from the Wazuh server (running on CSI Linux) to Splunk Enterprise using the Splunk Universal Forwarder (UF).

---

## ⚙️ Step-by-Step Setup

### 1. Splunk Indexer configuration

Splunk Indexer needs to be setup to receive logs before installing and configuring universal forwader on wazuh host. To configure the indexer you need to set a receiving port and create a index.

#### Configuring Receiving Port

- Go to Settings > Forwarding and receiving.

- Under Receive data, click Add new.

- Enter `9997` in the Listen on this port input box and click Save.

![siem](Screenshots/wazuhport.png)


#### Configuring Indexer

- Go to Settings > Indexes > New Index.

- Enter wazuh-alerts in Index name and click Save.






### 1. Install Splunk Universal Forwarder

```bash
wget -O splunkforwarder.tgz 'https://download.splunk.com/products/universalforwarder/releases/9.2.1/linux/splunkforwarder-9.2.1-<build>.tgz'
tar -xvzf splunkforwarder.tgz
cd splunkforwarder
sudo ./splunk start --accept-license
