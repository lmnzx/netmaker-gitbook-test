---
icon: hand-wave
cover: .gitbook/assets/Screenshot 2024-11-15 at 4.14.03 PM.png
coverY: 0
layout:
  cover:
    visible: true
    size: full
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# About

Netmaker lets you create, manage, and automate virtual overlay networks using WireGuard. If you have two or more devices that need to communicate securely, Netmaker will help you forge the connection, allowing you to scale up to hundreds, or thousands, of devices, environments, networks, and users.

<figure><img src="https://api.scalar.com/cdn/images/nihKnpk06xBjyKI4sa5CZ/YqplyQgAwxEbEvzf1k04j.png" alt=""><figcaption></figcaption></figure>

Netmaker takes these devices and creates a flat network wher they can communicate securely. If you’re familiar with AWS, it’s like a VPC but made up of arbitrary computers. From the machine’s perspective, all these other machines are in the same neighborhood, even if they’re spread all over the world.

Netmaker also enables you to control of traffic flowing into and out of the network using gateways and ACL policies. The end result is you can create much more complex networks than a simple mesh, and create some more common patterns like remote access.

<figure><img src="https://api.scalar.com/cdn/images/nihKnpk06xBjyKI4sa5CZ/BVN4nGx5LKlHvYQAgrZ8q.svg" alt=""><figcaption></figcaption></figure>

Netmaker has many similarities to Tailscale, ZeroTier, and Nebula. What makes Netmaker different is the speed and flexibility. Netmaker is faster because it uses kernel WireGuard. It is more flexible because it lets you build many different types and patterns of networks, and also gives you the choice of how endpoints are added to the network, with three different client-side applications. And, of course, you can also self-host Netmaker, to give you complete control of your network traffic.

## How Does Netmaker Work?

Netmaker relies on WireGuard to create tunnels between machines. At its core, Netmaker is managing WireGuard across machines to create sensible networks. Netmaker is the management server, which manages three different types of client-side applications.

**The configuration server:** Netmaker is the configuration server, which can be either self-hosted, or deployed using our cloud-hosted SaaS. There is a fully open source version, as well as a Professional version.

The Clients: Netmaker manages three different types of clients -

* **Netclient:** A headless agent that manages WireGuard and is meant primarily for the “worker nodes” of your network, e.g. server endpoints, and devices that will route traffic for your network. It runs on Windows, Linux, Mac, and Docker.
* **WireGuard:** Netmaker can add pure WireGuard tunnels to the network, allowing you to deploy endpoints on any WireGuard compatible device.
* **Remote Access Client:** A user-centric application meant for end-users, primarily for remote access, with authentication and authorization via identity, and session expiry.

As the network manager, you interact with the server to create and manage networks and devices. The server holds configurations for these networks and devices and pushes updates to the agents (netclient) over a message queue.

The client will let the server know when any local changes (like ip address, port) should be pushed out to the other clients. By doing this across many machines simultaneously, we create fully dynamic and configurable virtual networks.

## Use Cases for Netmaker

There are many use cases for Netmaker. In fact, you could probably be using it right now. Because of Netmaker’s extreme speed, there is almost no cost to putting a Netmaker overlay network on top of any existing Network.

This is a sample of how some users use Netmaker in production today. Guided setup for many of these use cases can be found in the How-To Guides or on our Blog or YouTube channel:

1. Automation and management of large WireGuard-based networks
2. Secure access to a home or office network
3. Remote management of edge sites, servers, robots, and drones
4. Site-to-site access from customer environments to cloud endpoints
5. Secure network for IoT device data transfer

\




