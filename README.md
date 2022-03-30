# ubuntu_janus_webRTC



sudo apt-get install libmicrohttpd-dev libjansson-dev libnice-dev libssl-dev libsrtp2-dev libsofia-sip-ua-dev libglib2.0-dev libopus-dev libogg-dev libcurl4-openssl-dev pkg-config gengetopt libtool automake cmake libconfig-dev


wget https://github.com/cisco/libsrtp/archive/v2.0.0.tar.gz
tar xzvf v2.0.0.tar.gz
cd libsrtp-2.0.0/
./configure --prefix=/usr --enable-openssl
make shared_library && sudo make install


sudo apt-get install g++
git clone git://git.libwebsockets.org/libwebsockets
cd libwebsockets
mkdir build
cd build
cmake -DCMAKE_INSTALL_PREFIX:PATH=/usr -DCMAKE_C_FLAGS="-fpic" ..
make && sudo make install


git clone https://github.com/meetecho/janus-gateway.git
cd janus-gateway
sh autogen.sh
./configure --prefix=/usr/local --enable-libsrtp2 --enable-openssl --disable-aes-gcm --enable-nss
make && sudo make install



Demo 띄우기

npm install -g local-web-server
cd janus-gateway/html
ws --http2


https



