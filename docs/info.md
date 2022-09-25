### Patterns
In software development, a pattern describes a general solution to a design problem that recurs repeatedly in many projects. We used some of them to build the modern solution with clean architecture.

* [3-tier architecture](./docs/3-tier-architecture.md) - Carousel module uses 3-tier architecture. API/Presentation Layer, Domani/Business Logic Layer, and Persistent Layer.
* [Modularity](./docs/essential-modularity/) - Core of Carousel. The set of the services which are responsible for modularity, module information and dependency resolving between modules.
* [Dependency Injection](https://docs.microsoft.com/en-us/dotnet/core/extensions/dependency-injection) - the dependency injection (DI) software design pattern, which is a technique for achieving [Inversion of Control (IoC)](https://docs.microsoft.com/en-us/dotnet/architecture/modern-web-apps-azure/architectural-principles#dependency-inversion) between classes and their dependencies.
* [Factory](https://github.com/shipcarousle/carousel-core-services/blob/main/src/server/platform/Carousel.Platform.Core/Domain/AbstractTypeFactory.cs) -  follow the [Factory method pattern](https://en.wikipedia.org/wiki/Factory_method_pattern). They are simply the place where you instantiate and override objects. This means that in Carousel there are no “new” statements in the codebase.
* [Native Extensibility](./docs/extensibility.md) - unique extension framework based on reflection, abstract-factory and dependency injection. Allows extending business logic, API contracts, Data Model and Admin UI without touching the source code.
* [Backend for Frontend / Exprience API](./docs/experience-api.md) - Hide all the frontend business logic of a module behind them and give a very simple and straightforward GraphQL business interface.

### 3rd-Party Frameworks and Components

We tested and choose the best in breed 3rd-Party Frameworks and Components which make Enterprise requirements.

* [.NET 6](https://dotnet.microsoft.com/en-us/) - Cross-platform. Open Source. A developer platform.
* [ASP.NET Core](https://dotnet.microsoft.com/en-us/apps/aspnet) - Extends the .NET developer platform with tools and libraries specifically for building web apps and Web API.
* [GraphQL](https://github.com/graphql-dotnet/graphql-dotnet) - Implementation of GraphQL in .NET.
* [Entity Framework](https://docs.microsoft.com/en-us/ef/) - Modern object-database mapper for .NET. By default use MS SQL provider.
* [MS SQL](https://azure.microsoft.com/en-us/products/azure-sql/database/) - Primary data-storage.
* [Hangfire](hangfire.io) - Platform for background processing and recurring jobs.
* [Redis](https://redis.io/) - Distributed cache storage.
* [Azure Application Insight](https://docs.microsoft.com/en-us/azure/azure-monitor/app/app-insights-overview) - Monitoring tools
* [SignalR](https://dotnet.microsoft.com/en-us/apps/aspnet/signalr) - Incredibly simple real-time web.
* [CSV Helper](https://github.com/JoshClose/CsvHelper) - Library for reading and writing CSV files. Extremely fast, flexible, and easy to use
* [FluentValidation](https://github.com/FluentValidation/FluentValidation) - Validation library that uses a fluent interface and lambda expressions for building strongly-typed validation rules.
* [Swagger UI](https://github.com/swagger-api/) - dynamically generate documentation from a Swagger-compliant API.
* [Nuke.build](https://nuke.build/) - The cross-platform build automation solution for .NET with C# DSL.

### Carousel Components
We created our own interfaces, abstractions, utilities to simplify the development routine and don't worry about implementation. Carousel Team will care about implementation without Breaking Changes.

* [Cache](./docs/essential-caching.md) - Default ASP.NET Core in-memory cache with cache invalidation via Redis.
* [Settings](https://github.com/shipcarousel/carousel-core-services/blob/main/src/server/platform/Carousel.Platform.Core/Settings/SettingDescriptor.cs) - Design-Time Module Settings with special fluent syntax and localization.
* [Security](./docs/role-based-securitymd) - Role-based security with permissions to have secured access to any API.
* [Events](./docs/extending-using-events.md) - Internal event bus for fast communication between modules.
* [Generic Import/Export](https://github.com/shipcarousel/carousel-core-services/blob/main/src/server/platform/Carousel.Platform.Core/ExportImport/IPlatformExportImportManager.cs) - Native export/import functionality for either backup or migration processes.
* DistributedLock - Startup synchronization for singleton operations in multi-instance configurations.
* [GenericCrud](https://github.com/shipcarousel/carousel-core-services/blob/main/src/server/platform/Carousel.Platform.Core/GenericCrud/ICrudService.cs) - Utility interfaces and class to improve developer productivity for implementation of CRUD operations for new entities.
* [ChangeLog](https://github.com/shipcarousel/carousel-core-services/blob/main/src/server/platform/Carousel.Platform.Core/ChangeLog/IChangeLogService.cs) - implementation of Change Log.
* [DynamicProperties](./docs/using-dynamic-properties.md) - Set of the interfaces, services, UI elements to implement the ability to extend an entity with new properties run-time and using the admin interface.
* [Localization](https://github.com/shipcarousel/carousel-core-services/blob/main/src/server/platform/Carousel.Platform.Core/Localizations/ITranslationService.cs) - Abstraction above localization files.
* [Carousel CLI](./docs/CLI-tools.md) -  is the official CLI .NET Core GlobalTool that helps you build, test and deploy releases, create and push NuGet packages, provide package management for projects based on VirtoCommerce, and automate common DevOps tasks.

### Carousel Modules
Carousel has developed these modules which can be helpful in analytics solution.