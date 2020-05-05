# 5G-MEDIA Service Virtualization Platform

## Introduction

The 5G-MEDIA Service Virtualization Platform consists of four core components.
It has two central components: the 5G-MEDIA Service MAPE and the 5G-MEDIA Services Orchestrator, which are responsible for the intelligent orchestration of media services over the heterogeneous NFVIs. In addition, it has two auxiliary services: the 5G Apps and Services Catalogue (Public Catalogue) and the 5G-MEDIA AAA, which support horizontal services of the platform such as VNF onboarding to public catalogue, user authentication and authorization services. 

The communication among the components is held via 1) web services that some components expose and 2) using a publish/subscribe broker. The [Apache Kafka](https://kafka.apache.org/) has been selected as publish/subscribe broker. 


## Installation

To install the SVP follow the installation guidelines per component following the below flow:
1. **Install the 5G-MEDIA Services orchestration**. The backbone of this component is the [Open Source Mano](https://osm.etsi.org/). The guidelines are available [here](https://osm.etsi.org/wikipub/index.php/OSM_Release_FIVE).
2. **Install the publish/subscribe broker.** Follow the [guidelines](https://github.com/wurstmeister/kafka-docker) to build the docker image including the Apache Kafka broker (and zookeeper) and deploy it. 
3. **Install the 5G-MEDIA MAPE**. Follow the [guidelines](https://github.com/5g-media/mape) to deploy it.
4. **Install the 5G-MEDIA CATALOGUE**. Follow the [guidelines](https://github.com/5g-media/5g-catalogue) to deploy it.
5. **Install the 5G-MEDIA AAA**. Follow the [guidelines](https://github.com/5g-media/5G-MEDIA_AAA) to deploy it.


### Minimum System Requirements

The *minimum system* requirements to install the 5G-MEDIA Service Virtualization Platform are:
| # | Requirements |
| --- | --- |
| **Operating  System** | Ubuntu 16.04 LTS or newer version |
| **CPU** | 25 vCPUs |
| **MEMORY** | 35 GB RAM |
| **HARD DISK** | 250 GB available | 

The 5G-MEDIA Service Virtualization Platform could be installed in either a Linux bare metal server or (Linux) Virtual Machines. In case that you prefer Virtual Machines, you can install the components of the Service Virtualization Platform in different Virtual Machines ensuring that there is network connection among them. For example, in the frame of the project we have installed them in different OpenStack-based Virtual Machines using a common management network.


## Acknowledgements
This project has received funding from the European Union’s Horizon 2020 research and innovation programme under grant agreement [No 761699](http://www.5gmedia.eu/). The dissemination of results herein reflects only the author’s view and the European Commission is not responsible for any use that may be made 
of the information it contains.

## License
[Apache 2.0](LICENSE.md)