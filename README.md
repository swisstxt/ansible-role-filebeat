# Ansible Role Filebeat

This role installes and configures `filebeat` (https://www.elastic.co/guide/en/beats/filebeat/current/index.html).
The role currestly only supports a few prospector settings as well as logstash output accouding to SWISS TXT requirements.

## Role Variables

``` yaml
# Specify the logstash settings
filebeat_logstash_server: logstash.example.com
filebeat_logstash_port: 5555

# Specify a input aka prospector
filebeat_inputs:
- document_type: icecast
  paths:
  - /var/log/streaming/*/*.log
  tail_files: true
```
