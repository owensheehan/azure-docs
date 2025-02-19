---
title: Best practices for Using and Monitoring the Server Load for Azure Cache for Redis
titleSuffix: Azure Cache for Redis
description: Learn how to use and monitor your server load for Azure Cache for Redis.
author: shpathak-msft
ms.service: cache
ms.topic: conceptual
ms.date: 08/25/2021
ms.author: shpathak
---

# Manage Server Load for Azure Cache for Redis

## Value sizes

The design of your client application determines whether you should store many small values or a smaller number of larger values. From a Redis server perspective, smaller values give better performance. We recommend keeping value size smaller than 100 kB.

If your design requires you to store larger values in the Azure Cache for Redis, the server load will be higher. In this case, you might need to use a higher cache tier to ensure CPU usage doesn't limit throughput.

Even if the cache has sufficient CPU capacity, larger values do increase latencies, so follow the guidance in [Configure appropriate timeouts](cache-best-practices-connection.md#configure-appropriate-timeouts).

Larger values also increase the chances of memory fragmentation, so be sure to follow the guidance in [Configure your maxmemory-reserved setting](cache-best-practices-memory-management.md#configure-your-maxmemory-reserved-setting).

## Avoid client connection spikes

Creating and closing connections is an expensive operation for Redis server. If your client application creates or closes too many connections in a small amount of time, it could burden the Redis server.

If you're instantiating many client instances to connect to Redis at once, consider staggering the new connection creations to avoid a steep spike in the number of connected clients.

## Memory pressure

High memory usage on the server makes it more likely that the system will need to page data to disk, resulting in page faults that can slow down the system significantly.

## Avoid long running commands

Redis server is a single-threaded system. Long running commands can cause latency or timeouts on the client side because the server can't respond to any other requests while it's busy working on a long running command. For more information, see [Troubleshoot Azure Cache for Redis server-side issues](cache-troubleshoot-server.md).  

## Monitor Server Load

Add monitoring on Server load to ensure you get notifications when high server load occurs. Monitoring can help you understand your application constraints. Then, you can work proactively to mitigate issues. We recommend trying to keep server load under 80% to avoid negative performance effects.

## Plan for server maintenance

Ensure you have enough server capacity to handle your peak load while your cache servers are undergoing maintenance. Test your system by rebooting nodes while under peak load. For more information on how to simulate deployment of a patch, see [reboot](cache-administration.md#reboot).

## Next steps

- [Troubleshoot Azure Cache for Redis server-side issues](cache-troubleshoot-server.md)
- [Connection resilience](cache-best-practices-connection.md)
  - [Configure appropriate timeouts](cache-best-practices-connection.md#configure-appropriate-timeouts).
- [Memory management](cache-best-practices-memory-management.md)
  - [Configure your maxmemory-reserved setting](cache-best-practices-memory-management.md#configure-your-maxmemory-reserved-setting)
