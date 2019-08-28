# Type-inference

This image is merely a wrapper for [type-inference](https://github.com/proganalysis/type-inference)

In order to find the list of pure methods in a java project, run:
```
docker run -it -v path/to/my/project:/myProject lyadis/type-inference /bin/bash
```

Then inside your container:

```
find /myProject/src/main -name "*.java" | xargs ./binary/javai-reim
mv infer-output/* /myProject/
```
