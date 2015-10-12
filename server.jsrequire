
 
var http = require('http');

//Lets define a port we want to listen to
var server_port = process.env.OPENSHIFT_NODEJS_PORT || 8080;
var server_ip_address = process.env.OPENSHIFT_NODEJS_IP || '127.0.0.1';
//What is a port?
//Why port 80?
//Why do we this? 
//What does it do?

var nomo = require('node-monkey').start({host:server_ip_address, port:'8000'} );

//We need a function which handles requests and send response
function handleRequest(request, response){
    response.end('Yes! It Works!! Path Hit: ' + server_ip_address + ":" + server_port + "/" + request.url);
    console.log("my server ip address is: " + server_ip_address);
}


//Create a server
var server = http.createServer(handleRequest);
//What is a server object?
//Why do we this? 
//What does it do?

//Lets start our server
server.listen(server_port, server_ip_address, function(){
    //Callback triggered when server is successfully listening. Hurray!
    console.log("HTTP Server listening on: " + server_ip_address + ":" + server_port);
});

