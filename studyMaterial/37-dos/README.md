# 37. DoS. Denial of Service 

## What is “denial of service”?
A denial of service occurs when a legitimate user is denied access to a network, system, device, or other resources that they are otherwise authorized to access. That can include their email, e-banking account, public online services, etc.

Denial of service can result from a cyber attack known as a denial of service attack (DoS), whose explicit aim is to achieve this effect.

## Protection Against Denial of Service Attacks
While DoS attacks are less challenging to stop or prevent, DDoS attacks can still present a serious threat.

Prevent spoofing: Check that traffic has a source address consistent with the set of addresses for its stated site of origin and use filters to stop dial-up connections from spoofing.

Limit broadcasting: Often attacks will send requests to every device on the network, amplifying the attack. Limiting or turning off broadcast forwarding where possible can disrupt attacks. Users can also disable echo and chargen services where possible.

Streamline incident response: Honing your incident response can help your security team respond quickly when DoS attacks are detected.

Protect endpoints: Ensure that all endpoints are patched to eliminate known vulnerabilities. Endpoints capable of running EDR agents should have them installed.

Dial in firewalls: Ensure your firewalls are limiting ingress and egress traffic across the perimeter wherever possible.

Monitor the network: The more you know about what normal inbound traffic looks like, the quicker you'll spot the start of a DDoS attack. Real-time visibility with network detection and response (NDR) is an efficient and reliable way to maintain a profile of what your network should look like (using machine learning) so you can detect suspicious surges immediately.


## Types of DDoS Attacks
### SMURF ATTACK
A smurf attack is a DDoS attack that sends packets spoofing the victim's source IP. When devices on the network attempt to respond, the amount of traffic slows the targeted device to the point of being unusable.

### SYN FLOOD
A SYN flood attack opens many connections with the target target server and then never closes them. The attacker, acting as a client, sends a SYN message. When the server responds with a SYN-ACK, the malicious client never sends an ACK message. In this way the server is forced to keep numerous connections open, taxing it's resources until it fails.

### LAYER 7 DDOS ATTACK
A Layer 7 DDoS attack (or application attack) targets a specific service instead of an entire network. These are becoming increasingly more common than broad network attacks.

## Resources
https://www.cisa.gov/uscert/ncas/tips/ST04-015
https://crashtest-security.com/denial-of-service-attack/
https://www.extrahop.com/resources/attacks/dos/
https://www.techtarget.com/searchsecurity/definition/denial-of-service
