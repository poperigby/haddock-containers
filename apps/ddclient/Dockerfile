FROM archlinux:latest

LABEL name="ddclient"
LABEL maintainer="PopeRigby <poperigby@mailbox.org>"
LABEL org.opencontainers.image.source="https://github.com/poperigby/haddock-containers"

# Install ddclient
RUN pacman -Syyu --noconfirm ddclient

# Clean up cache
RUN pacman -Scc --noconfirm

VOLUME ["/var/cache/ddclient", "/etc/ddclient"]

ENTRYPOINT ["ddclient"]
CMD ["-foreground"]
