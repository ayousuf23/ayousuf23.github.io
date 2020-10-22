---
title: "Chat"
collection: portfolio
created: June 2020
order: 1060
---
Chat is a chat application created using C# and .NET Core. The program consists of two programs. The first is a central server program that forwards messages to clients (which are the instances of the client-side chat program program). The second is a client program that sends and receives messages to and from the server program. The benefit of this approach is that clients do not need to handle port forwarding. Both programs are multi-threaded (you can think of a thread as a virtual processor). Although using multiple threads is hard to manage and write code for, it can be beneficial because the UI thread can remain responsive while the non-UI thread can focus on networking and data processing tasks.  

The program uses individual sockets for networking rather than HTTP or other high level protocols.  
