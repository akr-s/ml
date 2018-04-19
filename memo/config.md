# コンフィグ
## configparser
```
[Default]
error_log = True

[Server]
ip = 127.0.0.1
port = 80
```

```python
import configparser
config = configparser.ConfigParser()

config['Default'] = {
     'error_log':True
}

config['Server'] = {
     'ip':'127.0.0.1',
     'port':80
}

with open('config.ini','w') as config_file:
  config.write(config_file)
```
``` python
import configparser
#読み込み
config = configparser.ConfigParser()
config.read('config.ini')

print(config['Server'])
print(config['Server']['ip'])
```
