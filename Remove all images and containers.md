# Docker: Remove all images and containers
Di 22 Oktober 2013
By Uli Köhler

Problem: You use Docker, but working with it created lots of images and containers. You want to remove all of them to save disk space.

Solution: Warning: This will destroy all your images and containers. It will not be possible to restore them!

Execute those commands in a shell:

```
#!/bin/bash
# Delete all containers
docker rm $(docker ps -a -q)
# Delete all images
docker rmi $(docker images -q)
```
