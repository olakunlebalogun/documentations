# Spring boot Unit Test  

## Testing Service Implementation  

``` 
public class ProductServiceImplTest {
    private ProductServiceImpl productServiceImpl;
    private ProductRepository productRepository;

    @BeforeEach
    void setUp() {
        productRepository = Mockito.mock(ProductRepository.class);
        productServiceImpl = new ProductServiceImpl(productRepository);
    }

}
```java

OR

``` 
@ExtendWith(MockitoExtension.class)
public class ProductServiceImplTest {

    @Mock
    private ProductRepository productRepository;
    
    @InjectMocks
    private ProductServiceImpl productServiceImpl;



}

```java


## Resources 
https://www.baeldung.com/integration-testing-in-spring
https://t.co/Lyzh5k6noq
https://reflectoring.io/spring-boot-web-controller-test/
https://reflectoring.io/unit-testing-spring-boot/#creating-readable-assertions-with-assertj
https://reflectoring.io/spring-boot-data-jpa-test/
https://reflectoring.io/spring-boot-test/
https://reflectoring.io/spring-boot-web-controller-test/#matching-json-output

https://www.baeldung.com/guide-to-jayway-jsonpath
https://jsonpath.com/
https://github.com/json-path/JsonPath/blob/master/README.md


https://www.baeldung.com/spring-boot-testing
https://www.baeldung.com/mockito-series
https://www.baeldung.com/mockito-annotations
https://www.baeldung.com/bdd-mockito
https://www.baeldung.com/mockito-mock-methods
https://www.baeldung.com/mockito-argument-matchers
https://www.baeldung.com/mockito-exceptions
https://www.baeldung.com/mockito-java-8
https://www.baeldung.com/mockito-behavior
https://www.baeldung.com/mockito-verify
Baeldung Mockito Advanced Series
https://www.baeldung.com/mockito-void-methods
https://www.baeldung.com/mockito-final
https://www.baeldung.com/mockito-2-lazy-verification
https://www.baeldung.com/mockito-callbacks
https://www.baeldung.com/mockito-deprecated-mockitojunitrunner
https://www.baeldung.com/kotlin-mockito
https://www.baeldung.com/mockito-mock-static-methods
https://www.baeldung.com/mockito-spy
https://www.baeldung.com/mockito-argumentcaptor
Mockito Integration with Other Libraries
https://www.baeldung.com/injecting-mocks-in-spring
https://www.baeldung.com/java-spring-mockito-mock-mockbean
https://www.baeldung.com/spring-mock-rest-template
https://www.baeldung.com/mockito-junit-5-extension
https://www.baeldung.com/junit-test-abstract-class
https://www.baeldung.com/mockito-vs-easymock-vs-jmockit
https://www.baeldung.com/powermock-private-method
https://www.baeldung.com/intro-to-powermock


Toptal documentation on JUnit testing and Mockito
https://www.toptal.com/java/a-guide-to-everyday-mockito
https://www.toptal.com/java/getting-started-with-junit

Digital Ocean Documentation
https://www.digitalocean.com/community/tutorials/mockito-tutorial#mockito-maven-dependencies

Articles Recommended by Mr. Jide
https://1kevinson.com/how-to-write-integration-tests-with-h2-in-memory-database-and-springboot/
https://medium.com/@wahyudi.hh/h2-database-as-embedded-postgres-for-spring-boot-integration-test-295683c7b974
https://www.vincenzoracca.com/en/blog/framework/spring/integration-test/
https://www.concretepage.com/spring-5/activeprofiles-example-spring-test
https://www.youtube.com/watch?v=q2L9nuiJU70

Unit Testing
https://www.vincenzoracca.com/en/blog/framework/spring/unit-test/


https://www.vincenzoracca.com/en/blog/framework/spring/
https://martinfowler.com/articles/practical-test-pyramid.html


TestContainers
https://1kevinson.com/integration-testing-with-springboot-docker-and-tests-containers/
https://www.freecodecamp.org/news/integration-testing-using-junit-5-testcontainers-with-springboot-example/
https://www.baeldung.com/docker-test-containers