# awesome-list

My Awesome List of anything cool that my curious mind finds interesting

- [Ansible](#ansible)
- [Awesome Lists](#awesome-lists)
- [CI/CD](#continious-integration)
- [Data Science](#data-science)
- [Docker](#docker)
- [DynamoDB](#dynamodb)
- [Elasticsearch](#elasticsearch)
- [Environment Setups](#environment-setups)
- [Epic Github Repos](#epic-github-repos)
- [Golang](#golang)
- [Grafana](#grafana)
- [Great Blogs](#great-blogs)
- [Knowledge Base](#knowledge-base)
- [Kubernetes](#kubernetes)
  - [Kubernetes Storage](#kubernetes-storage)
- [Machine Learning](#machine-learning)
- [Monitoring](#monitoring)
- [MongoDB](#mongodb)
- [Programming](#programming)
- [Queues](#queues)
- [Self Hosting](#self-hosting)
  - [Email Server Setups](#email-server-setups)
  - [Mailscanner Server Setups](#mailscanner-server-setups)
- [Serverless](#serverless)
- [Sysadmin References](#sysadmin-references)
- [VPN](#vpn)
- [Web Frameworks](#web-frameworks)

## Ansible
- [Kubernetes on LXC with Ansible](https://github.com/zimmertr/Bootstrap-Kubernetes-with-LXC)

## Awesome Lists
- [Awesome ChatOps](https://github.com/exAspArk/awesome-chatops)
- [Awesome Scalability](https://github.com/binhnguyennus/awesome-scalability)
- [Awesome Drone](https://github.com/drone/awesome-drone)

## Epic Github Repos
- [mlabouardy](https://github.com/mlabouardy?tab=repositories)

## Authentication
- [Nginx ES and Kibana Proxy with LDAP](https://mapr.com/blog/how-secure-elasticsearch-and-kibana/)

## Data Science
- [bulutyazilim - datascience awesome list](https://github.com/bulutyazilim/awesome-datascience)

## Grafana
- [Grafana Dashboards @mlabouardy](https://github.com/mlabouardy/grafana-dashboards)

## Docker

#### Deploy Stacks to your Swarm: :whale: :heart:

Logging:

- [shazChaudhry Swarm GELF Stack](https://github.com/shazChaudhry/docker-elastic)

Metrics:

- [StefanProdan - Prometheus, Grafana, cAdvisor, Node Exporter and Alert Manager](https://github.com/stefanprodan/swarmprom)
- [Mlabouardy - Telegraf, InfluxDB, Chronograf, Kapacitor & Slack](https://github.com/mlabouardy/swarm-tick)

#### Awesome Docker Repos
- [Jess's Dockerfiles](https://github.com/jessfraz/dockerfiles)
- [Firecat53's Dockerfiles](https://github.com/firecat53/dockerfiles)

#### RaspberryPi ARM Images:
- [arm32v6/alpine:edge](https://hub.docker.com/r/arm32v6/alpine/)
- [arm32v6/golang:alpine](https://hub.docker.com/r/arm32v6/golang/)
- [arm32v6/haproxy:alpine](https://hub.docker.com/r/arm32v6/haproxy/)
- [arm32v6/node:alpine](https://hub.docker.com/r/arm32v6/node/)
- [arm32v6/openjdk:alpine](https://hub.docker.com/r/arm32v6/openjdk/)
- [arm32v6/postgres:alpine](https://hub.docker.com/r/arm32v6/postgres/)
- [arm32v6/python:2.7-alpine3.6](https://hub.docker.com/r/arm32v6/python/)
- [arm32v6/python:3.6-alpine3.6](https://hub.docker.com/r/arm32v6/python/)
- [arm32v6/rabbitmq:alpine](https://hub.docker.com/r/arm32v6/rabbitmq/)
- [arm32v6/redis:alpine](https://hub.docker.com/r/arm32v6/redis/)
- [arm32v6/ruby:alpine3.6](https://hub.docker.com/r/arm32v6/ruby/)
- [arm32v6/tomcat:alpine](https://hub.docker.com/r/arm32v6/tomcat/)
- [arm32v6/traefik:latest](https://hub.docker.com/r/arm32v6/traefik/)
- [arm32v7/debian:lates](https://hub.docker.com/r/arm32v7/debian/)
- [hypriot/rpi-redis](https://hub.docker.com/r/hypriot/rpi-redis/)
- [jixer/rpi-mongo](https://github.com/jixer/rpi-mongo)
- [alexellis/armhf](https://github.com/alexellis/docker-arm/tree/master/images/armhf)
- [zeiot: rpi-prometheus stack](https://github.com/zeiot)
- [larmog](https://hub.docker.com/u/larmog/)
- [Rpi MongoDB](https://github.com/andresvidal/rpi3-mongodb3)
- [ARM Swarm](https://github.com/armswarm)

#### Docker Image Repositories
- [Docker Hub: arm32v6](https://hub.docker.com/u/arm32v6/)
- [Docker Hub: armv7](https://hub.docker.com/u/armv7/)
- [Github: Luvres Armhf](https://github.com/luvres/armhf)
- [Apache/PHP7 on Alpine](https://github.com/ulsmith/alpine-apache-php7)
- [Tomcat on Alpine](https://github.com/docker-library/tomcat/blob/master/8.0/jre8-alpine/Dockerfile)
- [Nginx (jwilder)](https://github.com/jwilder/nginx-proxy)
- [Alpine Images (smebberson)](https://github.com/smebberson/docker-alpine)
- [SameerSbn](https://hub.docker.com/u/sameersbn/)
- [Linuxserver.io](https://hub.docker.com/u/linuxserver/)
- [Apache-PHP5](https://hub.docker.com/r/nimmis/alpine-apache-php5/)
- [Apache-PHP-Email](https://github.com/harobed/docker-php-ssmtp)

#### Docker-Awesome-Lists
- [Java Docker Services](https://github.com/AdamBien/docklands)
- [shouse Docker Awesome List](https://gist.github.com/shouse/a14c44e97a2cd2a1f030)

#### Docker Blogs:
- [Whoami used in Traefik Docs](https://hub.docker.com/r/emilevauge/whoami/)
- [Sqlite with Docker](https://github.com/spartakode/my-docker-repos/blob/master/sqlite3/Dockerfile)
- [Rails with Postgres and Redis](https://github.com/mookjp/rails-docker-example)
- [Async Tasks with Flask and Redis](https://testdriven.io/asynchronous-tasks-with-flask-and-redis-queue)
- [Flask and Postgres](https://github.com/davidmukiibi/docker-flask)
- [Elastic Beats on RaspberryPi](http://ict.renevdmark.nl/2016/07/05/elastic-beats-on-raspberry-pi/)

#### Docker Storage
- [Rancher Convoy](https://github.com/rancher/convoy)
- [Flocker](https://flocker.readthedocs.io/en/latest/flocker-features/storage-backends.html#supported-backends)
- [EMC ScaleIO](http://node.mu/2017/06/30/scaleio-on-ubuntu-xenial/)
- [RexRay Ceph with Ansible](https://github.com/lucj/swarm-rexray-ceph)
- [ContainX](http://containx.io/)


#### OpenFaas:
- [FaaS Releases](https://github.com/openfaas/faas/releases)
- [FaaS Workshop](https://github.com/openfaas/workshop)

#### Prometheus / Grafana on Swarm:
- [StefanProdan - SwarmProm](https://github.com/stefanprodan/swarmprom)
- [Monitoring with Prometheus](https://medium.com/@soumyadipde/monitoring-in-docker-stacks-its-that-easy-with-prometheus-5d71c1042443)
- [UschtWill - Prometheus Grafana Elastalert](https://github.com/uschtwill/docker_monitoring_logging_alerting)
- [Chmod-Org Promethus with Blackbox](https://github.com/chmod666org/docker-swarm-prometheus)
- [Finestructure: Prometheus Tutorial](https://finestructure.co/blog/2016/5/16/monitoring-with-prometheus-grafana-docker-part-1)

## Logging / Kibana / Beats

### Libraries
- [Loguru](https://github.com/Delgan/loguru) | [Flask Example with Loguru](https://gist.github.com/M0r13n/0b8c62c603fdbc98361062bd9ebe8153)

### Frameworks
- [shazChaudhry Swarm GELF Stack](https://github.com/shazChaudhry/docker-elastic)


## Continious Integration:

#### Circle-CI
- [PHP with Circle-CI](https://circleci.com/docs/1.0/language-php/)

#### Concourse
- [Setup Concourse Environment with Docker](https://concourse.ci/docker-repository.html)
- [Getting Started with Concourse and Docker](https://blog.anynines.com/getting-started-with-concourse-ci-and-docker/)
- [Concourse Gated Pipelines](https://github.com/pivotalservices/concourse-pipeline-samples/tree/master/concourse-pipeline-patterns/gated-pipelines)
- [Concourse Boilerplate](https://github.com/EugenMayer/concourseci-server-boilerplate)

#### Jenkins
- [Modess - PHP with Jenkins](https://modess.io/jenkins-php/)
- [CI/CD Nodejs Tutorial with Jenkins](https://code.tutsplus.com/tutorials/setting-up-continuous-integration-continuous-deployment-with-jenkins--cms-21511)
- [CI/CD Nodejs Tutorial with Jenkins @medium](https://medium.com/@mosheezderman/how-to-set-up-ci-cd-pipeline-for-a-node-js-app-with-jenkins-c51581cc783c)
- [Epic CICD workflow with Jenkins, Gitlab, Sonar, Nexus](https://github.com/shazChaudhry/docker-swarm-mode)

#### SwarmCi
- [SwarmCI](https://github.com/ghostsquad/swarmci)

#### Travis-CI
- [Getting Started with Travis-CI (Original Docs)](https://docs.travis-ci.com/user/getting-started/)
- [Getting Started with Travis-CI (dwyl - nodejs)](https://github.com/dwyl/learn-travis)
- [Blog Site with Travis-CI (Python)](https://matthewmoisen.com/blog/how-to-set-up-travis-ci-with-github-for-a-python-project/)
- [Build Tests with Python on Travis-CI](https://github.com/softwaresaved/build_and_test_examples/blob/master/travis/HelloWorld.md)
- [Moving app with Travis-CI](https://www.raywenderlich.com/109418/travis-ci-tutorial)

#### LambCI
- [LambCI](https://github.com/lambci/lambci)

## DynamoDB

#### DynamoDB Docs

- [AWS DynamoDB: SQL to NoSQL](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/SQLtoNoSQL.ReadData.Query.html)

#### DynamoDB Best Practices

- [Choosing the Right Partition Key](https://aws.amazon.com/blogs/database/choosing-the-right-dynamodb-partition-key/)
- [10 Things you should know](https://cloudacademy.com/blog/amazon-dynamodb-ten-things/)

#### DynamoDB General Info

- [Understanding DynamoDB](https://medium.com/@yaofei/understand-dynamodb-b278f718ddb8)

## Elasticsearch

#### Elasticsearch Documentation
- [General Recommendation](https://www.elastic.co/guide/en/elasticsearch/reference/current/general-recommendations.html)
- [How Many Shards in my Cluster](https://www.elastic.co/blog/how-many-shards-should-i-have-in-my-elasticsearch-cluster)
- [Managing Time-Based Indices Efficiently](https://www.elastic.co/blog/managing-time-based-indices-efficiently)
- [Elasticsearch Best Practices (Bonsai.io)](https://bonsai.io/2016/01/11/ideal-elasticsearch-cluster)
- [AWS ES - Scaling up my Domain](https://aws.amazon.com/premiumsupport/knowledge-center/elasticsearch-scale-up/)

#### Elasticsearch Cheetsheets:
- [My ES Cheatsheet](https://gist.github.com/ruanbekker/e8a09604b14f37e8d2f743a87b930f93)

#### Elasticsearch Blogs
- [Maximize Elasticsearch Indexing Performance](https://qbox.io/blog/maximize-guide-elasticsearch-indexing-performance-part-1)
- [Autoritative Guide to ES Performance Tuning](https://qbox.io/blog/authoritative-guide-elasticsearch-performance-tuning-part-1)
- [Full text Search Queries](https://opendistro.github.io/for-elasticsearch-docs/docs/elasticsearch/full-text/)
- [Query Elasticsearch](https://okfnlabs.org/blog/2013/07/01/elasticsearch-query-tutorial.html)

#### Elasticsearch Tools
- [Export Data from ES to ES](https://github.com/mallocator/Elasticsearch-Exporter)

## Environment Setups:
- [Golang](https://medium.com/aishik/install-golang-the-right-way-4743fee9255f)

## Knowledge Base

## KB HTTPS
- [How does HTTPS work (Miguel Grinberg)](https://blog.miguelgrinberg.com/post/running-your-flask-application-over-https)

## Kubernetes

- [Awesome Kubernetes](https://github.com/ramitsurana/awesome-kubernetes/blob/master/README.md)
- [Kubernetes Cheatsheet](https://cheatsheet.dennyzhang.com/cheatsheet-kubernetes-a4)
- [Getting Started: Python application on Kubernetes](https://kubernetes.io/blog/2019/07/23/get-started-with-kubernetes-using-python/)
- [Kubernetes Deployments: The Ultimate Guide](https://semaphoreci.com/blog/kubernetes-deployment)
- [Prometheus Monitoring Stack with Kubernetes on DO](https://www.digitalocean.com/community/tutorials/how-to-set-up-a-prometheus-grafana-and-alertmanager-monitoring-stack-on-digitalocean-kubernetes)
- [Traefik as an Ingress Controller on Minikube](https://tech.evaneos.com/traefik-as-an-ingress-controller-on-minikube-with-kustomize-helm-a3b2f44a5c2a)
- [Traefik Ingress with Kubernetes](https://itnext.io/traefik-cluster-as-ingress-controller-for-kubernetes-99fa6c34402)
- [Manual Connect your Kubernetes from Outside](https://medium.com/faun/manually-connect-to-your-kubernetes-cluster-from-the-outside-d852346a7f0a)
- [HTTPS Letsencrypt on k3s](https://pascalw.me/blog/2019/07/02/k3s-https-letsencrypt.html)
- [Kubernetes: Nodeport vs Loadbalancer](https://medium.com/google-cloud/kubernetes-nodeport-vs-loadbalancer-vs-ingress-when-should-i-use-what-922f010849e0)
- [Prometheus Monitoring Pipeline on Kubernetes](https://medium.com/kubernetes-tutorials/simple-management-of-prometheus-monitoring-pipeline-with-the-prometheus-operator-b445da0e0d1a)
- [Building a Kubernetes CI/CD Pipeline with Rancher](https://rancher.com/blog/2018/2018-08-07-cicd-pipeline-k8s-autodevops-rancher-and-gitlab/)
- [Building a Kubernetes CI/CD Pipeline with AWS](https://medium.com/swlh/universal-cicd-pipeline-on-aws-and-k8s-7b4129fac5d4)
- [Gitea and Drone CI/CD on k3s](https://itnext.io/explore-gitea-drone-ci-cd-on-k3s-4a9e99f8b938)
- [Serverless with Kubernetes using OpenFaaS and Linkerd2](https://github.com/openfaas-incubator/openfaas-linkerd2/blob/master/README.md)
- [Managing Kubernetes with kubectl](https://rancher.com/blog/2019/how-to-manage-kubernetes-with-kubectl/)
- [OpenFaas Workshop on k3s](https://gist.github.com/alexellis/a6ee5f094f86987a0dc508442220c52a)
- [Kubernetes Hands-On Lab with collabnix](http://collabnix.com/kubernetes-hands-on-lab-4-deploy-application-stack-using-helm-on-play-with-kubernetes-platform/)
- [Create ReadWrite Persistent Volumes on Kubernetes](https://medium.com/asl19-developers/create-readwritemany-persistentvolumeclaims-on-your-kubernetes-cluster-3a8db51f98e3)
- [Kubernetes Clusters with k3s and multipass](https://medium.com/@mattiaperi/kubernetes-cluster-with-k3s-and-multipass-7532361affa3)

### Kubernetes Storage
- [Kadalu](https://kadalu.io/docs/quick-start)
- [Rancher: Longhorn Storage](https://rancher.com/docs/k3s/latest/en/storage/)


## Golang

- [Generate Fake Random Data with Golang](https://github.com/brianvoe/gofakeit)
- [Ultimate Golang Study Guide](https://github.com/hoanhan101/ultimate-go)

## Great Blogs

- [Exratione.com](https://www.exratione.com/blog/)
- [Joelabrahamsson.com](http://joelabrahamsson.com/elasticsearch-101/)
- [Benjamin Cane](http://bencane.com/)
- [Michael Herman](http://mherman.org/)
- [Charles Leifer](http://charlesleifer.com/)
- [Labouardy](https://www.blog.labouardy.com/)
- [Mark's Tech Blog](https://tech.marksblogg.com)

## Linuxkit:
- [Getting Started with Linuxkit](https://medium.com/aishik/getting-started-with-linuxkit-and-moby-project-ff7121c4e321)

## Logging Stacks
- [shazChaudhry Swarm GELF Stack](https://github.com/shazChaudhry/docker-elastic)

## Machine Learning:
- [PracticalAI](https://github.com/GokuMohandas/practicalAI/blob/master/README.md)

## Metrics:
- [AppMetrics with Flask](https://github.com/avalente/appmetrics)
- [Scales: Metrics for Python](https://github.com/Cue/scales)
- [Graphite: Python Flask Metrics](https://pypi.org/project/graphite-pymetrics/)

## MongoDB:
- [Setup MongoDB Cluster](https://linode.com/docs/databases/mongodb/build-database-clusters-with-mongodb/)
- [MongoDB Scripts](https://github.com/AD7six/mongo-scripts)
- [MongoDB Monitoring Tools](https://docs.mongodb.com/v2.4/administration/monitoring/#self-hosted-monitoring-tools)
- [Roles with MongoDB](https://studio3t.com/knowledge-base/articles/mongodb-users-roles-explained-part-1/)
- [Queries: Guru99](https://www.guru99.com/mongodb-tutorials.html)
- [Queries: Exploratory](https://blog.exploratory.io/an-introduction-to-mongodb-query-for-beginners-bd463319aa4c)
- [Queries: Tutorialspoint](https://www.tutorialspoint.com/mongodb/mongodb_create_database.htm)
- [Queries: MongoDB Cheatsheet](https://gist.github.com/rbekker87/5b4cd9ef36b6ae092a6260ab9e621a43)

## Monitoring
- [Docker Swarm Monitoring Stack: Telegraf, InfluxDB, Chronograf, Kapacitor](https://hackernoon.com/monitor-swarm-cluster-with-tick-stack-slack-3aaa6483d44a) [github source](https://github.com/mlabouardy/swarm-tick)
- [Docker Swarm Monitoring Stack: Prometheus, Grafana, cAdvisor, Node Exporter](https://stefanprodan.com/2017/docker-swarm-instrumentation-with-prometheus/) [github source](https://github.com/stefanprodan/swarmprom)
- [Prometheus Grafana Docker](https://finestructure.co/blog/2016/5/16/monitoring-with-prometheus-grafana-docker-part-1)
- [Prometheus Blog Seros](https://pierrevincent.github.io/2017/12/prometheus-blog-series-part-1-metrics-and-labels/)
- [Memcached Monitoring](https://blog.serverdensity.com/monitor-memcached/)
- [Nagios with Nagios Graph](https://raymii.org/s/tutorials/Nagios_Core_4_Installation_on_Ubuntu_12.04.html)
- [Slack Alerts with Prometheus](https://medium.com/quiq-blog/better-slack-alerts-from-prometheus-49125c8c672b)
- [Local Prometheus Stack](https://github.com/deanwilson/docker-compose-prometheus)
- [Docker Swarm Promethus Setup #1](https://github.com/chmod666org/docker-swarm-prometheus)
  - [Docker Swarm Prometheus Setup #1: Blog](https://chmod666.org/2017/08/monitoring-a-docker-swarm-cluster-with-prometheus)
- [Docker Swarm Promethus Setup #2](https://homelab.business/docker-swarm-monitoring-part-01/)
- [Docker Swarm Promethus Setup #3 (Blackbox)](https://medium.com/the-telegraph-engineering/how-prometheus-and-the-blackbox-exporter-makes-monitoring-microservice-endpoints-easy-and-free-of-a986078912ee)
- [Uptime (fzaninotto)](https://github.com/fzaninotto/uptime)

## Monitoring and Alerting
- [Cabot (Lightweight Pagerduty)](https://github.com/arachnys/cabot)
- [Nagios](https://www.nagios.org/)

## Monitoring as Statuspages
- [Statuspage (darkpixel](https://github.com/darkpixel/statuspage)
- [Cachet](https://github.com/cachethq/Cachet)

## Programming

#### Golang:
- [Golang Tutorials](http://golangtutorials.blogspot.co.za/2011/05/table-of-contents.html)
- [Golang Wiki](https://github.com/golang/go/wiki)

#### Java:
- [Java Spring Boot Examples](https://wiki.ruanbekker.com/index.php/Java_Spring_Boot_App_Examples)

#### Python

#### Ruby:
- [Learn Ruby: Learn Ruby the Hard Way](https://learnrubythehardway.org/book)
- [Learn Ruby: Ruby for Beginners](http://ruby-for-beginners.rubymonstas.org/index.html)
- [Learn Ruby: Launch School](https://launchschool.com/books/ruby/read/loops_iterators#forloops)
- [Learn Ruby: Arrays](https://gistpages.com/posts/ruby_arrays_insert_append_length_index_remove)
- [Install Ruby Environment on Mac](https://gorails.com/setup/osx/10.12-sierra)

#### Ruby on Rails:
- [Tutorial: Ruby On Rails](https://www.railstutorial.org/book/beginning)
- [Tutorial: ROR on Docker](http://codingnudge.com/2017/03/17/tutorial-how-to-run-ruby-on-rails-on-docker-part-1/)

## Queues

- [Alpine SQS](https://github.com/roribio/alpine-sqs)
- [Kombu: Messaging library for Python](https://github.com/celery/kombu)
- [Python Job Queues with Redis](https://python-rq.org/)

## Sysadmin References:
- [Sysadmin Command References](https://gist.github.com/ruanbekker/3118ed23c25451132becacd3b974db08)
- [Linux Performance Observability Tools](https://medium.com/@chrishantha/linux-performance-observability-tools-19ae2328f87f)
- [Troubleshooting High IO Wait](http://bencane.com/2012/08/06/troubleshooting-high-io-wait-in-linux/)
- [IO Monitoring in Linux](https://blog.pythian.com/basic-io-monitoring-on-linux/)
- [IOStat and VMStat for Performance Monitoring](http://xiayubin.com/blog/2014/01/29/how-i-use-iostat-and-vmstat-for-performance-analysis/)
- [Debugging Heavy Load](https://www.tummy.com/articles/isolating-heavy-load/)

## Self Hosting

#### Email Server Setups
- [Extratione: Postfix Dovecot MySQL Virtual Users Postfixadmin](https://www.exratione.com/2016/05/a-mailserver-on-ubuntu-16-04-postfix-dovecot-mysql/)
- [Extratione: Postfix Dovecot MySQL Virtual Users Postfixadmin (Ubuntu 18)](https://www.exratione.com/2019/02/a-mailserver-on-ubuntu-18-04-postfix-dovecot-mysql/)
- [Linuxsize: Postfix Dovecot MySQL Virtual Users Postfixadmin](https://linuxize.com/post/set-up-an-email-server-with-postfixadmin/)
- [Howtoforge: Postfix, MySQL, Dovecto, Dspam](https://www.howtoforge.com/postfix_mysql_dovecot_dspam_clamav_postgrey_rbl_debian_etch)
- [Linuxsize: VirtualUsers, MySQL, Postfix, Dovecot](https://linuxize.com/post/set-up-an-email-server-with-postfixadmin/)

#### Mailscanner Server Setups
- [Spamassassin with Debian 8](https://syslint.com/blog/tutorial/how-to-install-and-configure-spamassassin-with-postfix-in-debian-8/)

#### Financial
- [SelfHosted Firefly](https://github.com/firefly-iii/firefly-iii)



#### Self Hosting Frameworks:
- [Sandstorm](https://sandstorm.io/)

## Serverless

- [Serverless Zappa](https://github.com/Miserlou/Zappa)
- [Serverless Contact Form](https://github.com/faizanbashir/python-ses-dynamodb-contactform)
- [Serverless Authentication on AWS (danilop)](https://github.com/danilop/LambdAuth)

## VPN:
#### VPN-Howto:
- [Ubuntu OpenVPN Script](https://www.cyberciti.biz/faq/howto-setup-openvpn-server-on-ubuntu-linux-14-04-or-16-04-lts/)
- [Ubuntu IPSec Script](https://github.com/hwdsl2/setup-ipsec-vpn)
- [DO - Setup OpenVPN on Ubuntu](https://www.digitalocean.com/community/tutorials/how-to-set-up-an-openvpn-server-on-ubuntu-16-04)
- [Elasticshosts - IPSec VPN](https://www.elastichosts.com/blog/linux-l2tpipsec-vpn-client/)
- [PPTP/IPSec/OpenVPN Auto Install](https://github.com/bedefaced/vpn-install)

## Website Templates

#### Resume Templates
- [johnmarcampbell resume-site](https://github.com/johnmarcampbell/resume-site)

## Web Frameworks

#### Python Flask:
- [Python Flask Upload Example](https://gist.github.com/dAnjou/2874714)
- [Awesome Flask - humiaozuzu](https://github.com/humiaozuzu/awesome-flask#awesome-flask)
- [Awesome Flask Apps - Greyli](https://github.com/greyli?tab=repositories)
- [Flask over HTTPS (MG)](https://blog.miguelgrinberg.com/post/running-your-flask-application-over-https)
- [Flask Advanced Patterns](https://speakerdeck.com/mitsuhiko/advanced-flask-patterns-1)
- [Flask MVC Boilerplate](https://github.com/tojrobinson/flask-mvc)
