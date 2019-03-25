# JPro from Jars

This project helps you to use [JPro](https://jpro.one/), when you have the Jars of your application.

This can be useful, when you are using neither Maven nor Gradle.

## How to use:

### Step1
Put your Jars into the folder "libs".

It can be either a single fat-jar, or your application and it's libraries.

### Step2
Change the mainclass in the file `gradle.properties``

### Step3
On Mac/Linux, run the following command: `./gradlew jproRun`.

On Windows, run the following command: `gradlew.bat jproRun`.

After some time, the browser should open automatically.


# Additional Notes
* Take a look at our [documentation](https://www.jpro.one/?page=docs/current/1.1/), for further information. 
* This project is based on [HelloJPro](https://github.com/jpro-one/HelloJPro)
* Technically, this is a simple gradle-project using JPro. You can configure this project, like any other JPro project.
* If you want to use multipl mainclasses, you can add the file `src/main/resources/jpro.conf` and add multiple mainclasses.




## Deployment:

### Step `1`. Prepare your server

To run JPro on linux, the server must be configured correctly.

Checkout the following chapters to configure your server correctly for JPro:

[DEPLOYING JPRO](https://www.jpro.one/?page=docs/current/2.6/DEPLOYING_JPRO)
 
[PREPARING LINUX FOR JPRO](https://www.jpro.one/?page=docs/current/2.7/PREPARING_LINUX_FOR_JPRO)

### Step `2`. Create the binary

Create a zip which contains the application with the following command:

```groovy
./gradlew jproRelease
```
The path of the zip-file is the following: `build/distributions/HelloJPro-jpro.zip`

Now copy this file to your Server and unzip it.

### Step `3`. Run JPro

In the unzipped folder you can find a start-script: `bin/start.sh`

By running `./bin/start.sh` you start the JPro Server on your server. 

The JPro Server is now ready to server your URLs entered in your browser.

```bash
./bin/start.sh
```


