# ログ
## logging

```python
import logging

# ログレベルを変更する
logging.basicConfig(level=logging.INFO)

# formaterを指定してログ出力のテンプレを変更できる。
formatter = '%(levelname)s:%(message)s'
logging.basicConfig(level=logging.INFO, format=formatter)

# ファイルに出力するとき
logging.basicConfig(filename='sample.log', level=logging.INFO)

#　ログレベル毎に出力する。
logging.critical('critical')
logging.error('error')
logging.warning('warning')
logging.info('info')
logging.debug('debug')
logging.info('info %s', 'logginig message')
```


# logger

loggingは起動時にトップレベルの階層でのみ実施して、
個別のログはloggerを使うようにしたほうが良いらしい。  


```python
from logging import getLogger
logger = getLogger(__name__)
logger.setLevel(logging.DEBUG)
logger.debug('debug')
```
