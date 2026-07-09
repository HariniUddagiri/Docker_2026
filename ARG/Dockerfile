ARG version
FROM almalinux:${version:-9}
#ENV course="DevOps with AWS" \
   # trainer="Harini" \
   # duration="120HRS"
#here username is key, Harini is default value
ARG USERNAME=Harini
#ENV USERNAME=$USERNAME
RUN echo "Hello User: ${USERNAME}, image version: ${version}" > /tmp/devops.txt
CMD ["sleep", "100"]