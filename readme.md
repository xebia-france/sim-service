# Requirements

$ brew install gradle (optionnal)  
$ brew install groovy (optionnal)  
$ brew install vert.x  

# Getting started

## Start services
$ ./services.sh

## Start server
$ ./server.sh

# Streams

## Hello

Every service announces itself to /city

```json
{
  "group" : "choose your team name and stick to it",
  "id" : "unique instance id",
  "type" : "service name",
  "version" : "instanceVersion"
}

## PowerPlant
PowerPlant "pp" receives power request from Factory "f"  
service.powerPlant.pp <= [powerRequest:10, factory:"f"]

## Factory
Factory "f" receives power response from PowerPlant "pp"   
service.factory.f <= [powerResponse:5, powerPlant:"pp"]  

## Bank
Bank "b" receives power requests and responses from PowerPlant "pp" and factory "f"
service.powerPlant.pp <= [powerRequest:10, factory:"f"]
service.factory.f <= [powerResponse:5, powerPlant:"pp"]

# Messages
hello
```json
{
  "group" : "chooseYourGroupNameAndStickToIt",
  "id" : "chooseYourGroupNameAndStickToIt-chooseTheInstanceId",
  "version" : "instanceVersion"
}
```


