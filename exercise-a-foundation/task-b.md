# Exercise A - Foundation - Task B

We will be working with these files in this exercise.

- [jenkins/Dockerfile](jenkins/Dockerfile)
- [jenkins/jenkins.yaml](jenkins/jenkins.yaml)
- [jenkins/plugins.txt](jenkins/plugins.txt)

## Task 1: Use Explicit Version of Jenkins

It is recommended to explicitly use a specific version of Jenkins, even for Jenkins LTS versions. It improves traceability.

Check the version of the Jenkins LTS we are running on the lower left corner of the Jenkins web user interface.

Hints:

```patch
@@ -1,4 +1,4 @@
--- a/exercise-a-foundation/jenkins/Dockerfile
+++ b/exercise-a-foundation/jenkins/Dockerfile
-FROM docker.io/jenkins/jenkins:lts
+FROM docker.io/jenkins/jenkins:2.249.1

 LABEL maintainer="Leonard Sheng Sheng Lee <leonard.sheng.sheng.lee@gmail.com>"

```

- Run `make`. See [Makefile](Makefile) for more information.
- Open [http://localhost:8080](http://localhost:8080) to access Jenkins.
