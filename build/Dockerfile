ARG runtime="nvidia"
FROM nvidia/cuda:8.0-runtime-ubuntu16.04

LABEL "maintainer"="Chris Diehl <cultclassik@gmail.com>"

# NVidia required env vars
ENV NVIDIA_VISIBLE_DEVICES=0
ENV NVIDIA_DRIVER_CAPABILITIES="compute,utility"

ENV MINER_FILE="Zec.miner.0.3.4b.Linux.Bin.tar.gz"
ENV MINER_URL="https://github.com/nanopool/ewbf-miner/releases/download/v0.3.4b/${MINER_FILE}"

RUN apt-get update && apt-get install -y --no-install-recommends \
    wget \
 && rm -rf /var/lib/apt/lists/* \
 && mkdir /miner \
 && wget --no-check-certificate $MINER_URL \
 && tar -xvf $MINER_FILE -C /miner --strip-components 1 \
 && rm $MINER_FILE

WORKDIR /miner

# API port
EXPOSE 42000/tcp

ENTRYPOINT [ "/bin/bash", "/miner/miner" ]
CMD [ "--server", "hostname", "--port", "port", "--user", "user", "--pass", "pass", "--telemetry", "0.0.0.0:42000 ]
