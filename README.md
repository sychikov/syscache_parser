# syscache_parser
# Парсер syscache и проверка хэшей по AV\TI

# Описание

В ОС Windows существует множество артефактов, оставляемых файлами и процессами. Одним из мест хранения таких артефактов является файл Syscache.hve, находящийся в папке “System Volume Information”, которая, в свою очередь, находится в корне примонтированного диска. В данном файле хранятся хеши SHA-1 файлов, с которыми производились какие-либо действия на системе.

# Что мы хотим

Необходимо разработать утилиту, которая будет:

1. Парсить Syscache.hve файл и получать оттуда хеши SHA-1 файлов
2. Искать эти хеши в публичных списках индикаторов компрометации, вредоносного ПО, фидах Threat Intelligence
3. Для обнаруженных совпадений выводить информацию об угрозе или ссылку на эту информацию

# Setup
pip3 install -r packages

# Usage
python3 SyscacheParser.py --path Syscache.hve

