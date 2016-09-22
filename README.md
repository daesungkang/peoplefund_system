# peoplefund_system


DISK / MEMORY 사용율 측정

sudo apt-get install unzip
sudo apt-get install libwww-perl libdatetime-perl

curl http://aws-cloudwatch.s3.amazonaws.com/downloads/CloudWatchMonitoringScripts-1.2.1.zip -O
unzip CloudWatchMonitoringScripts-1.2.1.zip
rm CloudWatchMonitoringScripts-1.2.1.zip
cd aws-scripts-mon

vi awscreds.template 
AWSAccessKeyId=
AWSSecretKey=

crontab 
* *     * * *   root    //home/ubuntu/aws-scripts-mon/mon-put-instance-data.pl --mem-avail --mem-util --mem-used --swap-util --swap-used --disk-path=/ --disk-space-avail --aws-credential-file=/home/ubuntu/aws-scripts-mon/awscreds.template
