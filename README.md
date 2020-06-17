# Subprocess

Use subprocess in python for execute git commands.

## Usage

```python
import subprocess


lines = subprocess.check_output([
        'git', '--no-pager', 'log', '--pretty=format:', '--name-only',
        '--since="3 days ago"'
    ])


for path in lines.splitlines():
    print(path.decode("utf-8"))
```

## Results:

Shows the list of files changed 
