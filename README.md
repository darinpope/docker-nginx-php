# docker-nginx-php

based on https://x-team.com/blog/docker-compose-php-environment-from-scratch/

review https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/create_deploy_docker_v2config.html#create_deploy_docker_v2config_dockerrun under "for an instance with two containers" to see how to run on Elastic Beanstalk.

Papertrail Integration
https://help.papertrailapp.com/kb/configuration/configuring-centralized-logging-from-docker/#logspout


docker run --restart=always -d \
    -v=/var/run/docker.sock:/var/run/docker.sock gliderlabs/logspout  \
    syslog+tls://logsN.papertrailapp.com:XXXXX

 logs7.papertrailapp.com:33346    