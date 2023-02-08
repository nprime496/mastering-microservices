

The following packages were installed using the commands specified: Cloc (Count Lines of Code), Yeoman, and JHipster Generator. 


Cloc was installed by running the command npm install -g cloc and Yeoman was installed using npm install -g yo. The version of Yeoman was then confirmed by running yo --version. Finally, the JHipster Generator was installed using the command npm install -g generator-jhipster and its version was confirmed by running jhipster --version. Screenshots were taken to document the installation process.

Screenshots:


![](media/versions.png)

Create gateway and (micro) services following https://github.com/mastering-microservices/tutorial_en/blob/main/microservices/microservices.md

Launch the service registry
``` 
cd ~/github/mastering-microservices/gateway
docker-compose -f src/main/docker/jhipster-registry.yml up
Launch the gateway (dev profile)
cd ~/github/mastering-microservices/gateway
./gradlew
``` 

adminmosig

