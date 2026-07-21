### **Installing plugins**

All plugins can be installed under `/godata`.

### **Installing plugins using an environment configuration**

To install plugins, just add an ENV variable with the prefix `GOCD_PLUGIN_INSTALL_` and your name as `suffix` and the value being the download URL. The plugin will only be downloaded if not yet present.

An example example would be `GOCD_PLUGIN_INSTALL_docker-elastic-agents=https://github.com/gocd-contrib/docker-elastic-agents/releases/download/v0.8.0/docker-elastic-agents-0.8.0.jar`:

`docker run \
  -e GOCD_PLUGIN_INSTALL_docker-elastic-agents=https://github.com/gocd-contrib/docker-elastic-agents/releases/download/v0.8.0/docker-elastic-agents-0.8.0.jar \
  gocd/gocd-server:v25.1.0`

To install multiple plugins, add several `-e` arguments as such:

`docker run \
  -e GOCD_PLUGIN_INSTALL_a-plugin=https://example.com/a-plugin.jar \
  -e GOCD_PLUGIN_INSTALL_b-plugin=https://example.com/b-plugin.jar \
  gocd/gocd-server:v25.1.0`

### **Installing plugins using a custom entry-point script (see below)**

`mkdir -p /godata/plugins/external
curl --location --fail https://example.com/plugin.jar > /path/to/godata/plugins/external/plugin.jar
chown -R 1000 /godata/plugins/external`

### **Loading configuration from existing git repo**

To load existing configuration from git repo, just add an ENV variable `CONFIG_GIT_REPO`. Auth token may be used to access private repo. Branch `master` would be cloned by default. To load another branch, define an ENV variable `CONFIG_GIT_BRANCH`. If `/godata/config` already is git repo then CONFIG_GIT_REPO will be ignored. Cloned repo **must** contain all files from `/godata/config` dir.

`docker run \
  -e CONFIG_GIT_REPO=https://gocd_user:<password_or_auth_token>/config.git \
  -e CONFIG_GIT_BRANCH=branch_with_config \
  gocd/gocd-server:v25.1.0`