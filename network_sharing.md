# File sharing

## File sharing with scp
The same as cp, but for remote files.

```bash
$ scp [-i | -r | -P | -v] <source> <destination>
```

- -i : identity file (private key, default: ~/.ssh/id_rsa)
- -r : recursive
- -P : port (default: 22)
- -v : verbose

```bash
$ http-server -p 8080
```

```bash
$ scp -v -P 8080 $USER@localhost:/public/favicon.ico .
```
```bash
$ scp -v -P 8080 README.md $USER@127.0.0.1:.
```
```bash
$ scp -v -P 8080 $USER@$(hostname):/favicon.ico .
```

## File sharing with rsync
The same as `scp`, but `rsync` is more powerful.

```bash
$ rsync [-a | -v | -z | -P | -e] <source> <destination>
```

- -a : archive mode
- -v : verbose
- -z : compress
- -P : progress
- -e : specify the remote shell to use

```bash
$ rsync -v -P -e "ssh -p 8080" $USER@localhost:/favicon.ico basic_command
```