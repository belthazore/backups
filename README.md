
# Settings Backup installer

Бэкап настроек системы.
Не доработано создание бэкапа текущих настроек (этап распаковки).

```sh
## BASH
## The creation of a backup of the current system settings is not finalized.

cd /tmp/
wget https://github.com/belthazore/backups/blob/master/pack.7z
mkdir ~/backup_test
cd ~/backup_test
7z x /tmp/pack.7z
cp pack/* ~
rm /tmp/pack.7z
cd ..
rm -rf backup_test
```

- scripts.7z -> Скрипты создания и распаковки бэкапа
- pack.7z -> бэкап файлов

## Alias  

alias backupDo='cd ~/backup/container && ./pack.sh && cd ~'
