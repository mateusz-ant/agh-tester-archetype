Spring MVC & Jetty Maven Archetype
=========================================


Installing archetype within your local repository
---------------------------------------------

* Download zip package and unpack it somewhere.
* Enter unpacked folder and invoke command:

        mvn install archetype:update-local-catalog

* Now you have locally installed archetype. You can delete zip and unpacked folder.

Setting up new project
----------------
* In workspace folder type in following command to create new project:

        mvn archetype:generate
                -DarchetypeCatalog=local
                -DarchetypeGroupId=agh.bit.ideafactory
                -DarchetypeArtifactId=agh-tester-archetype
                -DarchetypeVersion=1.0.0-SNAPSHOT
                -DgroupId=my.groupid
                -DartifactId=my-artifactId
                -Dversion=version

  ...where values of DgroupId, DartifactId, Dversion are chosen by you.

Running the project
----------------

* Go to your project root folder and execute command:

        mvn jetty:run

Now launch your browser and you should see 'hello world' page on localhost:8080
You can also visit localhost:8080/anything