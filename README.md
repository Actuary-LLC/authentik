# authentik
Modeled after https://github.com/brokenscripts/authentik_traefik

# Notes
was able to get postgres to write to the NFS share by adding no_root_squash to the unraid rules and changing the docker container to the root user
UNRAID
cat /etc/exports
"/mnt/user/postgres" -fsid=110,async,no_subtree_check *(rw,sec=sys,insecure,anongid=100,anonuid=99,no_root_squash)
