# ecs-esproxy
Simple NGINX container to proxy requests to an AWS ElasticSearch Domain.


## Overview
This container is targeted for use inside a VPC against a ES domain which is restricted by IP to the VPC nat gateway IP.  A shortcut for the Kibana plugin is available at /kibana/

## Configuration
Use ES_ENDPOINT and ES_SCHEME to control where and how Nginx will connect to the AWS ElasticSearch domain.

## Example Run
docker run -it --rm -p 80:80 -e ES_ENDPOINT=search-my-domain.my-region.es.amazonaws.com -e ES_SCHEME=https infra-esproxy

Test with curl -v http://localhost:80/
