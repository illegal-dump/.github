# About

Project for kubernetes training purposes.

Scope:
- [webapp](https://github.com/illegal-dump/webapp), simple GUI written in Vue+Node, simple mock
- [api-gateway](https://github.com/illegal-dump/api-gateway), set of ymls for NGINX Kubernetes Gateway deployment
- [k8](../k8/) - complete set of ymls for illegal-dump project
- ...
- all above deployed on kubernetes cluster locally and on AWS


<br/><br/><br/>

# Architecture

![uml](http://www.plantuml.com/plantuml/png/bLDVQzH047_VJp4KH8i4v9x4XrBneOXQ50M5quUvP99RakocixDNY_IxExURDA4N_9E7kyp-_inlPpUNGP0bzfq9hNK3ClPGKOsnao_qKrvtjd4zEO5IVuYDUGf5KHYZ8bjZAV2LTZWCyCk0FjlRL7rtpmwHpdy01iWhvlwetFP-PplIEa4FbJ5R76pHeD0jtgdw-khjzJTu5tV4ZeG2N6KeMoftf2volF6UA-jGsMCOxLVEY-hQUkciUtuJaTiOijU2iI82fi6p43_cJkj9irJefifMUnt_Ya1y83vfTCJMXPj_K6x6d1KAxZ0Gd4rlAlxeWpHCdp-zFpzJxKnA8qdFAB_FH_8mlm_UMV5iNJEFRs3Va-mfXXHaBYT2mrYZmuIEx-gPZ6yYHO8j7SX96ZxMBUODvRMfooH8rohV5YZODdifBfP7hPIvKlR5wdciKwRPmIju-U89-1f4qzQsr63YeToJOgMcPxrz5GsTl-kF6S__uhTHmyr_6Vvn5oVnTDDBFF6d8tqCTLIBmdcuAfm_hoHRT5LmRNOd5fVagjXtlm40)

<br/><br/><br/>

# Kubernetes

## 1. Create cluster

```
minikube start --memory 8192 --cpus 2
```

## 2. Add entry to /etc/hosts

```
echo "$(minikube ip) minikube.local" | sudo tee -a /etc/hosts
```

test by `ping minikube.local`:
```
PING minikube.local (192.168.49.2) 56(84) bytes of data.
64 bytes from minikube.local (192.168.49.2): icmp_seq=1 ttl=64 time=0.133 ms
64 bytes from minikube.local (192.168.49.2): icmp_seq=2 ttl=64 time=0.117 ms
^C
--- minikube.local ping statistics ---
2 packets transmitted, 2 received, 0% packet loss, time 1005ms
rtt min/avg/max/mdev = 0.117/0.125/0.133/0.008 ms
```

## 3. Install NGINX Kubernetes Gateway

See [api-gateway](https://github.com/illegal-dump/api-gateway) instruction.


## 4. Apply yml-s from k8 folder





<br/><br/><br/>


---

### kubectl Cheat Sheet

[https://kubernetes.io/docs/reference/kubectl/cheatsheet/](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)


---

### Attribution
icons: [https://www.vecteezy.com/free-vector/dump](https://www.vecteezy.com/free-vector/dump)

map: [https://www.openstreetmap.org/](https://www.openstreetmap.org/) and [https://leafletjs.com](https://leafletjs.com)

