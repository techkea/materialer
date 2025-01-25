# Docker Cheatsheet

**Start en Container fra et Image**
    
> `docker run ubuntu` (Ubuntu er Image navnet)    

**Adgang til container gennem terminalen**

> `docker run -it ubuntu`    
>  -i : interactive    
>  -t : Teletypewriter (terminalen) 

**Adgang til container gennem http protokollen (browseren, Postman etc.)**

>  `docker run -p [host_port]:[container_port] IMAGE`    
>  `docker run -p 8080:80 nginx`    
>  -p : port mapping    

**Se en liste over Images**

> `docker images`

**Slet et image**

> `docker rmi <id_til_image>`    

**Se en liste over Containers**

> `docker ps`     

og ikke kørende containers     

> `docker ps -a`    
> -a : all    

**Download et image**    

> `docker pull ubuntu`    

**Kør container så den ikke blokerer terminalen**

> `docker run -d nginx`    
> -d : detached

**Slet (remove) en container når den slukkes**

> `docker run --rm  Ubuntu`    
> --rm : remove (after close)

**Tilføj miljøvariabler**

> `docker run -e GITHUB_TOKEN=xyz123dkajh`    
> -e : environement

**Del en mappe fra host til container**    

> `docker run -v /host/path:/container/path`    
> `docker run -v /user/clbo/flaskapp:/app`    
> `-v : volume`      

**Push et image til docker hub**    

> `docker login`    
> `docker push USERNAME/IMAGE`    

<!--
## Skab et netvæk mellem containers 

Dine containers skal have et fast navn    

> `docker run --name product_service`      

Dine containers skal være på det samme netværk (brug **bridge**, eller lav dit eget)       

> `docker run --network bridge`    

I din app.py kode (eller lign. sted) skal du ændre 

> `http://localhost:5000/products` til      
> `http://products_service:5000/products`      

-->