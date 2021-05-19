# Setup

### Clone Sphinx Repos
- clone all six Sphinx repos into a single dir

### Polar
- import Sphinx-Test-2 into Polar

### PostgreSQL
- make username postgres and password sphinx
- run cluster.sql to create tables

### Sphinx Proxy
- `go build`

### Sphinx Auth
- `go build`

### Sphinx Mqtt
- `go build`
- ./plugins/auth/authhttp/http.json
```
{
    "auth": "http://localhost:9090/mqtt/auth",
    "acl": "http://localhost:9090/mqtt/acl",
    "super": "http://localhost:9090/mqtt/superuser"
}
```

### Sphinx Tribes
- `go build`

### Sphinx Meme
- `go build`

### Sphinx Relay
- `npm install`

# Testing
- set up cluster_config.json
- set path to Sphinx dir as config.path
- `node ./testing/cluster-test.js`