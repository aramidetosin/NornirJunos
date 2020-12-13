# NornirJunos

Automating Stuff with Nornir and nornir_pyez

![alt text](https://github.com/aramidetosin/NornirJunos/blob/main/pics/topo.png?raw=true)

## Requirements

```
pip install nornir_pyez
```

Must also have base config in place so that SSH access can be reached

## Usage

The main.py file deploys MC-LAG on 2 vMX devices serving as PE to a CE

1. Change the host variables as needed
2. Run main.py

## Interface config

![alt text](https://github.com/aramidetosin/NornirJunos/blob/main/pics/topo2.png?raw=true)

1. interfaces.j2
2. config_ints.py

## IS-IS config

1. isis_config.j2
2. isis_interfaces.j2
3. config_isis.py

## MPLS => RSVP => CSPF

This will deploy RSVP signaled MPLS with CSPF bandwidth constraints. Note that it will deploy the LSP on the edges and just RSVP in the core

1. mpls_proto.j2
2. deploy_mpls.py