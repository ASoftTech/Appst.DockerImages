# Readme

## Overview

This is a series of Docker files I've used which come in quite handy

### rpi-raspbian-mono

This image is a debian jessie image with mono added on top, currently at version 4.2.2.30 <br>
I've used resin/rpi-raspbian:jessie as the base image as it seems to be the most popular on Docker at the moment

### rpi-raspbian-aspnet-mono

This image is based on top of rpi-raspbian-mono and adds the needed bits in order to run the new aspnet mvc6 sites <br>
This is similar to the microsoft/aspnet image but it's different in that it's designed to be used on a raspberry pi arm platform
instead of an x86 / x64 platform. This image is currently set for use with rc1.

### rpi-raspbian-aspnet-coreclr

This image is based on top of resin/rpi-raspbian:jessie, again it targets the raspberry pi / arm platform <br>
This currently doesn't work as there isn't a arm compiled version of coreclr, but it maybe useful at some point in the future.
