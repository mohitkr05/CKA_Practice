
# Read more about the Tips and Tricks about the exam [here](https://docs.linuxfoundation.org/tc-docs/certification/tips-cka-and-ckad)


1. Root privileges can be obtained by running 'sudo −i'.
2. Rebooting of your server IS permitted at any time.
3. Do not stop or tamper with the certerminal process as this will END YOUR EXAM SESSION.
4. Do not block incoming ports 8080/tcp, 4505/tcp and 4506/tcp. This includes firewall rules that are found within the distribution's default firewall configuration files as well as interactive firewall commands.
5. Use Ctrl+Alt+W instead of Ctrl+W.
5.1 Ctrl+W is a keyboard shortcut that will close the current tab in Google Chrome.
6. Ctrl+C & and Ctrl+V are not supported in your exam terminal. To copy and paste text, please use;
6.1 For Linux: select text for copy and middle button for paste (or both left and right simultaneously if you have no middle button).
6.2 For Mac: ⌘+C to copy and ⌘+V to paste.
6.3 For Windows: Ctrl+Insert to copy and Shift+Insert to paste.
7. In addition, you might find it helpful to use the Notepad (see top menu under 'Exam Controls') to manipulate text before pasting to the command line.
8. Installation of services and applications included in this exam may require modification of system security policies to successfully complete.
9. Only a single terminal console is available during the exam. Terminal multiplexers such as GNU Screen and tmux can be used to create virtual consoles.


# CKA Clusters

|Cluser |Members |CNI |Description |
| :------------- | :----------: | -----------: | -----------: |
|k8s  | 1 master, 2 worker| flannel | k8s cluster |
|hk8s | 1 master, 2 worker| calico| k8s cluster |
|bk8s | 1 master, 1 worker|flannel |k8s cluster |
|wk8s |1 master, 2 worker |flannel |k8s cluster |
|ek8s |1 master, 2 worker |flannel |k8s cluster |
|ik8s |1 master, 1 base node|loopback|k8s cluster − missing worker node |

- At the start of each task you'll be provided with the command to ensure you are on the correct cluster to complete the task.
- Nodes making up each cluster can be reached via ssh, using a command such as the following: ssh <nodename>
- You can assume elevated privileges on any node by issuing the following command: sudo -i
- You can also use sudo to execute commands with elevated privileges at any time
- You must return to the base node (hostname node-1) after completing each task.
Nested−ssh is not supported.
- You can use kubectl and the appropriate context to work on any cluster from the base node. When connected to a cluster member via ssh, you will only be able to work on that particular cluster via kubectl.
- Further instructions for connecting to cluster nodes will be provided in the appropriate tasks
- Where no explicit namespace is specified, the default namespace should be acted upon.
- If you need to destroy/recreate a resource to perform a certain task, it is your responsibility to back up the resource definition appropriately prior to destroying the resource.
- The CKA & CKAD environments are currently running Kubernetes v1.21.
- The CKA, CKS and CKAD exam environment will be aligned with the most recent K8s minor version within approximately 4 to 8 weeks of the K8s release date
  
