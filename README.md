# Axon Framework — Spring Cloud Extension

Distributed Axon command routing through Spring Cloud discovery and an HTTP command bus connector. This extension handles command distribution; it does not provide an event store.

This is the LeaseBlocks fork of [AxonFramework/extension-springcloud](https://github.com/AxonFramework/extension-springcloud), included as a submodule in the LeaseBlocks workspace. [pom.xml](pom.xml) defines this checkout's artifact and dependency versions.

## Build and test

Use JDK 17 or later and the checked-in Maven wrapper from this directory:

```sh
./mvnw clean verify
./mvnw -Dcoverage clean verify
```

On JDK 17+, the `java17-modules` profile automatically includes the Spring Boot 3 and Spring Boot 4 integration-test modules. The `coverage` property adds the aggregate coverage module. Dependency and plugin versions are maintained in the parent and module POMs.

Integration tests use Testcontainers and require Docker.

## Modules

- [springcloud](springcloud/): core extension.
- [springcloud-spring-boot-autoconfigure](springcloud-spring-boot-autoconfigure/): Spring Boot configuration.
- [springcloud-spring-boot-starter](springcloud-spring-boot-starter/): starter dependency bundle.
- [springcloud-spring-boot-3-integrationtests](springcloud-spring-boot-3-integrationtests/) and [springcloud-spring-boot-4-integrationtests](springcloud-spring-boot-4-integrationtests/): framework integration checks.
- [coverage-report](coverage-report/): aggregate coverage reports.

## Documentation and license

See the [local documentation](docs/README.md) and [upstream reference guide](https://docs.axoniq.io/spring-cloud-extension-reference/latest/). The upstream guide follows its own release; check this checkout's source and POMs when behavior differs.

Upstream support: [AxonIQ forum](https://discuss.axoniq.io/) and [issue tracker](https://github.com/AxonFramework/extension-springcloud/issues).

Licensed under [Apache 2.0](LICENSE.txt).
