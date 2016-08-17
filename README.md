
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


## Dependency Evaluation

Used [DependencyFinder](http://depfind.sourceforge.net/) to find the dependency for the class. Download and extract the archive. Run the GUI tool `./bin/DependencyFinder`.
Select the compiled jar and computing the dependency graph will be display below

```
com.pingidentity.adapter.idp
    SampleSubnetAdapter
    SampleSubnetAdapter$1
    SampleSubnetAdapter$IPv4FieldValidator
com.pingidentity.sdk *
    AuthnAdapterResponse *
    AuthnAdapterResponse$AUTHN_STATUS *
    IdpAuthenticationAdapterV2 *
java.io *
    IOException *
    PrintStream *
java.lang *
    Exception *
    IllegalArgumentException *
    Integer *
    Object *
    String *
    StringBuilder *
    System *
    UnsupportedOperationException *
java.net *
    Inet6Address *
    InetAddress *
java.util *
    HashMap *
    HashSet *
    Map *
    Set *
javax.servlet.http *
    HttpServletRequest *
    HttpServletResponse *
org.sourceid.saml20.adapter *
    AuthnAdapterDescriptor *
    AuthnAdapterException *
    ConfigurableAuthnAdapter *
org.sourceid.saml20.adapter.conf *
    Configuration *
    Field *
org.sourceid.saml20.adapter.gui *
    AdapterConfigurationGuiDescriptor *
    FieldDescriptor *
    TextFieldDescriptor *
org.sourceid.saml20.adapter.gui.validation *
    FieldValidator *
    ValidationException *
org.sourceid.saml20.adapter.idp.authn *
    AuthnPolicy *
    IdpAuthnAdapterDescriptor *
```