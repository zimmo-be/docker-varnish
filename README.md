# How to use this image

    varnish:
      image: zimmo-varnish:latest
      volumes:
        - project.vcl:/etc/varnish/default.vcl
      links:
        - nginx
      ports:
        - 80
    
    nginx:
      image: nginx:1.10-alpine
      volumes:
        - .:/var/www/html/
