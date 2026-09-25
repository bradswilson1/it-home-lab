# Networking

Notes and labs from the networking block.

## Network path (Lesson 6)

### My network (from ipconfig /all)
- IPv4 address: 192.168.4.36
- Subnet mask: 255.255.252.0
- Default gateway: 192.168.4.1
- DNS servers: 204.111.1.194 / 204.111.1.195

### Ping ladder results
| Test | Target | Result | Avg ms |
|---|---|---|---|
| Local stack | 127.0.0.1 | 4/4 replies | 0 ms |
| Router | 192.168.4.1 | 4/4 replies | 0 ms |
| Internet by IP | 8.8.8.8 | 4/4 replies | 20 ms |
| DNS | google.com (142.251.16.113) | 4/4 replies | 15 ms |

### tracert google.com
- Number of hops: 24
- First hop was my default gateway: (yes / no) = YES
- Hops 2-5: ISP network (private addresses, then 204.111.x)
- Hops 6-24: Google's network; hops 12-23 timed out because Google's
  internal routers don't answer trace requests
- Hop 3 showed higher latency (38 ms) than later hops; routers treat
  trace replies as low priority, so this isn't a real slowdown

### arp -a
- Confirmed my PC has learned the router's MAC address (IP-to-MAC mapping)
- Noticed two devices sharing a manufacturer prefix and one device holding two IPs

### What I learned
- Before this lesson, I didn't know that an IP address starting with 169.254
  means the PC never got an address from the router.
- The most useful command was tracert. I didn't know I could see the route my
  data takes, from my ISP into Google's network, or that there were so many
  hops in between (24 to reach google.com).
