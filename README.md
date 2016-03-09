Docker Flow
===========

Summary
---

Demo
---

License
-------
[MIT License](http://opensource.org/licenses/MIT)

TODO
----

* Tests
* Submit to jenkins-ci.org

Misc
----

```bash
docker-machine create \
    -d virtualbox \
    docker-flow

eval "$(docker-machine env docker-flow)"

export CONSUL_IP=$(docker-machine ip docker-flow)

docker run -d \
    -p "8500:8500" \
    -h "$CONSUL_IP" \
    --name "consul" \
    progrium/consul -server -bootstrap
```