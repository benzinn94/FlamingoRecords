FROM mcr.microsoft.com/dotnet/core/sdk:3.0

LABEL "maintainer"="gautur16@ru.is, benediktt16@ru.is"

ENV ASPNETCORE_URLS=http://+:80

COPY . /app
WORKDIR /app/customer-service

RUN dotnet restore
RUN dotnet build

ARG POSTGRES_PASSWORD
ARG POSTGRES_DB

VOLUME [ "/${PWD}/customer-db/db-scripts:/docker-entrypoint-initdb.d postgres" ]

ENTRYPOINT [ "dotnet", "run" ]