## UDP Socket based Chat Server in C#

I wrote this project to practice and learn about UDP networking, my goal is to better understand how to handle networking traffic.

Additional goals are to make it predictable and (reasonably) reliable networking solution using UDP bulding out an acknowledgement system by myself. 

Eventually compare it to a similar application that utilize TCP sockets and compare the reliability, performance and overhead.

This project is written in C# but has a recursive main loop for reading from the network buffer, which will eventually cause an StackOverflowException if the server is under constant incoming traffic.

### TODO:
- [ ] Broadcast user messages from active users
- [ ] Disconnect users when they dont send ack's 
	- [ ] Retry sending messages a couple of times during a reasonable timeframe
    - [ ] If no ack is received, remove them from the active endpoint list
- [ ] Broadcast connection and disconnections to active users
