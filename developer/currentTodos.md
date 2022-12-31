# Todos
## make a class of ApplicationMenuRoutes - functionality
--- create dataAccessObjects + interfaces + factories
- [] Categories
- [] Shops
- [] Items

--- create class ComponentReadyChecksImpl
- [] make interface out of ComponentReadyChecks
- [] create class "ComponentReadyChecksImpl", which implements ComponentReadyChecks
- [] use daos in constructor to retrieve data
- [] Move readyChecks from ApplicationMenuRoutes to ComponentReadyChecksImpl

--- create NamedIcon class
- [] make NamedIcon - class out of "icon" + "name"
- [] add name + icon constructor parameters to NamedIcon
- [] add namedIcon as property to MenuRoute interface
- [] use NamedIcon instead of old MenuRoute properties in all references
- [] remove name + icon properties from MenuRoute

--- create MenuRouteBehavior class
- [] create class with two properties "componentFactory" + "readyCheck"
- [] add properties to constructor
- [] add bahavior property to MenuRoute interface
- [] use behavior property in all references from MenuRoute
- [] remove componentFactory and readyCheck as direct properties from MenuRoute

--- make class out of MenuRoute
- [] convert MenuRoute from interface to class
- [] create constructor with MenuRouteBehavior + NamedIcon properties
- [] use MenuRoute constructor in ApplicationMenuRoutes

--- MenuRouteFactory class
- [] create class MenuRouteFactory in ApplicationMenuRoutes.ts
- [] rename ApplicationMenuRoutes.ts to MenuRouteFactory.ts
- [] move MenuRouteFactory to factories - folder
- [] create function "getRoutes" in MenuRouteFactory. Return the ApplicationMenuRoutes in the function
- [] use MenuRouteFactory in MenuFactory

--- post processing
- [] merge branch to master