<h1>Week 1 highlight:</h1>
<h4> POM file </h4>

```java
  <!--添加Spring Boot的父级依赖-->
  <parent>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-parent</artifactId>
    <version>2.0.1.RELEASE</version>
  </parent>
        
```


```java
  <!--添加Web支持的starter pom-->
      <dependency>
          <groupId>org.springframework.boot</groupId>
          <artifactId>spring-boot-starter-web</artifactId>
      </dependency>
      
      
```


<h4> app.java </h4>

```java
package com.boot;

//添加Web支持的starter pom
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class App
{
    public static void main( String[] args )
    {
        SpringApplication.run(App.class, args);
    }
}
```

<h4> HomeController.java </h4>

```java
package com.boot.controller;

import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

//添加测试控制器
@RestController
public class HomeController {

    @RequestMapping("/")
    public String home() {
        return "Das Boot, reporting for duty!";
    }
}

```
#### File structure
![alt text](https://github.com/irispoon1022/springbootw0/blob/master/file_structure.png "Logo Title Text 1")
