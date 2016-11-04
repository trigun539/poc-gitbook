# Enterprise Metadata Repository

The EMR is a web application that contains all of the application, and database information in an easily digestable form.

## Software

- IBM JDK 1.7
- Websphere 8.5.5.8
- Editor of your Choice (eclipse, RAD, etc.)
- Maven 3.3 or higher
- NodeJS v6

## Setup

```bash
# Nexus Repo to use with Maven setup
http://nexus.ba.ssa.gov:8082/nexus/content/groups/EVAL_SSA_GROUP/

# Point npm to internal registry
http://nexus.ba.ssa.gov:8082/nexus/content/repositories/npm-all/
```

## Running

```bash
mvn jetty:run -pl emrService
```

## Project Structure

```bash
emr
 |--emrService
 |   |--src/main/webapp
 |       |index.html
 |       |--reactJS   
 |       |--css
 |--emrDao
 |--emrModel
```

emr is Parent Maven project it has parent pom.xml with packaing type "pom"
where we  define all the common maven properties used by child maven projects (emrService, emrDao, emrModel etc.)

emrService is the web project where all the webServices/react/css/frontend code will reside.

Application will be deployed to websphere 8.5.58 in production but if you want to use jetty to test/run application, we 
provide embedded jetty with application to test quickly your changes in development environment.

Use mvn jetty:run -pl emrService to deploy emrService code from command prompt.Jetty will start and wait at command
prompt. In order to stop jetty use ctrl+C at command prompt.
Application will run on http://localhost:9091/ and listen to emrService at this address.

it supports dynamic loading of static content(html, css) and java content. Static content changes reflects
automatically though but for java changes to reflect you need to direct jetty to load by hitting enter at
command prompt.
