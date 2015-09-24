# Elastic Crate Cluster Template for Giant Swarm

This is a simple service definition that gets you an elastic Crate cluster with Docker on [Giant Swarm](https://giantswarm.io/).

Check out the full guide here:

https://blog.giantswarm.io/BLA/

## Prerequisites 

* A [Dedicated Giant Swarm Cluster](https://giantswarm.io/request-invite/)
* The [swarm CLI](https://docs.giantswarm.io/reference/cli/installation/) installed

## Usage

If you just want to run a Crate cluster just by itself as a separate service:

1. Clone the [`swarm.json`](giantswarm-clojure/swarm.json) in this repo. 
2. Run `swarm up`.

__Note:__ You might need to [expose](https://docs.giantswarm.io/reference/swarm-json/#expose) port 4300 so you can use the Crate cluster from other services.

Alternatively, copy the component from the swarm.json to your own and connect it to your other components as you see fit.

### Scaling

For scaling your Crate cluster up or down use [`swarm scaleup`](https://docs.giantswarm.io/reference/cli/scaleup/) or [`swarm scaledown`](https://docs.giantswarm.io/reference/cli/scaledown/) on the component.

### Multiple Clusters

If you want to set up multiple Crate cluster, just duplicate the component, with a new component name, cluster name, and domain.

## Further Reading

For more details on configuration options and usage of Crate, see the [Docker Hub repo of the image](https://hub.docker.com/_/crate/) or the [Crate documentation](https://crate.io/docs/).