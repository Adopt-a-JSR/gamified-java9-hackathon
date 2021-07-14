# gamified-java9-hackathon

This repo has moved to AdoptOpenJDK as it's more appropriate.
https://github.com/AdoptOpenJDK/gamified-java9-hackathon

This is the source code for the Java 9 Gamified hackathon that was done on the 4'th of June 2016 at the Jozi-JUG.

http://www.meetup.com/Jozi-JUG/events/229688441/

Steps for testing
- mvn clean package.
- using Java 9 to enable http 2 : java -jar target/gamified-java9-hackathon-1.0.0-SNAPSHOT.jar.
- browse to http://localhost:8080/ or http://localhost:8443/
- Presenter launches http://localhost:8080/progress.html on projector.
- Hackaton people login to http://localhost:8080/ and start the challenge.

For proper use
- Issue your domain a certificate from letsencypt.
- Update application.properties.
- Add firewall rules to redirect 8080 -> 80 and 8443 -> 443.
- shell in a box is required for the JEP 286 demo. It's nice to show even if the JEP does not make Java 9.
- createuser.sh can create users on the shell in a box machine.

Notes
- It's 'hard coded' that users use Java 9 build 120-129, but update the unit test io.r3k.hackathon.hvcjava9.controllers.SubmitControllerTest if that is not the case.
