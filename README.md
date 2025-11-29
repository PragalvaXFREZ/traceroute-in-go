## Overview
Traceroute is a network diagnostic utility that traces the path packets take from your machine to a destination host. It helps identify routing paths and detect issues such as latency spikes or packet loss.

## How Traceroute Works
1. Sends ICMP Echo Request packets (or UDP, TCP in other implementations).
2. Starts with TTL = 1.
3. Each router that receives a packet with expired TTL returns an ICMP Time Exceeded message.
4. The program records that router’s IP address.
5. TTL is incremented step by step.
6. When the destination responds with an ICMP Echo Reply, the trace is complete.

## Running the Project Locally

### Clone the Repository

git clone https://github.com/PragalvaXFREZ/traceroute-in-go.git

cd traceroute-in-go


### Run the Program

sudo go run main.go -hostname=google.com


## Why sudo?
Sending raw ICMP packets requires root privileges on most operating systems.

## Inspiration
https://github.com/aerosouund/go-tracert/tree/master
