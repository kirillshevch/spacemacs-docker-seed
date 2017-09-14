#### spacemacs-docker seed repository

##  Usage

```bash
ip=$(ifconfig en0 | grep inet | awk '$1=="inet" {print $2}')
xhost + $ip
docker run -ti --name spacemacs-kirillshevch \
 -e DISPLAY=$ip:0 \
 -e TZ=UTC \
 -v ~/workspace/:/mnt/workspace \
 spacemacs/emacs25:develop
```

##### Content:
  - `private` - same as https://github.com/syl20bnr/spacemacs/tree/master/private
  - `.spacemacs` - All configs (except user) are set here
  - `Dockerfile` - Here you can add extra software, change user, etc.

##### Read [spacemacs-docker distribution README](https://github.com/syl20bnr/spacemacs/blob/develop/layers/%2Bdistributions/spacemacs-docker/README.org) for the details on build/usage.
