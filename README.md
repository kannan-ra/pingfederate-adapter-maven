
#### Maven Build
Traditionally PingIdentity SDK provide Ant build for their adapter development. This project is just a template to get started with.

#### Build Instructions

The main compile time dependency from the Vendor is
```
<dependency>
    <groupId>pingfederate</groupId>
    <artifactId>pf-protocolengine</artifactId>
    <version>8.2.0.12</version>
</dependency>
```

Install this library locally from source from `<pf_install>/server/default/lib`.
Or remote deploy this to repo managers like Nexus or Artifactory

```
mvn clean install
```

#### Metadata for PF
The jar would be packaged with `PF-INF/<adapater>` file which contains the class name of the adapter