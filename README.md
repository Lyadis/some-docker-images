# some-docker-images

apache-php
```
docker run -d -p REAL_PORT:80 -v /path/to/my/dir:/app tutum/apache-php
```

sshd
```
docker run -p REAL_PORT:22 lyadis/sshd
```

type-inference
```
docker run -it -v path/to/my/project:/myProject lyadis/type-inference /bin/bash -c 'find /myProject/src/main -name "*.java" | xargs ./binary/javai-reim;mv infer-output/* /myProject/'
```


