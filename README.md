# Java---Simple-Websocket-Server
My website is https://rbtrading.ca

On my website I'm using the following to initialize the websocket and I want the websocket to be secure so I'm using wss accordingly...


            function connect() {         


                console.log("connecting");
   

                wsocket = new WebSocket("wss://www.rbtrading.ca:74");  

                wsocket.onopen = onopen;
                wsocket.onmessage = onmessage;
                wsocket.onclose = onclose; 


            }


I have a simple bare-bones server programmed in Java.  The intention is to host a website over https.

The StartWebsocketServer uses a standard Socket to receive the input stream but it is encrypted.   I need to decode this somehow.  The "Sec-WebSocket-Key" must be visible to initialize a handshake with the websocket.   

StartWebsocketServer_version2 attempts initialize an SSLSocket but always returns 0 bytes.  Why?
