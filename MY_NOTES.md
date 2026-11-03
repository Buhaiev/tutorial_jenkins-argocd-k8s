# Notes made during project implementation
**During every tutorial project, I make notes on what I had to do to achieve the goal. These notes are stored here.**

1) I ran the tutorial with Amazon Linux instead of Ubuntu. This also means I installed an amazon-corretto Java. I installed Java 21, since Java 17 with Jenkins is outdated.
2) The image link describing what exactly to do in sshd_config is faulty and shows no image. However, key creation and connection per ssh from Jenkins master to agent worked without any additional changes; I suspect the options I was expected to uncomment in sshd_config were enabled by default.
3) Jenkins agent hostname is still set as "Jenkins-Master", likely a typo.
4) The list of plugins is once again inaccessible. I installed Maven Integration plugin, ...
5) The link to the original project is also lost! I went to the creator's Github page, found a similar-looking repository and included it here. The original tutorial from https://devcloudninjas.github.io/DevOps-Projects/ did not include any code. In addition, I had to write add the Dockerfile manually.
6) SonarQube server uses Adoptium to install a JDK; however, it is installable without Adoptium on Amazon Linux.
7) The link for downloading SonarQube is invalid; I had to download version 26. This version needs Java 21, not 17.
8) "Enable local webhooks validation" setting should be unset in order to allow webhook creation within the VPC.
9) The lombrok version is too old and had to be changed in pom.xml
10) Of course, AWS CLI is already installed on an Amazon Linux instance.
11) eksctl moved to another repository(eksctl-io instead of weaveworks).
12) The second repository's Jenkinsfile had the target repository set as the original repo, it had to be changed manually. 