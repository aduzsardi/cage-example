# Example Minimal

- One repository hosting all the source code for a pod docker-compose.
- Same repository hosting the infrastructure code.

The service consists of

- a db (postgres)
- a dummy service (httpd)

We will start it up, then change something and bring it down again.

The minimal things we need for that is:

- Two services [Pod, Service,...?](http://cage.faraday.io/basics)
- One environment (development)

## Tasks For You

0.  build the test/image.
1.  Bring up the whole stack.
1.  Source mount "src" ($ ./cage source mount src)
1.  Change the image to 2.4 or 2-alpine
1.  Rebuild the associated images.
1.  Restart the services
