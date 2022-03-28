# debian-packages
Installation files required for elastic-ansible-debian


please download elastic packages from these links:
then rename filese and remove version and amd64, eg: kibana-8.1.1-amd64.deb => kibana.deb

https://artifacts.elastic.co/downloads/kibana/kibana-8.1.1-amd64.deb
https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-8.1.1-amd64.deb
https://artifacts.elastic.co/downloads/logstash/logstash-8.1.1-amd64.deb


https://artifacts.elastic.co/downloads/beats/winlogbeat/winlogbeat-8.1.1-windows-x86_64.zip

maybe these links didnot work for download amd64.deb after elastic version 8:
https://artifacts.elastic.co/downloads/auditbeat/auditbeat-8.1.1-amd64.deb
https://artifacts.elastic.co/downloads/packetbeat/packetbeat-8.1.1-amd64.deb
https://artifacts.elastic.co/downloads/filebeat/filebeat-8.1.1-amd64.deb
https://artifacts.elastic.co/downloads/metricbeat/metricbeat-8.1.1-amd64.deb

then you need to downlad them from other ways like :
``` bash
echo "deb https://artifacts.elastic.co/packages/8.x/apt stable main" | sudo tee -a /etc/apt/sources.list.d/elastic-8.x.list
apt update
rm -rf /var/cache/apt/archives/*

apt-get install  --download-only auditbeat
apt-get install  --download-only packetbeat
apt-get install  --download-only filebeat
apt-get install  --download-only metricbeat

cd /var/cache/apt/archives/*
ls
``