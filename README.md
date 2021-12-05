# ccm_env
A Vagrant env to quickly launch a ccm environment

# Quick Start

```bash
vagrant up
vagrant ssh
ccm create test -v 4.0.1 -n 6 -s
export PATH="$PATH:$HOME/.ccm/repository/4.0.1/bin/"
nodetool status --port7100
nodetool ring --port 7100
```


