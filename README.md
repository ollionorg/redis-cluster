# Helm Chart for Redis in Cluster Mode
> ## ⚠️ WARNING: Here be dragons 
> This code is extremely early alpha. Use at your own peril.

This is a helm chart that spins up a redis cluster with the associated stateful sets with the right settings in `redis.conf`. It supports the creation of a cluster with just masters or with slaves as well and provides the command to configure the cluster using `redis_trib.rb`. 

Eventually the goal is for it to provide several other potentially useful operations:
* Gracefully terminating and cleaning up associated resources (read, deleting the persistent volumes it created)
* Increase cluster size
* Reduce cluster size
* Reshard keys (in relation to increasing and reducing cluster size)

## TODO
* Execute the `redis_trib.rb` command presented at the end of the Helm chart automatically (probably by using a custom docker with the relevant packages installed)
* Move the Redis cluster container base image out into a public repository
