FROM openjdk:27-ea-trixie as dps

WORKDIR /build

COPY --chmod=0755 mvnw mvnw

COPY .mvn/ .mvn/

RUN --mount=type=bind,source=pom.xml,target=pom.xml \
    --mount=type=cache,target=/root/.m2 ./mvnw dependency:go-offline -DskipTests




