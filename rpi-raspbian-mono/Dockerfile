# This acts as an overlay on top of rpi raspian to add in the needed mono files

# To Build
# docker build -t asofttech/rpi-raspbian-mono:4.2.2.30 .

FROM resin/rpi-raspbian:jessie

#based on dockerfile by Michael Friis <friism@gmail.com> / Jo Shields <jo.shields@xamarin.com>

# Install curl
RUN apt-get update \
	&& apt-get install -y curl \
	&& rm -rf /var/lib/apt/lists/*

# Add newer mono repo to list
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
RUN echo "deb http://download.mono-project.com/repo/debian wheezy/snapshots/4.2.2.30 main" > /etc/apt/sources.list.d/mono-xamarin.list

# Install mono
RUN apt-get update \
	&& apt-get install -y mono-devel mono-complete \
	&& apt-get install -y ca-certificates-mono fsharp mono-vbnc nuget \
	&& rm -rf /var/lib/apt/lists/*

