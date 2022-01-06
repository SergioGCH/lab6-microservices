First of all, we have to run this command:

```
./gradlew :registration:bootRun
```

The registration server is now exposed in http://localhost:1111. Then, we can run the two services with these commands:

```
./gradlew :accounts:bootRun
./gradlew :web:bootRun
```
Accounts log:
![accounts](https://user-images.githubusercontent.com/61270404/148394238-aa9ac38e-49c7-4685-bc61-12500c6bc95b.PNG)

Web log:
![web](https://user-images.githubusercontent.com/61270404/148394492-cca75286-8646-49cd-b9de-73a0dc063522.PNG)

Now we are able to see the two instances registered in localhost:1111

![eureka](https://user-images.githubusercontent.com/61270404/148395115-f9bfb4f1-e9d9-40b0-9f8c-33eb02c86595.PNG)

Service registration log after register:

![serviceRegistration](https://user-images.githubusercontent.com/61270404/148395601-bb2225dd-5323-4fc3-8395-600c8275c92b.PNG)

Now we want a second account service to be running in the port 4444 and have it registered. In order to do that, we must modify application.yml file from the accounts folder.
We change the port 2222 to 4444 and launch the same command in another terminal. 

![4444](https://user-images.githubusercontent.com/61270404/148396886-9653d260-be33-4516-9d4a-3b15bae36045.PNG)
![eureka4444](https://user-images.githubusercontent.com/61270404/148397050-06bc0046-5bd5-4dcf-823e-adc9e595ce78.PNG)

If we kill process 2222 it is no longer registered in Eureka:

