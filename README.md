# some-docker-images

## apache-php
Out of the shelf php server
```
docker run -d -p REAL_PORT:80 -v /path/to/my/dir:/app tutum/apache-php
```

## sshd
Out of the shelf ssh server
```
docker run -p REAL_PORT:22 lyadis/sshd
```

## openvpn
Out of the shelf openvpn server
See [here](https://github.com/kylemanna/docker-openvpn)

## type-inference
list pure method in a java project
```
docker run -it -v path/to/my/project:/myProject lyadis/type-inference /bin/bash -c 'find /myProject/src/main -name "*.java" | xargs ./binary/javai-reim;mv infer-output/* /myProject/'
```

## arduino-yun-cross-compiler
Cross compile c code for the arduino yun MIPS
See [here](https://hub.docker.com/r/lyadis/arduino-yun-cross-compiler/)
