- @Controller ( To declare a bean )
- @Service ( To declare a bean )
- @Autowired (To Autowire  a bean)
- @Qualifier (used with Autowired in case of more than one instance of a service)
- @Primary (To set a primary bean in case of more than one bean of same type present, would be used if qualifier is absent )
- @Profile (To define which service you want to use when a profile is set as active, So you can define multiple services with same name and based on the profile pick one of them)
- @Profile({"dev","default"}) -> The default designated beans would be used if no active profile is given
- @Configuration -> Used to tell that class contains the java configuration.
- @Bean -> Used to annotate a function returning Bean.
- @PropertySource -> Used to fetch properties from property files.
- @Value -> Used to fetch a particular value from your properties.

#annotations 