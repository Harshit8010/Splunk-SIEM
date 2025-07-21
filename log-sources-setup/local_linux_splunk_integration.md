# 🧾 Ingesting Local Linux System Logs via Systemd Journald Input for Splunk

This configuration uses the official Systemd Journald Input for Splunk app to ingest local Linux logs directly from journald into Splunk Enterprise.


## ⚙️ Step 1:

Splunk Enterprise (running on the same machine as the systemd journal

---

## ⚙️ Step 2: Configure the Journald Input

- Navigate to:

```
Settings > Data Inputs > Journald
```

![linux](../Screenshots/kalvm2.png)

- Add a new Journald input:

```
Name: journald_input --> Index: linux or any custom index --> Sourcetype: journald (or custom like linux:systemd)
```

![linux](../Screenshots/kalvm.png)

---
