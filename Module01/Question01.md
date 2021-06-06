
## What is dependency injection and what are the advantages?
> DI는 무엇이고 이점이 무엇일까?

### Dependency Injection
> 위키피디아에서는 이렇게 설명한다
  * In software engineering, dependency injection is a technique in which an object receives other objects that it depends on.
    * SW 엔지니어링에서 DI는 객체가 의존하고 있는 다른 객체의 종속성을 받는 하나의 기술입니다.
  * These other objects are called dependencies.
    * 이러한 다른 객체들은 의존성 호출입니다.
  * In the typical "using" relationship[1] the receiving object is called a client and the passed (that is, "injected") object is called a service.
    * 전형적인 사용 관계에서 수신 객체를 [`클라이언트`]라고 부르고, 전달된 객체를 injected(주입된) 객체를 [`서비스`]라고 합니다.
  * The code that passes the service to the client can be many kinds of things and is called the injector.
    * 서비스를 클라이언트에 전달하는 코드는 많은 종류가 될 수 있으며 인젝터라고 부릅니다.
  * Instead of the client specifying which service it will use, the injector tells the client what service to use.
    * 클라이언트는 사용할 서비스를 지정하는 대신, 인젝터에게 사용할 서비스를 알려줍니다.
  * The "injection" refers to the passing of a dependency (a service) into the object (a client) that would use it.
    * `injection`은 의존성(서비스)을 그것을 사용하는 객체(클라이언트)에게 전달하는 것을 말합니다.
  * The service is made part of the client's state.
    * 서비스는 클라이언트의 상태의 일부입니다.
  * Passing the service to the client, rather than allowing a client to build or find the service, is the fundamental requirement of the pattern.
    * 클라이언트가 서비스를 구축하거나 찾도록 허용하지 않고 서비스를 클라이언트에 전달하는 것이 패턴의 기본 요구 사항입니다.
  * The intent behind dependency injection is to achieve Separation of Concerns of construction and use of objects.
    * 의존성 주입의 의도는 객체의 구성 및 사용에 대한 우려의 분리를 달성하는 것입니다.
  * This can increase readability and code reuse.
    * 이것은 가독성과 코드 재사용성이 증가할 수 있습니다.
  * Dependency injection is one form of the broader technique of inversion of control.
    * 의존성 주입은 광범위한 제어 역전 기술의 한 형태이다.
  * A client who wants to call some services should not have to know how to construct those services.
    * 서비스를 호출하려는 클라이언트는 해당 서비스를 구성하는 방법을 몰라도 됩니다.
  * Instead, the client delegates the responsibility of providing its services to external code (the injector).
    * 대신 클라이언트는 서비스를 제공하는 책임을 외부 코드 (인젝터)에게 위임합니다.
  * The client is not allowed to call the injector code; it is the injector that constructs the services.
    * 클라이언트는 인젝터 코드를 호출 할 수 없습니다. 서비스를 구성하는 것은 인젝터입니다.
  * The injector then injects (passes) the services into the client which might already exist or may also be constructed by the injector.
    * 그런 다음 인젝터는 이미 존재하거나 인젝터에 의해 구성 될 수있는 서비스를 클라이언트에 인젝션 (통과)합니다.
  * The client then uses the services.
    * 그런 다음 클라이언트는 서비스를 사용합니다.
  * This means the client does not need to know about the injector, how to construct the services, or even which actual services it is using.
    * 즉, 클라이언트는 인젝터, 서비스 구성 방법 또는 실제 사용중인 서비스에 대해 알 필요가 없습니다.
  * The client only needs to know about the intrinsic interfaces of the services because these define how the client may use the services.
    * 클라이언트는 서비스의 고유 한 인터페이스에 대해서만 알면됩니다. 인터페이스는 클라이언트가 서비스를 사용하는 방법을 정의하기 때문입니다.
  * This separates the responsibility of "use" from the responsibility of "construction".
    * 이것은 "사용"의 책임과 "생성"의 책임을 분리합니다.
