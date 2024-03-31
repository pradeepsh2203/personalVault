## Property Source
You can use your properties file and import the properties you want in your application. Ussing annotation @PropertySource('classpath:your file path') #annotations . Then use @Value(${'your_property_key'}) annotation.

## Environment variables and program args
Environment variable in Snake caps can be used to override your properties.
Program Arguments in same case type can be used to override the Environment Variable.

Note:- In context of **Spring Boot** it auto imports the properties from application.properties so we are not required to use the property source annotation.

## Profile
In spring boot we can create profile based properties file. by adding -{profile} in our application properties file and we can activate our profile from our base file as well.

Spring Has properties binding  If you wanna use it search about it.
