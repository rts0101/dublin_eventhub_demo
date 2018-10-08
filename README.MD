## Event Hub Tech Demo ##


### What is this? ###

This app I put together to teach myself about event hub. It's a Spring Boot web service that sends a message to event hub, then consumes it and prints it to console.

### How do I run it? ###

There's a Dockerfile in the repo.
Run the following at the project root and you should be good to go.

~~~~
mvn package
docker build -t dublin_eventhub_demo_container .
docker run -p 8080:8080 dublin_eventhub_demo_container
~~~~

### Sample Message Format ###

```json
{
  "firstName": "test",
  "lastName": "testLastName",
  "email": "anotherTestEmail@dogpile.com",
  "eventPayloadDetails":
    {
      "appId":"680360c0-43fe-4209-aeb0-f7",
      "userName":"SadAndroid"
    }
}
```