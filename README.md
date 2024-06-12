# TCP_Demo
# Demo of BSD socket programs ... server ... client.
#
# Server:
#    Opens a listening socket.  Command-line arg specifies 'port'.
#    ... waits for connection (from client)
#    Accepts connection from client
#    Uses 'select()' to monitor (new) client socket as well as other connection requests on the 'listen' socket.
#    Loops receiving messages from client ... echos message back.  Very simplistic ... can't handle spaces in messages
#
# Client:
#    Creates a socket ... requests connection to server at specified IP (v4) address and port
#    User types message at command-line
#    Message is sent to 'server'
#    Looks for 'echo' message
#    Also uses 'select()' to monitor socket ... overkill since there's only one socket
#
# Usage:
#     TCP_server.exe <port>
#
#     TCP_client.exe <IP-addr-of-svr> <svr-port>
#
# Example:
#     TCP_server.exe 25555
#
#     TCP_client.exe 127.0.0.1 25555
#
# Build:
#    make
#
# Clean:
#    make clean
