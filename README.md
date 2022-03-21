Note: this code sample and blog article was contributed by [Reshma Sathe](https://www.linkedin.com/in/reshma-sathe/) in March, 2022. 

## Read the Blog: Getting Started with HelloSign Embedded Signing using Java Spring Boot

Embedded signing, part of the HelloSign API, allows customers to sign documents directly on your website by using a secure iFrame. This code shows how to use the HelloSign API to add embedded signing to a Java Spring Boot app.

This code sample was created for an article on the HelloSign blog. Please refer to [Getting Started with HelloSign Embedded Signing using Java Spring Boot](https://www.hellosign.com/blog/embedded-signing-using-java-spring-boot) to learn how to build this sample from the beginning.

---

## Just the Sample Code

Want to run the code without reading the blog? Use the instructions below. Refer to the blog post if you get stuck. 

1. Clone this repo.
2. Fill out the _example-application.properties_ file and rename to _application.properties_.
3. Run your Spring Boot app: `mvn spring-boot:run`.
4. Start ngrok `ngrok http 8080`. 
5. Add an event callback url to your HelloSign app using the ngrok url and webhook handling endpoint. (i.e. `https://8b8e-50-47-128-110.ngrok.io/api/hellosign/webhook`).
6. Send a POST request to create an embedded signature request and generate a sign url: `curl -X POST https://322b-50-47-128-110.ngrok.io/api/hellosign/embeddedsign`.
7. Copy the sign url into HelloSign's [Embedded Testing Tool](https://app.hellosign.com/api/embeddedTest). 
8. Complete the signature flow. This is the signing experience your end user would have when using embedded signing in your app.

Great job! After you've finished signing, take a look through the webhook logs and inspect the signed document on HelloSign.