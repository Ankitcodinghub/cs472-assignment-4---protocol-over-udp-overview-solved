# cs472-assignment-4---protocol-over-udp-overview-solved
**TO GET THIS SOLUTION VISIT:** [CS472 Assignment 4 – Protocol over UDP Overview Solved](https://www.ankitcodinghub.com/product/cs472-assignment-4-protocol-over-udp-overview-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;121132&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS472  Assignment 4 - Protocol over UDP Overview Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
This assignment will be a little different that our other programming assignments. There will be a programming component and a non-programming component. Most of the work you will need to do is in the non-programming component. This will reinforce that as a computer scientist you will often times need to go into code developed by others and understand it.

The code in this repository is intended to simulate a transport layer protocol and an application protocol. The code for the transport protocol is in du-proto.c and du-proto.h. Because getting access to IP directly from C code is not easy, the du-proto is built on top of UDP. This protocol works slightly different for clients and servers.

Transport Protocol du-proto

For clients, the initial starting point is to call dpClientInit(), passing the IP address of the server and the port number the server is listening on as arguments. For servers, they are started with dpServerInit(), passing the port number that the server will be using as an argument. Servers are then started with the dplisten() call, which blocks until a client connects via the dpconnect() call. After that both the clients and servers use dpsend() and dprecev() to exchange data with each other.

Application Protocol du-ftp

The application protocol implements a very simple FTP solution. Familiarize yourself with the code in du-ftp.c and du-ftp.h. The provided makefile builds a du-ftp executable that can be started in either client mode or server mode (see its arguments). It uses the du-proto protocol to transfer a file from the client to the server. By default the client file must exist under the .outfile directory and the server writes this file to the .infile directory. As it stands now the du-ftp is more of a hard coded file transfer solution, you will have some work to convert into a minimal application protocol. This will be described below.

Non programming assignment

Deliverables:

1. Go through the code in du-proto.c and make sure you understand it.

For each function, come up with the most appropriate description/comment block and include the function name and description in the written.pdf file.

2. I used a 3 sub-layers for various parts of transport model. If you look at dpsend() and dprecv(), each one of these is supported by two additional helper functions. For example dpsend() with dpsenddgram() and dpsendraw(). The same model is used by dprecv(). What are the specific responsibilities of these layers? Do you think this is a good design? If so, why. If not, how can it be improved?

3. Describe how sequence numbers are used in the du-proto? Why do you think we update the sequence number for things that must be acknowledged (aka ACK response)?

4. To keep things as simple as possible, the du-proto protocol requires that every send be ACKd before the next send is allowed. Can you think of at least one example of a limitation of this approach vs traditional TCP? Any insight into how this also simplified the implementation fo the du-proto protocol?

5. We looked at how to program with TCP sockets all term. This is the first example of the UDP programming interface we looked at. Breifly describe some of the differences associated with setting up and managing UDP sockets as compared to TCP sockets.

Programming

Please submit a zip file containing all the files required for your program to run along with the Makefile. Just submitting the files you have modified won’t be enough.

Deliverables:

1. Take a close look at dpsend() and dprecv(). Currently they will respond with an error if the amount of data to send is larger than DP_MAX_BUFF_SZ (in du-proto.h). Note that the du-proto was built with a maximum datagram of DP_MAX_BUFF_SZ, however dpsend() and dprecv() can be extended somewhat simply to send and receive data of arbitrary length. They both take a pointer to a buffer and the size of the buffer. Please update the code to address this feature, and test it via the dp-ftp client.

2. The du-ftp code is supposed to represent an application protocol. Currently the way its developed its not really a protocol. For example, it relies on the file names to be external to the protocol, there is no way for the clients and servers of du-ftp to exchange error information (for example, file not found), and so on. Thus, your goal is to turn du-ftp into a VERY SIMPLE file exchange protocol. You need to do the following:

Define a PDU for your protocol enhancements. You can look at how the pdu was used in my take on a transport protocol in duproto.h for inspiration. The PDU should allow du-ftp clients and servers to exchange things like the name of the file it is sending over, status on sending and receiving data, exchanging possible errors, and gracefully closing the file. Place this pdu definition in duftp.h using a C style typedef.

Modify du-ftp.c to send send data in larger blocks between the client and server. The default implementation is 500 bytes per exchange which is less that the du-proto max datagram size of 512. Given you fixed this above in deliverable 1, use larger send and receive messages to excercise your improvements.

Extra Credit

1. Currently the dp-proto does not do any retries or any sort of recover to react to errors. Try to implement some retry logic to harden the solution. Note that I placed a helper routine in the code called dprand() that you can use to try to simulate some random conditions.

2. Currently dp-proto just excahanges sequence numbers but it doesnt do anything to validate that the sequence numbers it gets are correct or expected. Add code to the implementation to support this feature.

3. Currently the underlying sockets used by dp-proto block until a request is received. Reasearch and look into how to configure the UDP socket properties to time out after a reasonable peroid of time (e.g., 10 seconds), implement these changes, and update the code with proper behavior on what to do in a timeout situation.
