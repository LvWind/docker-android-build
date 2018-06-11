# docker-android-build
Docker image to build android apps for drone CI.

---

Docker image:
```
docker pull lvwind/docker-android-build
```

drone config `.drone.yml` example:

```yml
pipeline:
  build:
    image: lvwind/docker-android-build
    environment:
      - ENDPOINT_OVERRIDE=true
    commands:
      - ./gradlew assemble
```