### Pip install

## Issue: No space left on device ERROR: Could not install packages due to an EnvironmentError.

This happens because of limited space of  **/tmp** directory, which is used for *pip install* to store tempoary packages.

## Solution

```python
$ echo "export TMPDIR=bigSpaceDisk/tmp" >> ~/.bashrc
$ source ~/.bashrc
```

