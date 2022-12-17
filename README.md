# .NET-Core-Linux-Daemon
Sample Linux Daemon written in .NET Core with systemd config and Docker deployment

cd Service.Sample
mkdir publish

docker build -f Dockerfile -t sample/service .
docker-compose up 