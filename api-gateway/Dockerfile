FROM mcr.microsoft.com/dotnet/core/sdk:3.0

LABEL "maintainer"="gautur16@ru.is, benediktt16@ru.is"

ENV ASPNETCORE_URLS=http://+:7000

COPY . /app
WORKDIR /app

RUN dotnet restore
RUN dotnet build

ENTRYPOINT [ "dotnet", "run" ]

# RUN notað til að setja upp command skipanir sem á að runna þegar forritið startast

# ADD folder/folder/folder * folder - Tekur allar skrár í fyrra inputinu og copy'ar yfir í seinna inputið
# ADD *.js* filepath - tekur allar javascript skrár og copy'ar þær yfir í filepath

# WORKDIR $DB - er það sam og að gera cd order-service/data/db

# RUN npm install - myndir setja allt sem er að installast úr npm install í $DB (sjá fyrir ofan)

# CMD segir okkur hvernig containerinn á að keyra upp

# Búa til container er docker create --name nafn-á-container
# Til að starta honum þá er docker start nafn-á-container