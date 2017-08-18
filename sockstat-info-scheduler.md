vi delta-index-output.sh


```
echo -- DATE -- >> /home/ec2-user/delta-index.log
date >> /home/ec2-user/delta-index.log
echo -- NET Stat -- >> /home/ec2-user/delta-index.log
cat /proc/net/sockstat >> /home/ec2-user/delta-index.log
echo --END-- >> /home/ec2-user/delta-index.log
echo >> /home/ec2-user/delta-index.log
```

chmod +x delta-index-output.sh

./delta-index-output.sh

crontab -e

```
* * * * * /home/ec2-user/delta-index-output.sh
```

check scheduler
```
tail -f ./delta-index.log
```
