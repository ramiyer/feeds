
A simple feed processor based on Storm

To run on a local cluster:

```bash
lein run -m feeds.topology/run!
# OR
lein run -m feeds.topology/run! debug false workers 10
```

To run on a distributed cluster:

```bash
lein uberjar
# copy jar to nimbus, and then on nimbus:
bin/storm jar path/to/uberjar.jar feeds.TopologySubmitter workers 30 debug false
```


## License

Distributed under the Eclipse Public License, the same as Clojure.
