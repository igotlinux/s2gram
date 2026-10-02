# s2gram

simple bash tool to ship terminal outputs file dumps and clipboard text straight into a telegram bot chat

handy when you are running a long server task or scan and want the notification on your phone instead of babysitting the terminal

## requirements

curl
telegram bot token from botfather
your telegram chat id

## install

```bash
git clone https://github.com/igotlinux/s2gram.git
cd s2gram
chmod +x s2gram.sh
sudo cp s2gram.sh /usr/local/bin/s2gram
```

set your bot token and chat id inside s2gram sh or export them in your env

## usage

pipe terminal output directly
```bash
tail -n 50 /var/log/nginx/access.log | s2gram
```

send a quick message
```bash
s2gram -t "backup finished successfully"
```

send a file
```bash
s2gram -f database_dump.sql.gz
```

send whatever is currently in your clipboard
```bash
s2gram -c
```

## license

mit
