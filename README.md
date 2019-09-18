### unp
---
https://github.com/mitsuhiko/unp

```py
// unp.py

FILENAME = object()
OUTPUT_FOLDER = object()
unpackers = []

def register_unpacker(cls):
  unpackers.append(cls)
  return cls
  
def fnmatch(pattern, filename):
  filename = os.path.basename(os.path.normcase(filename))
  pattern = os.path.normcase(pattern)

```

```
```

```
```


