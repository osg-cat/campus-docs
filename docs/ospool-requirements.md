# OSPool Contribution Requirements

## Supported Cluster OSes and HTCondor Versions

In the table below,
the OS is what you provide on the login and worker nodes;
the HTCondor version is what we will provide via our services.

| OS                                                                                                       | HTCondor                | Notes                                                                                                |
|----------------------------------------------------------------------------------------------------------|-------------------------|------------------------------------------------------------------------------------------------------|
| Enterprise Linux 7&nbsp;(*)                                                                              | 23.10.*                 | Enterprise Linux 7 is no longer supported, and thus our ability to support such systems may be removed at any time. |
| Enterprise&nbsp;Linux&nbsp;8&nbsp;(*)                                                                    | 25.*&nbsp;(>&nbsp;25.0) |                                                                                                      |
| Enterprise&nbsp;Linux&nbsp;9&nbsp;(*)                                                                    | 25.*&nbsp;(>&nbsp;25.0) |                                                                                                      |
| Enterprise&nbsp;Linux&nbsp;10&nbsp;(*)                                                                   | 25.*&nbsp;(>&nbsp;25.0) |                                                                                                      |
| Debian&nbsp;12&nbsp;(bookworm)                                                                           | 25.*&nbsp;(>&nbsp;25.0) |                                                                                                      |
| Debian&nbsp;13&nbsp;(trixie)                                                                             | 25.*&nbsp;(>&nbsp;25.0) |                                                                                                      |
| Ubuntu&nbsp;22.04&nbsp;(jammy)                                                                           | 25.*&nbsp;(>&nbsp;25.0) |                                                                                                      |
| Ubuntu&nbsp;24.04&nbsp;(noble)                                                                           | 25.*&nbsp;(>&nbsp;25.0) |                                                                                                      |
| Ubuntu&nbsp;26.04&nbsp;(resolute)                                                                        | 25.*&nbsp;(>&nbsp;25.0) |                                                                                                      |
| (*)&nbsp;Tested&nbsp;variants&nbsp;are&nbsp;CentOS Stream,&nbsp;Alma,&nbsp;and&nbsp;Rocky. {: colspan=2} |                         | &#8288 {: style="padding:0"}                                                                         |


## Contributing via a Hosted CE

### The cluster and login node are set up for our user account

-   The cluster is operational and generally works
-   The user account has a home directory on the login node
-   The user account can read, write, and execute files and directories within its home directory
-   Our home directory has enough available space and inodes (TBD but not a lot)
-   PATh staff know the right partition (and other batch system config) to use
-   PATh staff know the correct path to the batch-system binaries
-   The following Linux tools are installed and the user account can execute them:
    awk, bash, cat, cp, cut, date, grep, ln, mkdir, mv, printf, python, rm, rsync, sed, true, uname
-   The batch system is configured to allow the user account to submit jobs to the right partition(s) and for the default job “shape” (e.g., 1 core, 2 GB memory, and 24-hour maximum run time)
    
### It is possible to SSH from the CE to the login node:

-   PATh staff know the current hostname of your login node
-   That hostname has a public DNS entry that resolves to the correct IP address
-   PATh staff know the user account name (default, “osg01”)
-   PATh staff know about SSH configuration details to use (e.g., alternate port, jump host)
-   The SSH client on one of our IP addresses can connect to your login node (through firewalls, etc.)
-   The provided SSH public key has been installed in the right place and with the right permissions
-   The provided SSH public key is sufficient for authentication by your SSH server

### The worker nodes on which our jobs may run are ready:

-   Our home directory is shared with each cluster node
-   PATh staff know the correct path to scratch space for jobs (ideally on each worker node, but a shared filesystem may work)
-   Our user account can create subdirectories and run executables in the scratch directory
-   The worker nodes have permissive outbound network connectivity to the Internet (default allow, please note specific restrictions)


## Feedback

Do you have questions or comments about this page?
What could we do better?
If so, please email us at [support@osg-htc.org](mailto:support@osg-htc.org)!
