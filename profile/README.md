# Aboutheight:32px

Project for kubernetes <img src="https://kubernetes.io//images/favicon.png" style="height:32px"/> training purposes. 

Scope:
- [webapp](https://github.com/illegal-dump/webapp), simple GUI written in Vue <img src="https://vuejs.org/logo.svg" style="height:32px"/>, Node <img src="https://nodejs.org//static/images/favicons/favicon-32x32.png" style="height:32px"/> and mock server <img src="https://www.mock-server.com/favicon.ico" style="height:32px"/>
- [api-gateway](https://github.com/illegal-dump/api-gateway), set of ymls for NGINX Kubernetes Gateway <img src="https://avatars.githubusercontent.com/u/8629072?s=200&v=4" style="height:32px"/>deployment
- [coordinates](https://github.com/illegal-dump/coordinates), app written in Kotlin <img src="https://kotlinlang.org/assets/images/favicon.svg" style="height:32px" />, Quarkus <img src="https://raw.githubusercontent.com/github/explore/4a0bdb9141afd8d9be5d6b8d6b22eb40be88f665/topics/quarkus/quarkus.png" style="height:32px"/> and PostgreSQL <img src="https://www.postgresql.org/media/img/about/press/elephant.png" style="height:32px"/>  
- ...
- [k8](https://github.com/illegal-dump/.github/tree/main/k8) - complete set of ymls for illegal-dump project (all above projects)


As a part of training deployment will take place locally (minikube) and on AWS.

<br/><br/><br/>

# Architecture

![uml](http://www.plantuml.com/plantuml/png/VL9VYzD047_VJp4So5aa83w93yU93uUeXwAWK7sO9fDqoMOtDplRyv1-TwUxboQrXtreTkRtP_xiNaT1bZGu4tlhHsGSeA4MavDlz5lUEjlvWRn0hN_4nbn2LLN6CDM2ldC4VTeGUnAAyCSODRCjrWBVQOFZg2dGt_e-Hp_zyrsYrI_022LZzWV7zH0srf766Jf6ngnnj5M7GlVueEhRc_UtF-33NF6cGCLIkO_KHH_lGk36UbJsr4mzfzIp3-AiVt6NaFiKYzE2aIMN9o9W6WCByR_SANzMHaUgUwrr-5IHU4TyLkY0PM63WXkC11VJIPMVGvIEwUkNZwiB5SwaCjE-BF8uzQVWhGIslik4FC78OI3PKegvz1nEX8wnHOyPVJohPpQ-IvG8rhGZBtbfsFPOHYYvgKeHx8_lf5mpL6oxhLHN9tTqkOYKVVNaAiyfouN16tZryXc45aGRRcsjlKc0UakArUYHzTaqDBhmC1pQNFt7JxrUdtWPiqILVTowjdu2EMf5uR8A7Mn-mbcsgAdWKsEUMLoJRzBW_W80)

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


## 4. Install PostgreSQL via helm

See [PostgreSQL](https://github.com/illegal-dump/coordinates) instruction via helm

## 5. Apply yml-s from k8 folder

```
kubectl apply -f k8/
```

and go to [http://minikube.local:30080](http://minikube.local:30080)

![..](doc/../../doc/screeenshots.gif)

<br/><br/><br/>


---

### kubectl Cheat Sheet

[https://kubernetes.io/docs/reference/kubectl/cheatsheet/](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)


---

### Attribution
icons: [https://www.vecteezy.com/free-vector/dump](https://www.vecteezy.com/free-vector/dump)

map: [https://www.openstreetmap.org/](https://www.openstreetmap.org/) and [https://leafletjs.com](https://leafletjs.com)

