## Types of Spring Configuration
You can provide spring configuration in any one of these ways:-
- XML Based Configuration (Used in legacy system)
- Annotation Based Configuration
- Java Based Configuration (Most Preferred method)
- Groovy Based DSL.

## Spring Stereotype
Using annotation based classes to create beans in spring is termed as spring stereotyping #confirm. Spring uses component scan to find all these classes and the default base package is where our startup file exist.

## Java Configuration
*Generally used while using third party packages to include them in the spring context.*
You can use the java configuration to remove the annotations from the class and making function in the java configuration class and annotating them with the Bean( By default the bean name is the method name in camelCase).

## Factory Beans
It's a pattern *Not perfectly clear* but we use a method in factory class and return corresponding class based on some conditions.

**Note:**- You can use Profile and Primary annotations in java configurations too
Note:- Anything that exists inside your resource folder can be imported using classpath.