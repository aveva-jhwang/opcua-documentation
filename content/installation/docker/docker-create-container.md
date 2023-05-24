---
uid: DockerCreateContainer
---

# Create a Docker container

To create a Docker container that runs the adapter, follow the instructions below.

1. Create the following `Dockerfile` in the directory where you want to create and run the container.

    **Note:** `Dockerfile` is the required name of the file. Use the variation according to your operating system:

    **ARM32**
    
    ```dockerfile
    FROM ubuntu:20.04
    WORKDIR /
    RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y ca-certificates libicu66 libssl1.1 curl
    COPY opcuadockerstart.sh /
    RUN chmod +x /opcuadockerstart.sh
    ADD ./AVEVA-Adapter-for-OpcUa_1.4.0.196-arm_.tar.gz .
    ENTRYPOINT ["/opcuadockerstart.sh"]
    ```

    **ARM64**

    ```dockerfile
    FROM ubuntu:20.04
    WORKDIR /
    RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y ca-certificates libicu66 libssl1.1 curl
    COPY opcuadockerstart.sh /
    RUN chmod +x /opcuadockerstart.sh
    ADD ./AVEVA-Adapter-for-OpcUa_1.4.0.196-arm64_.tar.gz .
    ENTRYPOINT ["/opcuadockerstart.sh"]
    ```
    
	**AMD64 (x64)**

    ```dockerfile
    FROM ubuntu:20.04
    WORKDIR /
    RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y ca-certificates libicu66 libssl1.1 curl
    COPY opcuadockerstart.sh /
    RUN chmod +x /opcuadockerstart.sh
    ADD ./AVEVA-Adapter-for-OpcUa_1.4.0.196-x64_.tar.gz .
    ENTRYPOINT ["/opcuadockerstart.sh"]
    ```

2. Copy the <code>[!include[installer](../_includes/inline/installer-name.md)]-<var>platform</var>_.tar.gz</code> file to the same directory as the `Dockerfile`.

3. Copy the <code>[!include[startup-script](../_includes/inline/startup-script.md)]</code> script to the same directory as the `Dockerfile`.

4. Run the following command line in the same directory (`sudo` may be necessary):

    ```bash
    docker build -t opcuaadapter .
    ```