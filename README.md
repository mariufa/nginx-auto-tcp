# nginx-auto-tcp

docker run -d --name nginx-gen --network=test --volumes-from nginx    -v /var/^Cn/docker.sock:/tmp/docker.sock:ro    -v /tmp/templates:/etc/docker-gen/templates    -t jwilder/docker-gen -notify-sighup nginx -watch -only-exposed /etc/docker-gen/templates/nginx.tmpl /etc/nginx/stream.d/default.conf

 docker run -d -p 80:80 -p 5432:5432 --name nginx --network=test -v /home/marius/git/nginx-auto-tcp/nginx.conf:/etc/nginx/nginx.conf -v /tmp/nginx:/etc/nginx/stream.d -t nginx