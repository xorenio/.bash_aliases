# .bash_aliases
Place for all the useful aliases


## Screen + <3


### WinSCP
sudo passwdless WinSCP (Half built)

```bash
$ alias winscp='[[ ! $(screen -ls | grep -q "winscp") ]] && $(screen -dmS "winscp" sudo winscp)'
```


## ffmpeg

### To MP3

```bash
$ alias tomp3='for f in *.m4a; do ffmpeg -i "$f" -codec:v copy -codec:a libmp3lame -q:a 2 "${f%.m4a}.mp3"; done'
```

## DNS

### Arch

```bash
$ alias showmydns='( nmcli dev list || nmcli dev show ) 2>/dev/null | grep DNS'
```


## Memcache

### Clear

```bash
$ alias memcached-clear='echo "flush_all" | nc -q 2 localhost 11211'
```


## MyTop

```bash
$ alias dc-mytop='mytop -h 127.0.0.1 -u root -p password'
```

## Net-tools


### ports
```bash
$ alias ports='netstat -lnF4'
```
