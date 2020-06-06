# ansible

Problem:
$ ./ec2.py3 --list
Traceback (most recent call last):
  File "./ec2.py3", line 1700, in <module>
    Ec2Inventory()
  File "./ec2.py3", line 260, in __init__
    self.read_settings()
  File "./ec2.py3", line 314, in read_settings
    config = configparser.ConfigParser(DEFAULTS)
  File "/usr/local/Cellar/python/3.7.6_1/Frameworks/Python.framework/Versions/3.7/lib/python3.7/configparser.py", line 638, in __init__
    self._read_defaults(defaults)
  File "/usr/local/Cellar/python/3.7.6_1/Frameworks/Python.framework/Versions/3.7/lib/python3.7/configparser.py", line 1216, in _read_defaults
    self.read_dict({self.default_section: defaults})
  File "/usr/local/Cellar/python/3.7.6_1/Frameworks/Python.framework/Versions/3.7/lib/python3.7/configparser.py", line 753, in read_dict
    self.set(section, key, value)
  File "/usr/local/Cellar/python/3.7.6_1/Frameworks/Python.framework/Versions/3.7/lib/python3.7/configparser.py", line 1197, in set
    self._validate_value_types(option=option, value=value)
  File "/usr/local/Cellar/python/3.7.6_1/Frameworks/Python.framework/Versions/3.7/lib/python3.7/configparser.py", line 1182, in _validate_value_types
    raise TypeError("option values must be strings")
TypeError: option values must be strings

Resolution: 
https://github.com/ansible/ansible/pull/43716#issuecomment-418348101

The resolution has been applied in ec2.py.