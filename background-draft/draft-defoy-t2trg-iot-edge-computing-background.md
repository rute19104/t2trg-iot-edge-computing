---
stand_alone: true
ipr: trust200902
docname: draft-defoy-t2trg-iot-edge-computing-background-00
cat: info
pi:
  toc: 'yes'
  symrefs: 'yes'
  iprnotified: 'yes'
  strict: 'yes'
  compact: 'yes'
  sortrefs: 'yes'
  colonspace: 'yes'
  rfcedstyle: 'no'
  tocdepth: '4'
title: "IoT Edge Computing: Initiatives, Projects and Products"
abbrev: IoT Edge Computing Background
area: T2TRG
author:

- ins: X. de Foy
  name: Xavier de Foy
  org: InterDigital Communications, LLC
  street: '1000 Sherbrooke West'
  city: Montreal
  code: H3A 3G4
  country: Canada
  email: xavier.defoy@interdigital.com

- ins: J. Hong
  name: Jungha Hong
  org: ETRI
  street: '218 Gajeong-ro, Yuseung-Gu'
  city: Daejeon
  code: '34129'
  country: Korea
  email: jhong@etri.re.kr

- ins: Y-G. Hong
  name: Yong-Geun Hong
  org: ETRI
  street: '218 Gajeong-ro, Yuseung-Gu'
  city: Daejeon
  code: '34129'
  country: Korea
  email: yghong@etri.re.kr

- ins: M. Kovatsch
  name: Matthias Kovatsch
  org: Huawei Technologies Duesseldorf GmbH
  street: 'Riesstr. 25 C // 3.OG'
  city: Munich
  code: '80992'
  country: Germany
  email: ietf@kovatsch.net

- ins: E. Schooler
  name: Eve Schooler
  org: Intel
  street: '2200 Mission College Blvd.'
  city: Santa Clara, CA
  code: '95054-1537'
  country: USA
  email: eve.m.schooler@intel.com

- ins: D. Kutscher
  name: Dirk Kutscher
  org: University of Applied Sciences Emden/Leer
  street: 'Constantiaplatz 4'
  city: Emden
  code: '26723'
  country: Germany
  email: ietf@dkutscher.net

normative:

informative:

  IOT-EDGE:
    title: "IoT Edge Challenges and Functions"
    date: {DATE}
    seriesinfo:
      Internet-Draft: draft-hong-t2trg-iot-edge-computing
    author:
      - ins: J. Hong
      - ins: Y-G. Hong
      - ins: X. de Foy
      - ins: M. Kovatsch
      - ins: E. Schooler
      - ins: D. Kutscher
  OpenFog:
    title: 'OpenFog Reference Architecture for Fog Computing'
    date: '2017'
    seriesinfo: OpenFog Consortium
  ETSI_MEC_03:
    title: 'Mobile Edge Computing (MEC); Framework and Reference Architecture'
    author:
    - ins: ETSI
    date: '2019'
    seriesinfo: 'ETSI GS 003'
    target: 'https://www.etsi.org/deliver/etsi_gs/MEC/001_099/003/02.01.01_60/gs_MEC003v020101p.pdf'
  ETSI_MEC_02:
    title: 'Multi-access Edge Computing (MEC); Phase 2: Use Cases and Requirements'
    author:
    - ins: ETSI
    date: '2016'
    seriesinfo: 'ETSI GS 002'
    target: 'https://www.etsi.org/deliver/etsi_gs/MEC/001_099/002/02.01.01_60/gs_MEC002v020101p.pdf'
  _3GPP.23.501:
    title: 'System Architecture for the 5G System'
    author:
    - ins: 3GPP
    date: '2019'
    seriesinfo: '3GPP TS 23.501'
    target: 'http://www.3gpp.org/ftp/Specs/html-info/23501.htm'
  ETSI_MEC_WP_28:
    title: 'MEC in 5G networks'
    author:
    - ins: ETSI
    date: '2018'
    seriesinfo: 'White Paper'
    target: 'https://www.etsi.org/images/files/ETSIWhitePapers/etsi_wp28_mec_in_5G_FINAL.pdf'
  Linux_Foundation_Edge:
    title: 'Linux Foundation Edge'
    author:
    - ins: Linux Foundation
    date: '2019'
    seriesinfo: Portal
    target: https://www.lfedge.org/
  StarlingX:
    title: 'StarlingX'
    author:
    - ins: OpenStack Foundation
    date: '2019'
    seriesinfo: 'Portal'
    target: 'https://www.starlingx.io/'
  Sifalakis:
    title: 'An Information Centric Network for Computing the Distribution of Computations'
    author:
    - ins: M. Sifalakis
    - ins: B. Kohler
    - ins: C. Scherb
    - ins: C. Tschudin
    date: '2014'
    seriesinfo: 'Proceedings of the 1st International Conference on Information-centric networking (INC)'
  _5G-CORAL:
    title: '5G Convergent Virtualised Radio Access Network Living at the Edge (5G-CORAL) Project'
    author:
    - ins: Horizon 2020 Programme
    date: '2019'
    seriesinfo: 'Portal'
    target: 'http://5g-coral.eu/'
  OpenEdgeComputing:
    title: 'Open Edge Computing'
    date: '2019'
    seriesinfo: 'Portal'
    target: 'http://openedgecomputing.org/'
  IEEE-1934:
    title: 'FOG - Fog Computing and Networking Architecture Framework'
    author:
    - ins: IEEE
    date: '2019'
    seriesinfo: 'Portal'
    target: 'https://standards.ieee.org/standard/1934-2018.html'

--- abstract

Many IoT applications have requirements that cannot be met by the traditional Cloud. As a result, the IoT is driving the Internet toward Edge computing. This draft reviews initiatives, projects and products related to IoT Edge Computing.

--- middle

# Introduction

This list of open-source or commercial products, standard initiatives and research projects aims to provide an overview of the IoT edge computing.

It has been developped in support of {{IOT-EDGE}}. This other draft studies challenges and functions associated with IoT edge computing, and provides further background information on IoT, cloud computing and edge computing.

Our goal is to be representative rather than exhaustive. Please help us complete this overview by communicating with us about entries we have missed.

# Open Source Projects

## Gateway/CPE Platforms {#sec-gateway-platforms}

EdgeX Foundry, Home Edge, Edge Virtualization Engine are
Linux Foundation projects ({{Linux_Foundation_Edge}})
aiming to provide a platform for edge computing devices.

Such an open source platform can, for example, host proprietary
programs currently run on IoT gateway products (<xref target="products"/>).

EdgeX Foundry develops an edge computing framework running on the IoT gateway.

Home Edge develops an edge computing framework especially dedicated to home computing devices,
controlling home appliances, sensors, etc., and enabling AI applications, especially
distributed and parallel machine learning.

The Edge Virtualization Engine (EVE) project develops a virtualization platform (for VMs and containers)
designed to run outside of the datacenter, in an edge network; EVE is deployed on bare-metal hardware.

Computing devices:
: Hardware support for EdgeX and EVE is similar: they support x86 and ARM-based computing devices; A typical target can be a Linux Raspberry Pi  with 1GB RAM, 64bit CPU, 32GB storage.

Service platform:
: EdgeX uses a micro-service architecture. Micro-services on the gateway are connected together, and to outside applications, through REST, or messaging technologies such as MQTT, AMQP and 0MQ. The gateway can communicate with external backend applications or other gateways (north-south in tiered deployments or east-west in more distributed deployments). Gateway-device communication can use a wide range of IoT protocols. "Export services" enable on-gateway and off-gateway clients to register as recipient for data from devices. Core services are microservices that deal with persisting data from devices or alternatively "streaming" device data through, without persistence (core data service); managing information about the IoT devices, including their sensors, how to communicate with them, etc. (metadata service); and actual communication with IoT devices, on behalf of other on-gateway or off-gateway services (command service). A rule engine provides an API to register actions in response to conditions typically including an IoT device ID, sensor values to check, thresholds, etc. The scheduling micro service deals with organizing the removal of data persisted on the gateway. Alerts and notifications microservice can be used to dispatch alert/notifications from internal or external sources to interested consumers including backend servers, or human operators through email or SMS.

Edge cloud applications:
: Target applications for EdgeX include Industrial IoT (e.g., IoT sensor data and actuator control mixed with augmented reality application for technicians). Home Edge focuses on smart home use cases, including using AI lifestyle and safety applications.

## Edge Cloud Management Platforms {#sec-cloud-management-platforms}

This set of open-source projects setup and manage clouds of individual edge computing devices.

StarlingX ({{StarlingX}}) extends OpenStack to provide
virtualization platform management
for edge clouds, which are distributed (in the range of 100 compute devices),
secure and highly available.

Akraino Edge Stack, another project from the Linux Fundation Edge {{Linux_Foundation_Edge}},
has a wider scope of developing a management platform adapted for the edge
(e.g., covering 1000 plus locations),
aiming for zero-touch provisioning, and zero-touch lifecycle management.

Computing devices:
: Compute devices are typically Linux-based application servers or more constrained devices.

Service platform:
: StarlingX adds new management services to OpenStack by leveraging building blocks such as Ceph for distributed storage, Kubernetes for orchestration. The new services are for management of configuration (enabling auto-discovery and configuration), faults, hosts (enabling host failure detection and auto-recovery), services (providing high availability through service redundancy and multi-path communication) and software (enabling updates).

Edge cloud applications:
: An edge computing platform may support a wide range of use cases. E.g., autonomous vehicles, industrial automation and robotics, cloud RAN, metering and monitoring, mobile HD video, content delivery, healthcare imaging and diagnostics, caching and surveillance, augmented/virtual reality, small cell services for high density locations (stadiums), universal CPE applications, retail.

## Related Projects

Open Edge Computing ({{OpenEdgeComputing}}) is an initiative from universities, manufacturers, infrastructure providers and operators, enabling efficiently offloading cloudlets (VMs) to the edge.
Computing devices are typically powerful, well-connected servers located in mobile networks (e.g., collocated with base stations or aggregation sites).
The service platform is built on top of OpenStack++, an extension of OpenStack
to support cloudlets.
This project is mentioned here as a related project because of its edge computing focus, and potential for some IoT use cases. Nevertheless, its primary use cases are typically non-IoT related, such as offloading processing-intensive applications from a mobile device to the edge.

# Products

## IoT Gateways {#sec-iot-gateways}

Multiple products are marketed as IoT gateways (Amazon Greengrass, Microsoft Azure IoT Edge, Google Cloud IoT Core, and gateway solutions from Bosh and Siemens).
They are typically composed of a software frameworks that can run on a wide range
of IoT gateway hardware devices to provide local support for cloud services,
as well as some other local IoT gateway features such as relaying communication and caching content.
Remote cloud is both used for management of the IoT gateways, and for hosting
customer application components.
Some IoT gateway products (Amazon Snowball) have a primary purpose of storing edge data on premises, to enable physically moving this data into the cloud without incurring digital data transfer cost.

Computing devices:
: Typical computing devices run Linux, Windows or a Real-Time OS over an ARM or x86 architecture. The level of service support on the computing device can range from low-level packages giving maximum control to embedded developers, to high-level SDKs. Typical requirements can start at 1GHz and 128MB RAM, e.g., ranging from Raspberry Pi to a server-level appliance.

Service platform:
: IoT gateways can provide a range of service including: running stateless functions; routing messages between connected IoT devices (using a wide range of IoT protocols); caching data; enabling some form of synchronization between IoT devices; authenticating and encrypting device data. Association between IoT devices and gateway based can require a device certificate.

Edge cloud applications:
: Pre-processing of IoT data for later processing in the cloud is a major driver. Use cases include industrial automation, farming, etc.

## Edge Cloud Platforms {#sec-cloud-platforms}

Services such as MobileEdgeX provide a platform for application developers to deploy software (e.g., as software containers) on edge networks.

Computing devices:
: Bare metal and virtual servers provided by mobile network operators are used as computing devices.

Service platform:
: The service platform provides end device location service, using GPS data obtained from platform software deployed in end devices, correlated with location information obtained from the mobile network. The service platform manages the deployment of application instances (containers) on servers close to end devices, using a declarative specification of optimal location from the application provider.

Edge cloud applications:
: Use cases include autonomous mobility, asset management, AI-based systems (e.g., quality inspection, assistance systems, safety and security cameras) and privacy-preserving video processing. There are also non-IoT use cases such as augmented reality and gaming.

# Standards Initiatives

## ETSI Multi-access Edge Computing {#sec-etsi-mec}

The ETSI MEC industry standardization group develops specifications that enable efficient
and seamless integration of applications from vendors, service providers,
and 3rd parties across multi-vendor MEC platforms ({{ETSI_MEC_03}}).

Basic principles followed include: leveraging NFV infrastructure; being compliant with 3GPP systems;
focusing on orchestration, MEC services, applications and platforms.

Phase 1 (2015-2016) focused on basic platform services. Phase 2 (2017-2019) focuses on:
supporting non-3GPP radio access technologies, especially WiFi;
supporting a distributed, multi-operator and multi-vendor architecture;
supporting non-VM based virtualization such as containers and PaaS.

Computing devices:
: Computing devices are typically application servers, attached to an eNodeB or at a higher level of aggregation point, and provide service to end users.

Service platform:
: The mobile edge platform offers an environment where the mobile edge applications can discover, advertise, consume and offer mobile edge services. The platform can provide certain native services such as radio network information, location, bandwidth management etc. The platform manager is responsible for managing the life cycle of applications including informing the mobile edge orchestrator of relevant application related events, managing the application rules and requirements including service authorizations, traffic rules, DNS configuration.

Edge cloud applications:
: Some of the use cases for MEC ({{ETSI_MEC_02}}) are IoT-related, including: security and safety (face recognition and monitoring), sensor data monitoring, active device location (e.g., crowd management), low latency vehicle-to-infrastructure and vehicle-to-vehicle (V2X, e.g., hazard warnings), video production and delivery, camera as a service.

## Edge Computing Support in 3GPP

The 3GPP standards organization included edge computing support in 5G {{_3GPP.23.501}}.
Integration of MEC and 5G systems has been studied in ETSI as well {{ETSI_MEC_WP_28}}.

Computing devices:
: From 3GPP standpoint, a mobile device may access any computing device located in a local data network, i.e., traffic is steered towards the local data network where the computing device is located.

Service platform:
: An external party may influence steering, QoS and charging of traffic towards the computing device. Session and service continuity can ensure that edge service is maintained when a client device moves. The network supports multiple-anchor connections, which makes it possible to connect a client device to both a local and a remote data network. The client device can be made aware of the availability of a local area data network, based on its location.

Edge cloud applications:
: Edge cloud applications in 3GPP can help support the major use cases envisioned for 5G, including massive IoT and V2X.

## OpenFog and Industrial Internet Consortium {#sec-openfog}

The OpenFog Consortium (now merged with the Industrial Internet Consortium) aims to standardize industrial IoT, fog, and edge computing. It produced a reference architecture for the fog ({{OpenFog}}), which has been published as IEEE standard P1934 in 2018. This work continues within the Industrial Internet Consortium. 

Computing devices:
: Fog nodes include computational, networking, storage and acceleration elements. This includes nodes collocated with sensors and actuators, roadside or mobile nodes involved in V2X connectivity. Fog nodes should be programmable and may support multi-tenancy. Fog computing devices must employ a hardware-based immutable root of trust, i.e., a trusted hardware component which receives control at power-on.

Service platform:
: The service platform is structured around "pillars" including: security end-to-end, scalability by adding internal components or adding more fog nodes,openness in term of discovery of/by other nodes and networks, autonomy from centralized clouds (for discovery, orchestration and management, security and operation) and hierarchical organization of fog nodes.

Edge cloud applications:
: Major use cases include smart cars and traffic control, visual security and surveillance, smart cities.

## Related Standards

The IEEE Fog Computing and Networking Architecture Framework Working Group {{IEEE-1934}} published the OpenFog architecture as an IEEE document, and plan to do further work on taxonomy, architecture framework, and compliance guidelines.

# Research Projects

## Named Function Networking {#sec-nfn}

Named Function Networking ({{Sifalakis}}) is a research project that aims to extend ICN concepts (especially named data networking) to have the network orchestrate computation. Interests are sent for a combination of function and argument names, instead of using the content name in NDN.

Computing devices:
: NFN-capable switches are collocated with computing devices.

Service platform:
: NFN enables accessing static data and dynamic computation results in one data-oriented framework, thus benefiting from usual ICN features such as data authenticity and caching, as well as enabling the network to perform various optimizations, e.g., moving data, code or both closer to requesters. NFN also enables secure access to individual elements within Named Data Objects, e.g., for filtering or aggregation.

Edge cloud applications:
: Use cases include some form of MapReduce operations and service chaining. NDN, on which NFN is based, has been studied in the context of IoT, where it can provide local trust management and rendezvous service.

## 5G-CORAL

The 5G-CORAL project ({{_5G-CORAL}}) aims to enable convergence of access across multiple radio access technologies using fog computing, using for this purpose an edge and fog computing system (EFS).

Computing devices:
: Computing devices used in 5G-CORAL include cloud and central data center servers, edge data center servers, and fixed or mobile "fog computing devices", which can be computing devices located in vehicles or factories, e.g., IoT gateways, mobile phones, cyber-physical devices, etc.

Service platform:
: 5G-CORAL architecture is based on an integrated virtualized edge and fog computing system (EFS), that aims to be flexible, scalable and interoperable with other domains including transport (fronthaul, backhaul), core and clouds. An Orchestration and Control System (OCS) enables automatic discovery of heterogeneous, multiple-owner resources, and federate them into a unified hosting environment. OCS monitors resource usage to guarantee service levels. Finally, OCS also includes orchestration and life cycle functions, including live migration and scaling. Applications (user and third-party) both inside and outside the EFS subscribe to EFS services through APIs, with emphasis on IoT and cyber-physical functionalities.

Edge cloud applications:
: EFS-hosted services include analytics obtained from IoT gateways (e.g., LORA or eNodeB gateways), context information services from RATs, transport (fronthaul and backhaul) and core networks. EFS-hosted functions include network performance acceleration functions, virtualized C-RAN functions for access nodes and possible end user devices.

