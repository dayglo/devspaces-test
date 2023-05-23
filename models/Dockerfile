FROM ubuntu:latest
WORKDIR /models
ADD https://storage.googleapis.com/tfhub-modules/google/faster_rcnn/openimages_v4/inception_resnet_v2/1.tar.gz /data
ADD https://tfhub.dev/google/openimages_v4/ssd/mobilenet_v2/1 /data
VOLUME /models
ENTRYPOINT ["tail", "-f", "/dev/null"]