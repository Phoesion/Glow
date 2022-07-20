This is the official repo of Phoesion Glow. The repository can be used for issues/bugs reporting/tracking, discussions and (in the future) for open-sourced code.

## What is Phoesion Glow ?
Phoesion Glow is a set of tools and runtime with which your can create scalable Cloud Services.

Phoesion Glow is a complete solution for developing and managing your services, from libraries and tools in your IDE up to web servers, service bus and service hosts. 
All components have been created from scratch with the purpose of creating a uniform experience in both developing and managing your services.


## Architecture Overview
![Abstract_Architecture](https://glow-docs.phoesion.com/images/Introduction/Abstract_Architecture_Small.png)
#### Cloud entities :
- Phoesion Glow **Prism** \
	Prism is the only element exposed to the world and acts as the mediator/gateway between the world and your services.
	It can receive requests from HTTP, WebSocket/SignalR, MQTT or other protocols, and will forward them to the appropriate back-end service *(Firefly)* using the service bus *(Kaleidoscope)*.
	
- Phoesion Glow **Kaleidoscope** \
	This is the service bus for the entire cloud, used by all entities to communicate with each other.\
	Kaleidoscope is responsible for authenticating and message routing/queueing to/from all entities. *(eg. Prism<->Firefly)*
	
- Phoesion Glow **Firefly** \
	This is the element responsible for running your actual micro-services. \
	Fireflies are responsible for retrieving, hosting, running and managing you final service code.
	
- Phoesion Glow **Lighthouse** \
	Lighthouse is the command-and-control center. \
	Developers can connect to the lighthouse and from there monitor and manage the entire cloud (eg. deploy your code)

Phoesion Glow is based on a distributed micro-service cloud architecture.\
[Click here for more in-depth information about the architecture](xref:Architecture_Overview.md)


## High-Availability and Scaling
The separation of flow to components Mediator<->Bus<->Services allows you to create a highly-available, fault-tolerant and secure cloud solution in any way or configuration best suits your needs.

Adding/Removing new entities (eg. Firefly service) can be done dynamically without any static configurations or restarting the existing running instances. This means you can scale up or down your cloud dynamically as needed


## Community License
With *Community License* all components are provided for free, for both commercial and non-commercial purposes, so you can use them in your own or your customers' servers without any licensing complications.


## Usefull links
- [Samples](https://github.com/Phoesion/Glow-Samples)
- [Documentation](https://glow-docs.phoesion.com/getting_started/index.html)
- [Downloads](https://glow-docs.phoesion.com/downloads/intro.html)
- [Website](https://glow.phoesion.com)
