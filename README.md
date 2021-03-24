# my-nginx-image
A simple nginx docker image base on nginx-alpine image to learn k8s

### build
docker build . -t your-repository/SomeName:SomeTag

### usage

```bash
docker pull dogrich/my-nginx:v1
docker run -d -p 80:80 --name test dogrich/my-nginx:v1
curl 127.0.0.1
<h1>my-nginx:alpine | 1eeecbf34f5f | 172.17.0.2:80 | version:v5</h1>

# request custom html file
docker rm -f test
docker run -d -p 80:80 -v /usr/share/nginx/html/:/usr/share/nginx/html --name test dogrich/my-nginx:v1
echo "hello, world" > /usr/share/nginx/html/test.html
curl 127.0.0.1/test.html
hello, world
```


