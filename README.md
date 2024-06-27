<<<<<<< HEAD
# se2-freerider



## Getting started

To make it easy for you to get started with GitLab, here's a list of recommended next steps.

Already a pro? Just edit this README.md and make it your own. Want to make it easy? [Use the template at the bottom](#editing-this-readme)!

## Add your files

- [ ] [Create](https://docs.gitlab.com/ee/user/project/repository/web_editor.html#create-a-file) or [upload](https://docs.gitlab.com/ee/user/project/repository/web_editor.html#upload-a-file) files
- [ ] [Add files using the command line](https://docs.gitlab.com/ee/gitlab-basics/add-file.html#add-a-file-using-the-command-line) or push an existing Git repository with the following command:

```
cd existing_repo
git remote add origin https://gitlab.bht-berlin.de/s92532/se2-freerider.git
git branch -M main
git push -uf origin main
```

## Integrate with your tools

- [ ] [Set up project integrations](https://gitlab.bht-berlin.de/s92532/se2-freerider/-/settings/integrations)

## Collaborate with your team

- [ ] [Invite team members and collaborators](https://docs.gitlab.com/ee/user/project/members/)
- [ ] [Create a new merge request](https://docs.gitlab.com/ee/user/project/merge_requests/creating_merge_requests.html)
- [ ] [Automatically close issues from merge requests](https://docs.gitlab.com/ee/user/project/issues/managing_issues.html#closing-issues-automatically)
- [ ] [Enable merge request approvals](https://docs.gitlab.com/ee/user/project/merge_requests/approvals/)
- [ ] [Set auto-merge](https://docs.gitlab.com/ee/user/project/merge_requests/merge_when_pipeline_succeeds.html)

## Test and Deploy

Use the built-in continuous integration in GitLab.

- [ ] [Get started with GitLab CI/CD](https://docs.gitlab.com/ee/ci/quick_start/index.html)
- [ ] [Analyze your code for known vulnerabilities with Static Application Security Testing(SAST)](https://docs.gitlab.com/ee/user/application_security/sast/)
- [ ] [Deploy to Kubernetes, Amazon EC2, or Amazon ECS using Auto Deploy](https://docs.gitlab.com/ee/topics/autodevops/requirements.html)
- [ ] [Use pull-based deployments for improved Kubernetes management](https://docs.gitlab.com/ee/user/clusters/agent/)
- [ ] [Set up protected environments](https://docs.gitlab.com/ee/ci/environments/protected_environments.html)

***

# Editing this README

When you're ready to make this README your own, just edit this file and use the handy template below (or feel free to structure it however you want - this is just a starting point!). Thank you to [makeareadme.com](https://www.makeareadme.com/) for this template.

## Suggestions for a good README
Every project is different, so consider which of these sections apply to yours. The sections used in the template are suggestions for most open source projects. Also keep in mind that while a README can be too long and detailed, too long is better than too short. If you think your README is too long, consider utilizing another form of documentation rather than cutting out information.

## Name
Choose a self-explaining name for your project.

## Description
Let people know what your project can do specifically. Provide context and add a link to any reference visitors might be unfamiliar with. A list of Features or a Background subsection can also be added here. If there are alternatives to your project, this is a good place to list differentiating factors.

## Badges
On some READMEs, you may see small images that convey metadata, such as whether or not all the tests are passing for the project. You can use Shields to add some to your README. Many services also have instructions for adding a badge.

## Visuals
Depending on what you are making, it can be a good idea to include screenshots or even a video (you'll frequently see GIFs rather than actual videos). Tools like ttygif can help, but check out Asciinema for a more sophisticated method.

## Installation
Within a particular ecosystem, there may be a common way of installing things, such as using Yarn, NuGet, or Homebrew. However, consider the possibility that whoever is reading your README is a novice and would like more guidance. Listing specific steps helps remove ambiguity and gets people to using your project as quickly as possible. If it only runs in a specific context like a particular programming language version or operating system or has dependencies that have to be installed manually, also add a Requirements subsection.

## Usage
Use examples liberally, and show the expected output if you can. It's helpful to have inline the smallest example of usage that you can demonstrate, while providing links to more sophisticated examples if they are too long to reasonably include in the README.

## Support
Tell people where they can go to for help. It can be any combination of an issue tracker, a chat room, an email address, etc.

## Roadmap
If you have ideas for releases in the future, it is a good idea to list them in the README.

## Contributing
State if you are open to contributions and what your requirements are for accepting them.

For people who want to make changes to your project, it's helpful to have some documentation on how to get started. Perhaps there is a script that they should run or some environment variables that they need to set. Make these steps explicit. These instructions could also be useful to your future self.

You can also document commands to lint the code or run tests. These steps help to ensure high code quality and reduce the likelihood that the changes inadvertently break something. Having instructions for running tests is especially helpful if it requires external setup, such as starting a Selenium server for testing in a browser.

## Authors and acknowledgment
Show your appreciation to those who have contributed to the project.

## License
For open source projects, say how it is licensed.

## Project status
If you have run out of energy or time for your project, put a note at the top of the README saying that development has slowed down or stopped completely. Someone may choose to fork your project or volunteer to step in as a maintainer or owner, allowing your project to keep going. You can also make an explicit request for maintainers.
=======

<img src="https://maven.apache.org/images/maven-logo-black-on-white.png" alt="drawing" width="200"/>

## Assignment MB1: *Maven* Build & *JDBC* Database Access

In this assignment, database *FREERIDER_DB* from the previous assignment is accessed
from a Java program via the *JDBC* interface.

Technologies used:

- [*JDBC*](https://www.geeksforgeeks.org/introduction-to-jdbc) -
    the *Java Database Connectivity (JDBC)* interface is the earliest interface
    to access SQL-databases released in 1997. It is still the most commonly used
    interface. It is part of most other packages (e.g. `Spring Boot`, `Jakarta EE`)
    that build on it.

- [*Maven*](https://maven.apache.org) is used to acquire the *JDBC* package.
    *Maven* is a widely used *build tool* for Java
    ([*gradle*](https://gradle.org) is another widely used Java *build tool*).

  - The database-built is part of the project (under: `services/freerider_db` with
    `Dockerfile` for building the image for the container of the database service
    running *mysqld*).

  - [pom.xml](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html)
    (POM: Project Object Model) is the central file to control *maven* build.

- [Docker-compose](https://docs.docker.com/compose)
    is a tool set that simplifies image-build and container create, start/stop
    operations that is particularly useful when a project uses multiple containers.

  - [docker-compose.yml](https://docs.docker.com/get-started/08_using_compose)
    is the central file to control all container operations used in a project,
    their image-build processes and dependencies during start, e.g. the database
    container always must start first or other containers won't be able to open
    connections to the database.


### Challenges

- MB.1: [Get an Overview of Technologies](#mb1-get-an-overview-of-technologies) - (5 Pts)

- MB.2: [Project Setup](#mb2-project-setup) - (3 Pts)

- MB.3: [Build Database Service](#mb3-build-database-service) - (2 Pts)

- MB.4: [Build and Run JDBC-Client](#mb4-build-and-run-jdbc-client) - (5 Pts)


&nbsp;

### MB.1) Get an Overview of Technologies

Read about technologies and answer questions in each section.


#### a) *JDBC*

1. What is a database *Connection*? Which data is included?

1. What is a *Prepare*-statement? What is the result?

1. What is send from a client-program to the database?

1. What is a *Result Set*?

1. In which form do answers arrive from the database in a *Result Set*?


&nbsp;

#### b) *Docker-compose*

1. Name 3 most-commonly used commands with *docker-compose*.

1. What is `db-vol` in [docker-compose.yml](docker-compose.yml)?

1. Where must `Dockerfile` be located in the project according to [docker-compose.yml](docker-compose.yml)?

1. Where is `Dockerfile` be used for?

1. What does `3306:3306` mean in [docker-compose.yml](docker-compose.yml)?

1. How many *images* are used in the *image stack* of the created database container?


&nbsp;

#### c) *Maven*

1. What is a *build-process*?

1. What are `GAV` coordinates of a project?

1. What is *maven central*?

1. When does the *build-process* start and when does it end?

1. Name the steps (*"lifecycle"*) of the *maven* *build-process*.

1. What is `pom.xml`?

1. Which information does `pom.xml` include? Name three examples.

1. Where are `.jar` files pulled from *maven central* placed on a local system?

1. What is a *scaffold*?

1. Draw a *maven* scaffold for a project with *groupId:* `de.freerider` and
    *artifactId:* `jdbc-client`.

References:

- *Maven in five minutes*, [link](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html).

- Tim van Baarsen, *"Maven Cheat Sheet"*,
    [link](https://medium.com/@TimvanBaarsen/maven-cheat-sheet-45942d8c0b86).

- Digital Ocean, *"20+ Maven Commands and Options"*,
    [link](https://www.digitalocean.com/community/tutorials/maven-commands-options-cheat-sheet).



&nbsp;

### MB.2) Project Setup

Create a new directory for project *"se2-freerider"*:

```sh
mkdir se2-freerider                 # create new project directory
cd se2-freerider                    # change into directory

git init -b main                    # initialize for git with 'main' branch
touch .gitignore                    # create empty file .gitignore
git add .gitignore
git commit -m "initial commit, .gitignore"

git checkout -b maven-jdbc          # create new branch `maven-jdbc`, switch

# add link named 'downstream' pointing to the remote distribution repository
git remote add downstream https://github.com/sgra64/se2-freerider.git

# fetch branch 'maven-jdbc' from the remote repository
git fetch downstream maven-jdbc

# set local branch 'maven-jdbc' to track remote branch 'downstream/maven-jdbc'
git branch -u downstream/maven-jdbc maven-jdbc

# merge content of downstream branch into local branch 'maven-jdbc'
git merge --allow-unrelated-histories --strategy-option theirs downstream/maven-jdbc

```

The merge completes with no conflicts:

```
Auto-merging .gitignore
Merge made by the 'ort' strategy.
 .gitignore                                 |  77 +++++
 .vscode/settings.json                      |  34 ++
 FREERIDER_DB.session.sql                   |   1 +
 README.md                                  | 513 +++++++++++++++++++++++++++++
 docker-compose.yml                         |  26 ++
 services/freerider_db/Dockerfile           |  20 ++
 services/freerider_db/access.sql           |  25 ++
 services/freerider_db/datetime.txt         |  29 ++
 services/freerider_db/drop_data.sql        |   8 +
 services/freerider_db/howto.txt            |  62 ++++
 services/freerider_db/load_sample_data.sql |  28 ++
 services/freerider_db/schema.sql           |  44 +++
 12 files changed, 867 insertions(+)
 create mode 100644 .vscode/settings.json
 create mode 100644 FREERIDER_DB.session.sql
 create mode 100644 README.md
 create mode 100644 docker-compose.yml
 create mode 100644 services/freerider_db/Dockerfile
 create mode 100644 services/freerider_db/access.sql
 create mode 100644 services/freerider_db/datetime.txt
 create mode 100644 services/freerider_db/drop_data.sql
 create mode 100644 services/freerider_db/howto.txt
 create mode 100644 services/freerider_db/load_sample_data.sql
 create mode 100644 services/freerider_db/schema.sql
```

The local branch 'maven-jdbc' now has new files.

```sh
ls -la              # show content of project directory after merge
```
```
drwxr-xr-x 1 svgr2 Kein     0 Jun  7 01:05 .
drwxr-xr-x 1 svgr2 Kein     0 Jun  7 00:59 ..
drwxr-xr-x 1 svgr2 Kein     0 Jun  7 01:05 .git
-rw-r--r-- 1 svgr2 Kein  1329 Jun  7 01:05 .gitignore               <-- updated
drwxr-xr-x 1 svgr2 Kein     0 Jun  7 01:05 .vscode
-rw-r--r-- 1 svgr2 Kein   627 Jun  7 01:05 docker-compose.yml       <-- new
-rw-r--r-- 1 svgr2 Kein    24 Jun  7 01:05 FREERIDER_DB.session.sql <-- new
-rw-r--r-- 1 svgr2 Kein 14160 Jun  7 01:05 README.md                <-- new
drwxr-xr-x 1 svgr2 Kein     0 Jun  7 01:05 services                 <-- new
```

The [./services](./services) directory contains content for building and
running Docker containers:

```sh
find services       # show content of new services directory
```
```
services
services/freerider_db
services/freerider_db/access.sql
services/freerider_db/datetime.txt
services/freerider_db/Dockerfile
services/freerider_db/drop_data.sql
services/freerider_db/howto.txt
services/freerider_db/load_sample_data.sql
services/freerider_db/schema.sql
```


&nbsp;

### MB.3) Build Database Service

[Docker-compose](https://docs.docker.com/compose)
simplifies image-build and container create and start/stop operations.

[docker-compose.yml](docker-compose.yml)
is the central file to define all container assets (volumes, images) and
operations. It can include rules for the container-start order.
The database container always must start first or other containers may not
be able to open connections to the database.

[docker-compose.yml](docker-compose.yml)
currently defines one container (*"service"*) for the database
with name *"freerider_db"*:

```yml
# version: '3'
name: "freerider"

services:
  # database for the freerider reservation system
  mysqld:
    container_name: "freerider_db"
    # path to Dockerfile to build image
    build: "./services/freerider_db"
    image: "freerider/db-img:1.0"
    volumes:
      - "db-vol:/var/lib/mysql"
    environment:
      MYSQL_ALLOW_EMPTY_PASSWORD: "yes"
      MYSQL_ROOT_PASSWORD:
      # created via 'access.sql':
      # MYSQL_DATABASE: "FREERIDER_DB"
      # MYSQL_USER: "freerider"
      # MYSQL_PASSWORD: "free.ride"
    ports:
      - "3306:3306"
    # restart: "always"

volumes:
  # volume to store database data
  db-vol:
```

The section for service *"freerider_db"* defines the path to the directory
where [Dockerfile](services/freerider_db/Dockerfile) resides to build the
container image: *"freerider/db-img:1.0"*.

The container uses a volume: *"db-vol"* for holding the database data.
The container exposes port: *"3306"* as standard port for the database
server process *mysqld*.

The command to build all container assets (volumes, images) and create
and start containers is:

```sh
docker-compose up -d        # build and start container(s)
```

```sh
docker-compose logs -f      # show logs collected from container(s), -f: following
```

Container *"freerider_db"* is now running:

<img src="https://raw.githubusercontent.com/sgra64/se2-freerider/markup/maven-jdbc/docker_freerider_db.png" alt="drawing" width="800"/>

Database `FREERIDER_DB` does already exist as well as the user and password that
both have been configured into the container image.

Load data from
[services/freerider_db/load_sample_data.sql](services/freerider_db/load_sample_data.sql)
into the database.

An extension for *VSCode*:
[SQLTools](https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools)
allows to connect to the database from the IDE.

Install the extension, connect to the database using the following connection
information:

```
"server": "localhost",
"port": 3306,
"driver": "MySQL",
"database": "FREERIDER_DB",
"username": "freerider",
"password": "free.ride"
```

Run the query from file:
[FREERIDER_DB.session.sql](FREERIDER_DB.session.sql)

```sql
select * from CUSTOMER;
```

*SQLTools* will show the open connection (green dot) result of the query:

<img src="https://raw.githubusercontent.com/sgra64/se2-freerider/markup/maven-jdbc/sqltools_query.png" alt="drawing" width="800"/>



&nbsp;

### MB.4) Build and Run JDBC-Client

*Maven* is used to build the Java (*"jdbc-client"*) program.

Make sure *maven* is installed and its environment variables have been set
(*MAVEN_HOME* pointing to where *maven* is installed and *M2_HOME* with the
path where the local *maven* repository is located, usually in the *HOME*-directory):

```sh
mvn --version
echo $MAVEN_HOME $M2_HOME
```
```
Apache Maven 3.8.6
/c/opt/maven /c/Users/svgr2/.m2
```

If missing, set environment variables and add MAVEN_HOME to PATH:

```sh
# the MAVEN_HOME environment variable points to the installation directory
export MAVEN_HOME="/c/opt/maven"

# the M2_HOME environment variable points to the local package cache, usually
# a directory in the HOME-directory called '.m2'
export M2_HOME="$(cygpath ${HOMEPATH})/.m2"

# add MAVEN_HOME/bin to PATH to invoke the maven command 'mvn' in a terminal
export PATH="${PATH}:${MAVEN_HOME}/bin"
```

*Maven* assumes a certain project structure (*scaffold*) that can be
generated using a project's
[GAV](https://stackoverflow.com/questions/71835160/what-is-the-meaning-for-gav-in-maven-context) -
coordinates.

In the following step, the scaffold is created using *maven*.
Run commands in the project directory:

```sh
mvn archetype:generate -DinteractiveMode=false \
    -DgroupId="de.freerider" \
    -DartifactId="jdbc-client" \
    -Dversion="1.0.0-SNAPSHOT"
```
```
...
[INFO] BUILD SUCCESS
```

Result is a sub-directory in the project directory: `jdbc-client`.
This directory also holds `pom.xml`.

```sh
find jdbc-client
```
```
jdbc-client
jdbc-client/pom.xml             <-- pom.xml
jdbc-client/src                 <-- source code
jdbc-client/src/main
jdbc-client/src/main/java

jdbc-client/src/main/java/de    <-- packages start at src/main/java
jdbc-client/src/main/java/de/freerider
jdbc-client/src/main/java/de/freerider/App.java

jdbc-client/src/test            <-- JUnit test code (source)
jdbc-client/src/test/java
jdbc-client/src/test/java/de
jdbc-client/src/test/java/de/freerider
jdbc-client/src/test/java/de/freerider/AppTest.java
...
```

Open `jdbc-client/pom.xml` and add lines between the markers:

```xml
<project ... >
  <modelVersion>4.0.0</modelVersion>

  <groupId>de.freerider</groupId>
  <artifactId>jdbc-client</artifactId>
  <version>1.0.0-SNAPSHOT</version>

  <name>jdbc-client</name>
  <packaging>jar</packaging>
  <url>http://maven.apache.org</url>

  <!-- add lines -->
  <properties>  
    <maven.compiler.source>1.8</maven.compiler.source>
    <maven.compiler.target>1.8</maven.compiler.target>
  </properties>
  <!-- add lines -->

  <dependencies>
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>3.8.1</version>
      <scope>test</scope>
    </dependency>
  </dependencies>
</project>
```

Change to the `jdbc-client` directory and build the code:

```sh
cd jdbc-client
mvn clean compile package
...
[INFO] BUILD SUCCESS
```

Run the code:

```sh
mvn --quiet exec:java -Dexec.mainClass="de.freerider.App" -Dexec.args=""
```

Output:

```
Hello World!
```

Package code as `.jar`:

```sh
mvn package
...
[INFO] BUILD SUCCESS
```

The resulting `.jar`-file is in the `target` directory:

```sh
ls -la target
```
```
-rw-r--r-- 1 svgr2 Kein 2204 Jun  6 18:27 jdbc-client-1.0.0-SNAPSHOT.jar
```

Run the resulting `.jar`-file:

```sh
java -cp target/jdbc-client-1.0.0-SNAPSHOT.jar de.freerider.App
```
```
Hello World!
```

Create an *executable* `.jar` by adding a build-plugin to `pom.xml`
at the end of `pom.xml` (just before the closing `</project>` tag).
The plugin defines the class with the *main()* function to execute
when the `.jar` is started:

```xml
<build>
  <plugins>
    <plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-jar-plugin</artifactId>
    <version>2.4</version>
    <configuration>
        <archive>
        <manifest>
        <mainClass>de.freerider.App</mainClass>
        </manifest>
        </archive>
    </configuration>
    </plugin>
  </plugins>
</build>
```

Repackage and run `.jar`:

```sh
mvn package
java -jar target/jdbc-client-1.0.0-SNAPSHOT.jar
```
```
Hello World!
```

Add code to access the database to `src/main/java/de/freerider/App.java`:

```java
package de.freerider;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.ResultSet;
import java.sql.SQLException;
import java.sql.Statement;

public class App {
    // DB connection information
    static final String DB_URL  = "jdbc:mysql://localhost/FREERIDER_DB";
    static final String USER    = "freerider";
    static final String PASS    = "free.ride";

    // DB Query
    static final String QUERY   = "SELECT * FROM CUSTOMER;";

    public static void main(String[] args) {
        System.out.println( "Hello FREERIDER_DB!" );

        // Open a connection
        try(Connection conn = DriverManager.getConnection(DB_URL, USER, PASS)) {

            // create prepare-statement from connection
            Statement stmt = conn.createStatement();

            // send query to DB-server
            ResultSet rs = stmt.executeQuery(QUERY);

            // extract data from result set
            while(rs.next()) {
                // Retrieve by column name
                System.out.print("id: " + rs.getInt("ID"));
                System.out.print(", name: " + rs.getString("NAME"));
                System.out.print(", contact: " + rs.getString("CONTACT"));
                System.out.println(", status: " + rs.getString("STATUS"));
            }
        } catch(SQLException e) {
            e.printStackTrace();
        }
    }
}
```

Rebuild the application:

```sh
mvn compile package
...
[INFO] BUILD SUCCESS
```

While `compile` completes with `SUCCESS`, running the application:

```sh
mvn --quiet exec:java -Dexec.mainClass="de.freerider.App" -Dexec.args=""

# or as executable .jar:
java -jar target/jdbc-client-1.0.0-SNAPSHOT.jar
```

causes an error: *No suitable driver found for jdbc:mysql://localhost/FREERIDER_DB*

```
Hello FREERIDER_DB!
java.sql.SQLException: No suitable driver found for jdbc:mysql://localhost/FREER
IDER_DB
        at java.sql/java.sql.DriverManager.getConnection(DriverManager.java:708)
        at java.sql/java.sql.DriverManager.getConnection(DriverManager.java:230)
        at de.freerider.App.main(App.java:26)
        at org.codehaus.mojo.exec.ExecJavaMojo.doMain(ExecJavaMojo.java:385)
        at org.codehaus.mojo.exec.ExecJavaMojo.doExec(ExecJavaMojo.java:374)
        at org.codehaus.mojo.exec.ExecJavaMojo.lambda$execute$0(ExecJavaMojo.java:296)
        at java.base/java.lang.Thread.run(Thread.java:1583)
```

The Java JRE includes SQL-libraries (package: `java.sql`), but it does not include
drivers to connect to specific databases.

The driver-package for the *mysql* database must be added from the
[*Maven Central*](https://mvnrepository.com)
repository. Search for *"MySQL Connector Java"*, which will find the
[mysql-connector-java](https://mvnrepository.com/artifact/mysql/mysql-connector-java)
package.

Select version  `8.0.33` and copy the *Maven* depdendency:

```xml
<!-- https://mvnrepository.com/artifact/mysql/mysql-connector-java -->
<dependency>
    <groupId>mysql</groupId>
    <artifactId>mysql-connector-java</artifactId>
    <version>8.0.33</version>
</dependency>
```

into `pom.xml` under `<dependencies>`. This will add the driver package to *maven*
and to the classpath.

Re-packaging will add the new dependency to the `.jar`-file:

```sh
# must include dependencies into packaged .jar file
mvn package assembly:assembly -DdescriptorId=jar-with-dependencies
ls -la target
```

The *target* directory now shows two `.jar`-files: one (smaller, 3KB) with no
packaged dependencies and one with (1.4MB):

```
-rw-r--r-- 1    3310 Jun  6 23:19 jdbc-client-1.0.0-SNAPSHOT.jar
-rw-r--r-- 1 4141755 Jun  6 23:25 jdbc-client-1.0.0-SNAPSHOT-jar-with-dependencies.jar
```

Running the application (with included dependencies) will produce the expected output
assuming the database container is also running:

```sh
# run application by the executable jar
java -cp target/jdbc-client-1.0.0-SNAPSHOT-jar-with-dependencies.jar de.freerider.App
```

Output shows **records obtained from the database:**

```
Hello FREERIDER_DB!
id: 1, name: Meyer, Eric, contact: eme22@gmail.com, status: Active
id: 2, name: Sommer, Tina, contact: 030 22458 29425, status: Active
id: 3, name: Schulze, Tim, contact: +49 171 2358124, status: Active
```

The `.jar`-file without packaged dependencies includes:

```sh
# show content of jar-file:
jar tfv target/jdbc-client-1.0.0-SNAPSHOT.jar
```

Content of `.jar`-file without packaged dependencies:

```
     0 Thu Jun 06 23:19:56 CEST 2024 META-INF/
   154 Thu Jun 06 23:19:54 CEST 2024 META-INF/MANIFEST.MF
     0 Thu Jun 06 23:18:18 CEST 2024 de/
     0 Thu Jun 06 23:18:18 CEST 2024 de/freerider/
  2241 Thu Jun 06 23:18:18 CEST 2024 de/freerider/App.class
     0 Thu Jun 06 23:19:56 CEST 2024 META-INF/maven/
     0 Thu Jun 06 23:19:56 CEST 2024 META-INF/maven/de.freerider/
     0 Thu Jun 06 23:19:56 CEST 2024 META-INF/maven/de.freerider/jdbc-client/
  1428 Thu Jun 06 23:18:14 CEST 2024 META-INF/maven/de.freerider/jdbc-client/pom.xml
   123 Thu Jun 06 23:09:52 CEST 2024 META-INF/maven/de.freerider/jdbc-client/pom.properties
```

The `.jar`-file with packaged dependencies is much larger and contains many more
files since it not only includes the dependency for the *mysql* driver, but also
its transitively used dependencies:

```sh
# show content of jar-file that includes dependencies:
jar tfv target/jdbc-client-1.0.0-SNAPSHOT-jar-with-dependencies.jar
```

Content of `.jar`-file with packaged dependencies:

```
     0 Thu Jun 06 23:25:52 CEST 2024 META-INF/
   109 Thu Jun 06 23:25:50 CEST 2024 META-INF/MANIFEST.MF
     0 Thu Jun 06 23:18:18 CEST 2024 de/
     0 Thu Jun 06 23:18:18 CEST 2024 de/freerider/
...
  6459 Wed Oct 26 17:25:38 CEST 2022 google/protobuf/timestamp.proto
  6126 Wed Oct 26 17:25:38 CEST 2022 google/protobuf/type.proto
  4042 Wed Oct 26 17:25:38 CEST 2022 google/protobuf/wrappers.proto
```

In total: 1823 files.


Push branch `maven-jdbc` with all changes to your remote repository.


<!-- 
# scaffolding: generate maven quickstart project layout
mvn archetype:generate \
    -DarchetypeGroupId=org.apache.maven.archetypes \
    -DarchetypeArtifactId=maven-archetype-quickstart \
    -DarchetypeVersion=1.0 \
    -DinteractiveMode=false \
    \
    -DgroupId=${GAV["groupId"]} \
    -DartifactId=${GAV["artifactId"]} \
    -Dversion=${GAV["version"]}
 -->
>>>>>>> maven-jdbc
