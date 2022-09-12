# cs372_project2
Traceroute


Instructions
Below you will find the skeleton code for the client. You are to update the skeleton code to achieve the following objectives.

Objectives:

Update the __validateIcmpReplyPacketWithOriginalPingData() function:
Confirm the following items received are the same as what was sent:
sequence number
packet identifier
raw data
Set the valid data variable in the IcmpPacket_EchoReply class based the outcome of the data comparison.
Create variables within the IcmpPacket_EchoReply class that identify whether each value that can be obtained from the class is valid. 
For example, the IcmpPacket_EchoReply class has an IcmpIdentifier. Create a variable, such as IcmpIdentifier_isValid, along with a getter
function, such as getIcmpIdentifier_isValid(), and setting function, such as setIcmpIdentifier_isValid(), so you can easily track and
identify which data points within the echo reply are valid. Note: There are similar examples within the current skeleton code.
Create debug messages that show the expected and the actual values along with the result of the comparison.
Update the printResultToConsole() function:
Identify if the echo response is valid and report the error information details. For example, if the raw data is different, print to
the console what the expected value and the actual value.
Currently, the program calculates the round-trip time for each packet and prints it out individually. Modify the code to correspond to 
the way the standard ping program works. You will need to report the minimum, maximum, and average RTTs at the end of all pings from the 
client. In addition, calculate the packet loss rate (in percentage). It is recommended to create an output that is easily readable with 
the amount of data used for a trace route since a ping is the foundation for such functionality.
Your program can only detect timeouts in receiving ICMP echo responses. Modify the Pinger program to parse the ICMP response error codes 
and display the corresponding error results to the user. Examples of ICMP response error codes are 0: Destination Network Unreachable, 
1: Destination Host Unreachable. 
Ref: https://www.iana.org/assignments/icmp-parameters/icmp-parameters.xhtml (Links to an external site.)
The skeleton code currently has a placeholder for performing a trace route function. It starts with the traceRoute() function and uses 
private functions to carry out the implementation. Update the __sendIcmpTraceRoute() function to perform this task.
