
## What is dependency injection and what are the advantages?
> DI는 무엇이고 이점이 무엇일까?

### Dependency Injection
> 위키피디아에서는 이렇게 설명한다
```
In software engineering, dependency injection is a technique in which an object receives other objects that it depends on. These other objects are called dependencies. In the typical "using" relationship[1] the receiving object is called a client and the passed (that is, "injected") object is called a service. The code that passes the service to the client can be many kinds of things and is called the injector. Instead of the client specifying which service it will use, the injector tells the client what service to use. The "injection" refers to the passing of a dependency (a service) into the object (a client) that would use it.
```
```
SW 엔지니어링에서 DI는 객체가 의존하고 있는 다른 객체의 종속성을 받는 하나의 기술입니다. 이러한 다른 객체들은 의존성 호출입니다. 전형적인 사용 관계에서 수신 객체를 [클라이언트]라고 부르고, 전달된 객체를 injected(주입된) 객체를 [서비스]라고 합니다. 서비스를 클라이언트에 전달하는 코드는 많은 종류가 될 수 있으며 인젝터라고 부릅니다. 클라이언트는 사용할 서비스를 지정하는 대신, 인젝터에게 사용할 서비스를 알려줍니다. injection은 의존성(서비스)을 그것을 사용하는 객체(클라이언트)에게 전달하는 것을 말합니다.
```

```
```

```
```



```
The service is made part of the client's state. Passing the service to the client, rather than allowing a client to build or find the service, is the fundamental requirement of the pattern.

The intent behind dependency injection is to achieve Separation of Concerns of construction and use of objects. This can increase readability and code reuse.

Dependency injection is one form of the broader technique of inversion of control. A client who wants to call some services should not have to know how to construct those services. Instead, the client delegates the responsibility of providing its services to external code (the injector). The client is not allowed to call the injector code; it is the injector that constructs the services. The injector then injects (passes) the services into the client which might already exist or may also be constructed by the injector. The client then uses the services. This means the client does not need to know about the injector, how to construct the services, or even which actual services it is using. The client only needs to know about the intrinsic interfaces of the services because these define how the client may use the services. This separates the responsibility of "use" from the responsibility of "construction".
```

