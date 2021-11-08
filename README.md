# ft_irc

team project of 42 school where it is necessary to implement own simple IRC server.

Internet Relay Chat is a legacy application layer protocol for real-time messaging. designed for group communication, also allows you to communicate through private messages and share files. on the basis of IRC, many messengers were later developed.

the project is based on the [RFC 1459](https://datatracker.ietf.org/doc/html/rfc1459) standard. 

the server does not support server-to-server communication.

## how to use it

**to launch the server:**
```
make
./ircserv 6667 1234
```
**to launch the client:**
```
nc 127.0.0.1 6667
HERE SHOULD BE \r\n					!!!
```

## implemented commands

### PRIVMSG
params: `<receiver>{,<receiver>}` `<text to be sent>`

used for private correspondence between users. also exists the ability to send messages to channels.

### JOIN
params: `<channel>{,<channel>}` `[<key>{,<key>}]`

used by the client to enter the channel. if a password is set, it must be correct. when users enter a channel, they will receive a notification about all users on the channel.

if there was no group before, then the group is created

### INVITE
params: `<nickname>` `<channel>`

used to invite users to the channel. if the channel is open, then only the channel operator can invite to it.


### development team
[ngamora](https://github.com/zagaynov-andrew)

[mteressa](https://github.com/Fkhalilullin)

[constbar](https://github.com/constbar)





<!-- _QUIT(msg, &user);
<!-- _KILL(msg, &user); -->

<!-- _CAP(msg, *user); -->
<!-- _PASS(msg, *user); -->
<!-- _PING(msg, *user); -->
<!-- _NICK(msg, &user); -->
<!-- _USER(msg, *user); -->

<!-- _NOTICE(msg); -->
<!-- _PART(msg, *user); -->
<!-- _LIST(msg, *user); -->
<!-- _OPER(msg, *user); -->
<!-- _KICK(msg, *user); -->
<!-- _NAMES(msg, *user); -->
<!-- _TOPIC(msg, *user); -->
