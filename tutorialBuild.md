# Build DSpace for Docker
_It is not necessary to run this step using Docker. The following instructions illustrate how Docker can be used to run Docker._

_If you have maven installed locally, it is probably preferable to run the maven build using your local mave installation._

## Building DSpace Using Docker

Set the environment variable **DSPACE_SRC** to the root directory of your cloned DSpace repository.

- MacOS or bash: `export DSPACE_SRC=$(pwd)`
- Windows CMD: `set DSPACE_SRC=%cd%`
- Windows Powershell: ???

### Run Maven in Docker

    docker run -it --rm -v ${HOME}/.m2:/root/.m2 -v ${DSPACE_SRC}:/opt/maven -w /opt/maven maven mvn clean install
