FROM mcr.microsoft.com/dotnet/aspnet:6.0 AS base
WORKDIR /app
COPY ./publish/ ./
COPY ./sample.service /lib/systemd/system/

RUN apt-get update
RUN apt-get install systemd -y

CMD ["systemctl", "enable", "sample"]
CMD ["systemctl", "start", "sample"]

ENTRYPOINT ["dotnet", "Service.Sample.dll"]


#ENTRYPOINT ["systemctl", "start", "sample"]


#RUN systemctl daemon-reload
#RUN systemctl enable sample
#RUN systemctl start sample
#EXPOSE 80