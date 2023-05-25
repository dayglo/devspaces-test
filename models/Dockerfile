FROM dso-quay-registry-quay-quay-enterprise.apps.ocp1.azure.dso.digital.mod.uk/dso-project/jq-curl:latest

RUN adduser -D -h /models -u 1000 models 

WORKDIR /models

USER 1000

RUN mkdir -p /models/inception_resnet_v2 /models/tfhub_module && \
    wget -O /tmp/inception_resnet_v2.tar.gz https://storage.googleapis.com/tfhub-modules/google/faster_rcnn/openimages_v4/inception_resnet_v2/1.tar.gz && \
    wget -O /tmp/tfmodule_v1.tar https://tfhub.dev/google/openimages_v4/ssd/mobilenet_v2/1?tf-hub-format=compressed && \
    tar -vxf /tmp/inception_resnet_v2.tar.gz -C /models/inception_resnet_v2 && \
    tar -vxf /tmp/tfmodule_v1.tar -C /models/tfhub_module && \
    rm -f /tmp/inception_resnet_v2.tar.gz /tmp/tfmodule_v1.tar 

VOLUME /models

ENTRYPOINT ["tail", "-f", "/dev/null"]