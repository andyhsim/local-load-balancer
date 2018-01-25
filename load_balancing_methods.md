---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Load Balancing Methods

| Method|Description|
|:---|:---|
|Consistent Hash IP|<ul><li>Maps client requests to real servers by hashing the source IPs of the request.</li><li>Client/Server relationships are maintained across ports.</li></ul>|
|Insert Cookie|<ul><li>Inserts a tracking cookie into the request.<span style="mso-spacerun:yes">&nbsp; </span>Session data contained within the cookie is used with subsequent request to send traffic back to the same real server.</li><li>Persistence is hard-coded on a per-session basis.</li><li>Cookie expires after the client&rsquo;s browser is closed.</li><li>Requires that the client accepts cookies to be effective.</li></ul>|
|Least Connections|<ul><li>The real server with the fewest number of active connections gets first priority.</li><li>Algorithm requires a difference of 10 connections, which may skew results for customers</li></ul>|
|Persistent IP|<ul><li>Ties the source IP of the requester to the real server that processes the request by a hash of all 4 octets of the requesting IP address.</li><li>Persists for 60 minutes</li></ul>|
|Round Robin|<ul><li>Each new request is assigned to the next real server in the rotation.</li><li>Balanced distribution occurs over large samples, though small samples may display a disproportionate balance.</li></ul>|
|Shortest Response|<ul><li>Server with the shortest response time receives the request.</li><li>As load and response time increases, slower servers begin to field fewer requests.</li></ul>|
|Round Robin with Persistent IP|<ul><li>Each new request is assigned to the next real server in the rotation.</li><li>Requester&rsquo;s IP address is tied to the real server, resulting in subsequent requests from the IP to be assigned to the same real server.</li></ul>|
|Round Robin with Insert Cookie|<ul><li>Each new request is assigned to the next real server in the rotation.</li><li>The load balancer inserts a cookie into the request and uses the session information from the cookie to direct traffic to the same real server for subsequent requests.</li></ul>|
|Least Connections with Persistent IP|<ul><li>Each new request is assigned to the real server with the least number of active connections at the moment.</li><li>Requester&rsquo;s IP address is tied to the real server, resulting in subsequent requests from the IP to be assigned to the same real server.</li></ul>|
|Least Connections with Insert Cookie|<ul><li>Each new request is assigned to the real server with the least number of active connections at the moment.</li><li>The load balancer inserts a cookie into the request and uses the session information from the cookie to direct traffic to the same real server for subsequent requests.</li></ul>|
|Shortest Response with Persistent IP|<ul><li>Each new request is assigned to the real server with the shortest response time.</li><li>Requester&rsquo;s IP address is tied to the real server, resulting in subsequent requests from the IP to be assigned to the same real server.</li></ul>|
|Shortest Response with Insert Cookie|<ul><li>Each new request is assigned to the real server with the shortest response time.</li><li>The load balancer inserts a cookie into the request and uses the session information from the cookie to direct traffic to the same real server for subsequent requests.</li></ul>|
