# sns-services
Services for sound level

Api's Documentation
The api is secured by a token. It is created when the user logs in and is used to identify him in other requests. The token is deleted when the user logs out.

Slim Framework*

The api uses the slim framework.
Link: https://www.slimframework.com/

Success* / Error* 

>data = {
>“method” : “ ”,
>“status” : “ ”,
>“code” : “ ”
>}

Http*

The HTTP response code helps the developer and/or customer understand the status of the response. The various answers are specified via the Mozilla documentation.
Link: https://developer.mozilla.org/fr/docs/Web/HTTP/Status

-------------------------------------------------------------

All*

/version GET

Data received:

>data = {
>“version” : “ ”,
>“php” : “ “
>}

Api and php version.

/connect POST

Data to send:

>data = {
>“identifiant” : “ ”,
>“password” : “ ”
>}

Data received:

>data = {
>“nom” : “ ”,
>“prenom” : “ ”,
>“image” : “ ”,
>“auth” : “ ”,
>“token” : “ ”
}

Login page on application.

/verification GET

Data received:

>data = {
>“request” : “ ”,
>“status” : “ ”,
>“code” : “ ”
>} Success* / Error*

Checking the database’s connection.

-------------------------------------------------------------

User*

/son POST

Data to send:

>data = {
>“token” : “ ”
>}

Data received:

>data = {
>“alerte” : “ ”,
>“couleur” : “ ”,
>“valeur” : “ ”
>}

Sound recovered with socket.

/password PUT

Data to send:

>data = {
>“token” : “ ”,
>“password” : “ “
>}

Data received:

>data = {
>“request” : “ ”,
>“status” : “ ”,
>“code” : “ ”
>} Success*

User password update.

-------------------------------------------------------------

Admin*

/palier POST 

Data to send:

>data = {
>“token” : “ ”
>}

Data received

>data = {
>“minimum: “ “,
>“maximum” : “ ”
>}

Receive both levels of sound.

/palier PUT

Data to send:

>data = {
>“token” : “ “,
>“minimum” : “ ”,
>“maximum” : “ ”
>}

Data received:

>data = {
>“request” : “ ”,
>“status” : “ ”,
>“code” : “ ”
>} Success*

Updated both sound levels.
