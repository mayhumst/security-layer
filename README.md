# security-layer

This project utilizes the Repy_V2 sandbox environment found [here](https://github.com/SeattleTestbed/docs/blob/master/Programming/RepyV2Tutorial.md) to create a security layer to enhance the security of basic repy functions. This project was completed for the Computer Security / ISP class in the NYU cybersecurity department Fall 2023. 

This project was threefold -- develop a security layer/reference monitor, write a series of tests to ensure its integrity (and test classmates' layers), and then refine the security layer to patch bugs. Included are my security layer and my attack programs. 

The reference monitor demonstrates three design paradigms: accuracy, efficiency, and security. 

- Accuracy: The defense monitor should precisely and consistently manage file operations. Only specific operations, such as writeat, should have their behavior modified. All situations that are not described in the specifications must match that of the underlying API.

- Efficiency: The security layer should use a minimum number of resources, so performance is not compromised. For example, you may not call readat() everytime writeat() is called. It is permissable to call readat() upon fileopen(), however.

- Security: The defense layer should be robust against tampering and circumvention. Attackers must not be able to bypass, disable, or exploit the defense monitor's enhanced behaviors, ensuring the integrity and intended functionality of file operations.

In addition, this security layer utilizes mutexes to protect against multithreaded attacks. 

**NOTE:** To run the attack cases, follow the instructions on Repy_V2 regarding proper download, setup, and terminal commands. 