FROM ubuntu:22.04
RUN apt-get update -y && apt-get install -y fortune cowsay lolcat
ENV PATH=/usr/games:$PATH
CMD ["sh", "-c", "fortune | cowsay | lolcat -f"]
