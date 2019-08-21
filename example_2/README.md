# Example 2

The tree:

```
.
├── Makefile                      # run make dep to get cage into this folder
├── cage                          # is in .gitignore
├── pods                          # now contains two services.
│   ├── common.env                # empty
│   ├── service_1.yml             # This contains two containers in one "service", a db and another container
│   ├── service_2.yml             # Contains an external container, gruntworks shellcheck
│   └── targets                   # Contains two environments to play around with
│       ├── development
│       └── production
├── src                           # not there in your example, as this is the mounted src code...
│   └── bash-commons
│       ├── CODEOWNERS
│       ├── Dockerfile.bats
│       ├── Dockerfile.shellcheck
│       ├── LICENSE
│       ├── NOTICE
│       ├── README.md
│       ├── docker-compose.yml
│       ├── modules
│       └── test
└── src_service1                  # again an httpd:2-alpine image...
    └── Dockerfile
```

## Tasks For You

0.  build the test/image.
1.  Bring up the whole stack.
1.  Source mount "bash-commons"
1.  Change the image to 2.4 or 2-alpine
1.  Rebuild the image
1.  Now deploy to the production environment (and hopefully watch a postgres:9.4 being deployed)
1.  Shut down everything.
