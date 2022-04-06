# ubuntu_janus_webRTC

<br>

sudo apt-get install libmicrohttpd-dev libjansson-dev libnice-dev libssl-dev libsrtp2-dev libsofia-sip-ua-dev libglib2.0-dev libopus-dev libogg-dev libcurl4-openssl-dev pkg-config gengetopt libtool automake cmake libconfig-dev  <br>


wget https://github.com/cisco/libsrtp/archive/v2.0.0.tar.gz  <br>
tar xzvf v2.0.0.tar.gz   <br>
cd libsrtp-2.0.0/  <br> 
./configure --prefix=/usr --enable-openssl <br>
make shared_library && sudo make install <br>

<br>
sudo apt-get install g++<br>
git clone git://git.libwebsockets.org/libwebsockets<br>
cd libwebsockets<br>
mkdir build<br>
cd build<br>
cmake -DCMAKE_INSTALL_PREFIX:PATH=/usr -DCMAKE_C_FLAGS="-fpic" ..<br>
make && sudo make install<br>
<br>
<br>
git clone https://github.com/meetecho/janus-gateway.git<br>
cd janus-gateway<br>
sh autogen.sh<br>
./configure --prefix=/usr/local --enable-libsrtp2 --enable-openssl --disable-aes-gcm --enable-nss<br>
make && sudo make install<br>
<br>
<br>
<br>
Demo 띄우기<br>
<br>
npm install -g local-web-server<br>
cd janus-gateway/html<br>
ws --http2<br>
<br>
<br>
https


수정중..
