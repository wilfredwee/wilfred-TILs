# Running a server on Guest OS and connecting to it from Host OS

Assuming: You're NAT-ed and have set up port forwarding.

Because 127.0.0.1 is a loopback address, you can't run it on 127.0.0.1, the Host OS will not be able to connect to it.
<br /><br />
You'll have to run it on 0.0.0.0, then on the host OS, visit `http://127.0.0.1:<forwarded port>`
