*Build g4klx M17Gateway*
```
git clone https://github.com/g4klx/M17Gateway
cd M17Gateway
make
```

*Build g4klx M17GatewayLink*
```
git clone https://github.com/Paulo-D2000/m17-cxx-demod.git --branch GatewayLink_M17Rtx-dev
cd GatewayLink_M17Rtx-dev
mkdir build
cd build
cmake ..
make
make test
sudo make install
```

*Configure & Run M17Gateway*

Find ```M17Gateway/M17Gateway.ini```
Remove # from ```#Startup=M17-M17_C```and change to the desired reflector name
Start ```./M17Gateway/M17Gateway``` 


*Run M17GatewayLink*
start ```./GatewayLink_M17Rtx-dev/build/m17-gateway-link.cpp | play -b 16 -r 48000 -c1 -t s16 -``` 
