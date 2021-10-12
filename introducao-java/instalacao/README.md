## Instalação no Linux (Ubuntu)

### Java 10

    $ sudo add-apt-repository ppa:linuxuprising/java
    $ sudo apt update
    $ sudo apt-get install oracle-java10-installer

    $ export JAVA_HOME="/usr/lib/jvm/java-10-oracle"
    $ export PATH=$JAVA_HOME/bin:$PATH

    $ java -version

## Ferramentas de build

### Gradle (no site mostra como fazer)
- https://gradle.org/ 
- Versão instalada 4.7
- Ganhando popularidade (Android)
- Usa linguagem de programação Groovy
- Instalação:
  
        $ mkdir /opt/gradle
        $ unzip -d /opt/gradle gradle-4.7-bin.zip
        $ ls /opt/gradle/gradle-4.7
        $ export PATH=$PATH:/opt/gradle/gradle-4.7/bin
        $ sudo apt purge gradle // old versions
        $ gradle -v

### Maven
- https://maven.apache.org/
- Versão instalada 3.5.3
- Legados do ANT
- Baseado em XML
- Instalação:

        $ unzip -d /opt/maven apache-maven-3.5.3-bin.zip
        $ ls opt/maven/apace-maven-3.5.3
        $ sudo apt purge maven // old versions
        $ export PATH:$PATH:opt/maven/apache-maven-3.5.3/bin
        $ mvn -v

### Wrappers
- [Maven Wrapper](https://github.com/takari/maven-wrapper)
- [Gradle Wrapper](https://docs.gradle.org/current/userguide/gradle_wrapper.html)
