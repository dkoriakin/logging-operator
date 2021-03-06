# Logging Operator

A golang based CRD operator to setup and manage logging (Elasticsearch, Fluentd and Kibana) in Kubernetes cluster. It helps to setup each component of EFK stack separately.

### Supported Features

The "Logging Operator" includes these features:-

* Elasticsearch different node types, like:-
    * Master Node
    * Data Node
    * Ingestion Node
    * Client/Cordinator Node
* Elasticsearch setup with/without TLS
* Customizable elasticsearch configuration and Heap size
* Fluentd as a log-shipper which already has JSON logs support
* Kibana integration with elasticsearch for logs visulization
* Seamless upgrade for Elasticsearch, Fluentd, and Kibana
* Inculcated best practices for Kubernetes setup like `SecurityContext` and `Privilege Control`
* Loosely coupled setup, i.e. Elasticsearch, Fluentd, and Kibana can be setup individually as well.

### Architecture

<div align="center">
    <img src="./static/logging-operator-arch.png">
</div>

### Purpose

The purpose behind creating this CRD operator was to provide an easy and yet production grade logging setup on Kubernetes. But it doesn't mean this can only be used for logging setup only.

> This operator blocks Elasticsearch, Fluentd, and Kibana are loosely-couples so they can be setup individually as well. For example:- If we need elasticsearch for application database we can setup only elasticsearch as well by using this operator.
