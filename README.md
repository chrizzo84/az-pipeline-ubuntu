# Ubuntu 24.04 Azure Pipelines Agent in Docker
This is a Dockerfile + start.sh for Azure Piplines Agent with some preinstalled stuff.

## Preinstalled Software:
- OpenJDK 17
- OpenJDK 11
- OpenJDK 8
- Dotnet 8
- Python 3
- npm
- Azure CLI

## Capabilities:
| Env              | Path                                |
|------------------|-------------------------------------|
| az               | /usr/bin/az                         |
| curl             | /usr/bin/curl                       |
| dotnet           | /usr/bin/dotnet                     |
| git              | /usr/bin/git                        |
| java             | /usr/bin/java                       |
| JAVA_HOME_8_X64  | /usr/lib/jvm/java-8-openjdk-amd64   |
| JAVA_HOME_11_X64 | /usr/lib/jvm/java-11-openjdk-amd64  |
| JAVA_HOME_17_X64 | /usr/lib/jvm/java-17-openjdk-amd64  |
| python3          | /usr/bin/python3                    |
| nodejs           | /usr/bin/nodejs                     |
| npm              | /usr/bin/npm                        |

## License:
[GNU General Public License v3.0](LICENSE)

## HowTo:
This image is automatically built and pushed to the GitHub Container Registry (ghcr.io) using GitHub Actions.

Run it with:
```
docker run -e AZP_URL=https://dev.azure.com/<OranizationName> -e AZP_TOKEN=<YourPersonalAccessToken> -e AZP_AGENT_NAME=<AgentName> -e AZP_POOL=<PoolName> ghcr.io/chrizzo84/azpipeline:latest
```
