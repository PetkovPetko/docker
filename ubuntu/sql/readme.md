##Image is available on Docker Hub:
```bash
docker pull petkovpetko/lib:sql2022-tmpl
```

## Build docker image with
docker build -t myImage .

## Run docker image
for windows host:
```powershell
docker run -p 1433:1433 -e "MSSQL_SA_PASSWORD=yourStrong(!)Password" -e "SQL_NAME=Win-Host" -e "TEAMS_HOOK=http://teams.channel.web/hook/url" -v c:\sqlData:/var/opt/mssql/data -d myImage
```
for linux host:
```bash
docker run -p 1433:1433 -e "MSSQL_SA_PASSWORD=yourStrong(!)Password" -e "SQL_NAME=Linux-Host" -e "TEAMS_HOOK=http://teams.channel.web/hook/url" -v $(pwd):/var/opt/mssql/data -d myImage
```
