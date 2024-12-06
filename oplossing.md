Vul onderstaande aan met de antwoorden op de vragen uit de readme.md file. Wil je de oplossingen file van opmaak voorzien? Gebruik dan [deze link](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) om informatie te krijgen over
opmaak met Markdown.

# a)
## Gebruik docker
We installeren docker en voegen we zowel de jenkins user als de locale user toe aan de docker group zodat ze docker commands kunnen uitvoeren zonder sudo te gebruiken. We loggen in docker met onze jenkins user om ervoor te zorgen dat we images kunnen pushen naar de public repository thabondi/dtap-pe.

## Credentials prodserver
Na het aanmaken van een de aws ec2 instance kunnen we de private key gebruiken om nieuwe credentials aan te maken in jenkins. De credentials hebben we nodig om een ssh connectie te leggen met de production server.

## sshagent plugin
Om de credentails te kunnen gebruiken zonder een key file te gebruiken maken we gebruik van de sshagent plugin in jenkins.

## Production server port
Nodejs maakt gebruik van de poort 3000 dus zorgen we ervoor dat we via de command "docker run -d --rm -p 80:3000 --name production thabondi/dtap-pe:latest" hiermee kunnen we verbinding leggen met die production server via poort 80