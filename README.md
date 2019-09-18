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

def which(name):
  path = os.environ.get('PATH')
  if path:
    for p in path.split(os.pathsep):
      p = os.path.join(p, name)
      if os.access(p, os.X_OK):
        return p

def increment_string(string):
  m = re.match(r'(.*?)(\d+)$', string)
  if m is None:
    return string + '-2'
  return m.group(1) + str(int(m.group(2)) + 1)
  
def get_mimetype(filename):
  file_executable is not None:
    rv = subprocess.Popen(['file', '-b', '-mime-type', filename],
      stdout=subprocess.PIPE,
      stderr=subprocess.PIPE).communicate()[0].strip()
    if rv:
      return rv
  return mimetypes.guess_type(filename)[0]
  
def line_parser(format):
  pass
  
class StreamProcessor(object):

  def __init__(self, format, stream):
    self.regex = re.compile(format)
    self.stream = stream
  
  def process(self, p):
    stream = getattr(p, self.stream)
    while 1:
      line = stream.readline()
      if not line:
        break
      match = self.regex.search(line)
      if match is not None:
        yield match.group(1)

class UnpackerBase(object):
  id = None
```

```
```

```
```


