# FacebookMessenger

## Introduction

##  Overview

A chat application is a software program that enables users to communicate with each
other in real-time over a network. It allows individuals to exchange messages, files, and
other forms of media instantaneously. In this overview, we will discuss a simple chat
application implemented using Java programming language.

Java is a widely-used, platform-independent programming language known for its
simplicity, robustness, and versatility. It provides a rich set of libraries and frameworks
that make it suitable for developing various types of applications, including chat applications.

The simple chat application we will discuss consists of a client-server architecture.
The server acts as a central hub that receives and distributes messages between connected clients. The clients establish a connection to the server and send/receive messages through this connection.

Here’s a high-level overview of the components and their functionalities in our Java-based chat application:

## Server:
Listens for incoming client connections on a specific port. Maintains a list of connected clients. Receives messages from clients and broadcasts them to all connected
clients. Handles new client connections and disconnections. Client:
Establishes a connection to the server using the server’s IP address and port. Sends
messages to the server for distribution. Receives messages from the server and displays
them to the user.

## User Interface:

Provides a graphical or command-line interface for users to interact with the chat
application. Displays messages sent by other users. Allows users to enter and send
messages. The communication between the server and clients is typically based on
sockets, which provide a reliable, bidirectional data stream between networked devices.
Java’s Socket and ServerSocket classes can be utilized to establish these connections.
To enhance the chat application, additional features can be implemented, such as
private messaging, user authentication, file sharing, and chat room management. These





# Design Goals/Objectives

Develop a User Interface: The project aims to create a graphical user interface (GUI) for
a chat application. The user interface includes various components such as text fields,
buttons, and panels to facilitate user interaction and messaging.

Implement Secure Communication: The project focuses on implementing security
measures to ensure secure communication between users. The AES encryption algorithm is used to encrypt and decrypt messages, providing confidentiality and data integrity.

Compress Messages: The project includes the implementation of Huffman coding
to compress messages before sending them. This helps in reducing the message size
and optimizing data transmission.

Real-Time Communication: The chat application facilitates real-time communication between users. It establishes a socket connection to enable instant messaging and
updates the chat interface dynamically to display incoming messages.

Personalization: The application allows users to customize their profile by displaying their name, status, and profile picture. This adds a personal touch and enhances the
user experience.

User Interaction: The project focuses on handling user interactions such as sending
messages, displaying received messages, and updating the chat interface accordingly. It
incorporates event handling mechanisms to capture user actions and respond appropriately

# Project Details

In this section, we will delve into the details of the project, discussing its various components and functionalities.

## Subsection_name
Figure 2.1: Server-Client Architecture The figure illustrates the high-level architecture
of the chat application, showcasing the server acting as a central hub for message distribution and clients establishing connections to communicate.


Figure 2.1: Server Connection

3. Implementation

The implementation details of the project are discussed in this section, covering various
subsections that provide insights into the workflow, tools, libraries, and implementation
details.

## Subsection_name
This is just a sample subsection. Subsections should be written in detail. Subsections
may include the following, in addition to others from your own project.
## The workflow
The workflow of the chat application includes the following steps:
The server starts and listens for incoming client connections. Clients establish connections with the server using the server’s IP address and port. Clients send messages
to the server for distribution. The server receives messages from clients and broadcasts
them to all connected clients. Clients receive messages from the server and display
them to the user.
## Tools and libraries
The project utilizes the following tools and libraries:
Java programming language: It forms the foundation of the project, providing the
necessary functionalities for socket communication, user interface, and network programming.
Socket programming: The Java Socket and ServerSocket classes are used to establish connections and facilitate communication between the server and clients.
Graphical User Interface (GUI) library: Java’s Swing or JavaFX can be employed
to create a user-friendly and interactive interface for the chat application.



- Source Code Link

<https://github.com/pan78m/CSE/tree/master/Algorithm/Project/Messenger>

[https://github.com/pan78m/CSE/tree/master/Algorithm/Project/GroupChattingApplication](https://github.com/pan78m/CSE/tree/master/Algorithm/Project/Group Chatting Application)

Implementation details (with screenshots and programming codes)

![](Aspose.Words.95e27f7a-d81e-49a9-9b66-1a6785bc9666.007.png)

Figure 2.2: How work AES Algorithm

12

![](Aspose.Words.95e27f7a-d81e-49a9-9b66-1a6785bc9666.008.png)

Figure 2.3: Code

![](Aspose.Words.95e27f7a-d81e-49a9-9b66-1a6785bc9666.009.png)

Figure 2.4: Huffman Coding

13

![](Aspose.Words.95e27f7a-d81e-49a9-9b66-1a6785bc9666.010.png)

Figure 2.5: Encrypted message

# Algorithms
The algorithms used in the project revolve around socket communication, message distribution, and client-server interaction. They include:
Server initialization algorithm Client connection algorithm Message distribution algorithm
-Bullet points can also be included anywhere in this project report.

# Algorithm 1: Huffman Algorithm


## Input
- Your Input

## Output
- Your Output

## Data
- Testing set x

## Algorithm Steps
1. Initialize:
   - Set ∑ (sigma) to represent the summation.
   - Set i to start from 1.
   - Initialize ∑(i=1 to ∞) to 0. (Comment: this is a comment)

2. Huffman Algorithm Implementation:
   ```c
   Huffman(c):
       n = |c|
       Q = c

       for i <- 1 to n-1:
           temp <- get node()
           left(temp) <- GetMin(Q)
           right(temp) <- GetMin(Q)
           a = left(temp)
           b = right(temp)
           F(temp) <- f(a) + f(b)
           insert(Q, temp)

       return GetMin(Q)



The algorithms used in the project revolve around socket communication, message distribution, and client-server interaction. They include:
Server initialization algorithm Client connection algorithm Message distribution algorithm


# Algorithm 2: AES

## Input
- Plaintext: array of bytes
- Key: array of bytes

## Output
- Cipher-text: array of bytes

## Constants
- Nb: number of columns (32-bit words) in the state matrix (Nb = 4)
- Nr: number of rounds based on the key size
  - Nr = 10 for 128-bit key
  - Nr = 12 for 192-bit key
  - Nr = 14 for 256-bit key

## Algorithm Steps
1. **KeyExpansion:** Generate the round keys from the original key.
2. **InitialRound:**
   - AddRoundKey: XOR the state matrix with the initial round key.
3. **Rounds:**
   - For round = 1 to Nr - 1:
     - SubBytes: Substitute each byte of the state matrix with a corresponding byte from the S-Box.
     - ShiftRows: Shift the rows of the state matrix.
     - MixColumns: Mix the columns of the state matrix.
     - AddRoundKey: XOR the state matrix with the round key for the current round.
4. **FinalRound:**
   - SubBytes: Substitute each byte of the state matrix with a corresponding byte from the S-Box.
   - ShiftRows: Shift the rows of the state matrix.
   - AddRoundKey: XOR the state matrix with the round key for the final round.

## Output
- The resulting state matrix is the ciphertext.





# Results Analysis/Testing

This chapter presents the results of the implemented chat application project and pro- videos a general discussion of how these results were achieved. It also addresses any problems that were detected during the implementation and highlights the attributes touched by the project problem.

The implemented chat application successfully provides a user-friendly platform for real-time communication. Users can connect to the server, exchange messages, and engage in interactive conversations. The application’s functionality aligns with the initial project objectives of simplicity, reliability, and customization potential.

During the implementation process, several challenges and considerations emerged. These included:

Scalability: As the number of connected clients increases, the application’s performance and scalability should be carefully evaluated. Implementing efficient message distribution mechanisms and optimizing network communication are crucial to maintaining responsiveness and ensuring a seamless user experience.

Security: While the initial implementation focuses on basic functionality, the project
should consider incorporating security measures to protect user data and prevent unauthorized access. This may include user authentication, encryption of messages, and
secure communication protocols.

User Interface Design: The user interface plays a significant role in the overall user
experience. Enhancements to the interface design, such as improved visual aesthetics,
intuitive navigation, and efficient message display, can further enhance the usability of
the application.

Error Handling: Robust error handling mechanisms should be implemented to handle various scenarios, such as network interruptions, server/client disconnects, or mes- sage transmission failures. Clear error messages and graceful handling of exceptions can help users understand and recover from potential issues.

Cross-Platform Compatibility: The project should ensure compatibility with different operating systems and devices. Testing the chat application on various platforms and
addressing any platform-specific challenges will enhance its accessibility and usability.

## Result_individual Message_1

The results of any specific part of your project can be included using subsections.

![](Aspose.Words.95e27f7a-d81e-49a9-9b66-1a6785bc9666.011.png)

Figure 3.1: Message Chatting each other

## Result_Group message_2

Each result must include screenshots from your project. In addition to screenshots, graphs should be added accordingly to your project.

![](Aspose.Words.95e27f7a-d81e-49a9-9b66-1a6785bc9666.012.png)

Figure 3.2: Group message


# Discussion
In this chapter, the design, development, and implementation of a chat application using Java programming language were discussed. The project aimed to create a user-friendly and reliable platform for real-time communication, addressing various attributes such as knowledge depth, conflicting requirements, analysis depth, familiarity of issues, applicable codes, stakeholder involvement, and interdependence. The project success- fully achieved its objectives by implementing a client-server architecture, incorporating socket programming, and providing a seamless communication experience. How- ever, challenges related to scalability, security, user interface design, error handling, and cross-platform compatibility were identified, indicating areas for further improvement. Overall, the project demonstrated the successful creation of a functional chat application while acknowledging the need for future enhancements.




References

1. https://www.github.com
1. Group<a name="_page21_x89.86_y250.35"></a> Chat Application geekforceek. [https://www.geeksforgeeks.org/ a-group-chat-application-in-java/?ref=gcse. Accessed](https://www.geeksforgeeks.org/a-group-chat-application-in-java/?ref=gcse) 



## How to run this Project
- Go  to Messenger/src/Chat  folder
- Find the server dot java file
- First of all run the server dot java file then 
- Run user1 and user2 
- But reminder that sometimes shows some error because you need to connect any local server. Then this error do not shows next time

- You can run same way for Group chatting Part in the project.


## You can find project proposal [![PDF](<pdf (2).png>)](https://www.overleaf.com/read/hxnsznvkqmbj#a30969)

## Code of Sources

To deploy this project run

```bash
  Messenger/src/Chat
```
```bash
  Group Chatting Application/src/group/chatting/application
```




## Social

[![YouTube](https://img.shields.io/badge/YouTube-red?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/@pan78mtricks)

[![FACEBOOK](https://img.shields.io/badge/Facebook-Connect-brightgreen?style=for-the-badge&labelColor=black&logo=facebook)](https://www.facebook.com/pankaj.mahanto.78)

[![Linkedin](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](linkedin.com/in/pankaj-mahanto78/)

[![YouTube](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://x.com/mahanto_pankaj?t=uSysV9y-QMHIzqo-PIL3sA&s=08)



## Authors

[![Github](<github (1).png>)](https://www.github.com/pankaj-arya)

[![Gmail](https://img.shields.io/badge/just%20the%20message-8A2BE2)](https://www.google.com/gmail)
# You can find project report [![PDF](<pdf (2).png>)](https://www.overleaf.com/read/pkqvpwbsfkdd#091c8c)


