



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