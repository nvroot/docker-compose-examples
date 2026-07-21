# Gocd

<p align="left">
  <img src="../logo/gocd.svg" width="100" height="100">
</p>

| Name | Description |
|----------------|--------|
| **Used Image** |   gocd/gocd-server:v24.3.0   |
| **Description** |  —  |
| **Website** | —    |
| **Docs** |    —    |
| **Registry** |    https://hub.docker.com/r/gocd/gocd-server   |
| **Source&nbsp;Code&nbsp;** |   —  |
| **Port** |    8153   |
### **Under the hood**

The GoCD server runs as the `go` user, the location of the various directories is:

| **Directory** | **Description** |
| --- | --- |
| `/godata/artifacts` | the directory where GoCD artifacts are stored |
| `/godata/config` | the directory where the GoCD configuration is stored |
| `/godata/db` | the directory where the GoCD database and configuration change history is stored |
| `/godata/logs` | the directory where GoCD logs will be written out to |
| `/godata/plugins` | the directory containing GoCD plugins |
| `/home/go` | the home directory for the GoCD server |
