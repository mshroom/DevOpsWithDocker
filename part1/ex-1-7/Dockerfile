FROM ubuntu:16.04
RUN apt-get update && apt-get install -y curl wget 
COPY curler.sh .
CMD ["/bin/bash","curler.sh"]
