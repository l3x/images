# Overview

Here's the overall process for requesting, generating and publishing a random nunmber:

<img src="https://raw.githubusercontent.com/l3x/images/master/random-num-request.png">


# Components

**CLI** - Client that want us to generate a random number
* request random number

**KMA** - Keep Master that acts as gate keeper between the chain and random#-generating-groups 
* init new group creation
**  set # of nodes in group
**  select nodes that can join
* verify stake (has client purchased enough Keep to participate?)
* verify group ready to process random # requests
** publish group key to chain
   
**WRK** - Nodes that want to join group (worker nodes)     
* request to join group
* generate pub/priv key for group communication
* broadcast accusation (optional)

**GRP** - Group of worker nodes
* submit random number

**ETH** - Ethereum blockchain
* run contract to verify stake
* accepts published random number
