Run this [Nginx][] image with:

    $ docker run -d --name nginx-0 -v /var/www/nginx-0/htdocs:/var/www/localhost/htdocs -p 80:80 wking/nginx

[volume-mounting][volume-mount] your content under the container's
`/var/www/localhost/htdocs`.  You can also mount volumes from other
containers and serve their data, although you may need to tweak the
config to serve from an alternative location.  Adjusting this image to
serve from a configurable `$HTTP_ROOT` wouldn't be too difficult
either.

[Nginx]: http://nginx.org/
[volume-mount]: http://docs.docker.io/en/latest/use/working_with_volumes/
