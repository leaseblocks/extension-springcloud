# Spring Cloud extension agent instructions

- This is the LeaseBlocks fork; use local [pom.xml](pom.xml) versions rather than assuming parity with upstream or sibling extensions.
- Keep command routing and HTTP transport in [springcloud](springcloud/), and Spring Boot wiring in [springcloud-spring-boot-autoconfigure](springcloud-spring-boot-autoconfigure/).
- Honor module compiler settings: the core inherits Java 8 source/target; the Boot integration modules declare their own Java settings.
- Review discovery capabilities, member selection, and HTTP dispatch/reply handling together when changing distributed routing. This extension transports commands and does not provide an event store.
- Keep Spring Boot registration and conditional configuration aligned with both Boot 3 and Boot 4 integration modules; JDK 17+ activates these through `java17-modules`.
- Integration tests use Testcontainers; an unavailable Docker runtime is a validation limitation, not a passing test result.
- Keep upstream license notices and attribution. Build commands and module links are in [README.md](README.md).
