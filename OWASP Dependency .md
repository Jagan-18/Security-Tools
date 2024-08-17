

## Refer URL: https://github.com/jeremylong/DependencyCheck/blob/main/README.md





Commamd Step's:
==============

  -  sudo apt update

# S1: Check the Java version.
   -  java --version
   - sudo apt install openjdk-17-jre-headless

# S2 :For internet Access Enable for that Clone the github-repo for the existing on internet. 

   - git clone <https://github.com/........>

# S3: Dewnload the package for installation  of OS Dependency and leux machine.

   - $ VERSION=$(curl -s https://jeremylong.github.io/DependencyCheck/current.txt)

    - $ curl -Ls "https://github.com/jeremylong/DependencyCheck/releases/download/v$VERSION/dependency-check-$VERSION-release.zip" --output dependency-check.zip

   - sudo apt install unzip
   - unzip dependecy-check.zip
   - ls
   - rm -rf dependecy-check.zip
   - ls         ------------------> (Ex: Ekart, dependency check)
