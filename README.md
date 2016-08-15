
**(in progress)**

#### Maven Build
Traditionally PingIdentity SDK provide Ant build for their adapter development. This project is just an attempt on Maven build.


#### Build Instructions
Specify `pingfederate.home`

```
mvn -Dpingfederate.home=/var/lib/pingfederate-8.1.4/pingfederate clean install
```

#### PF Libs

[`addjars-maven-plugin`](https://code.google.com/archive/p/addjars-maven-plugin/) is used to specify the local pingfederate lib directories & it installs the jars in local Maven repository.

Would be much cleaner if we can explicitly [install pf dependencies](https://maven.apache.org/guides/mini/guide-3rd-party-jars-local.html) & specify them in the `pom.xml`. This will also make CI much easier.