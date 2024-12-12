# OPA
[ncc_group](https://research.nccgroup.com/2021/02/17/cryptopals-exploiting-cbc-padding-oracles/)
ON KALi
```
apt update
```
```
apt install -y docker.io
```

```
docker pull ubuntu:20.04
```
```
docker run -itd --privileged   --name OraclePadAttack ubuntu:20.04 
```
```
docker exec -it OraclePadAttack bash
```
```
apt update 
```
```
apt install python3-pip nano
```
```
pip install PyCryptoDome
```
```
nano full_attack.py
```
```
nano oracle_pad.py
```
```
python3 oracle_pad.py
```
```
exit
```
```
docker exec -it OraclePadAttack python3 oracle_pad.py
```
```
docker commit OraclePadAttack oraclepadattack:v1
```
```
docker image save oraclepadattack:v1 -o oraclepadattack.tar.gz
```
# LOAD AND RUN ! 
```
docker load  -i oraclepadattack.tar.gz
```
```
docker run -itd --privileged   --name OraclePadAttack oraclepadattack:v1 
```
```
docker exec -it OraclePadAttack python3 oracle_pad.py
```
