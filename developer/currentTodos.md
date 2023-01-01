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
- [] create abstract class "MenuRouteFactory"
- [] create abstract function `getNamedIcon(): NamedIcon`
- [] create abstract function `getRouteBehavior(): MenuRouteBehavior`
- [] implement function `getMenuRoute(): MenuRoute`, which uses the abstract functions
- [] implement single routeFactories
    - [] shoppingList
    - [] items
    - [] categories
    - [] shops
    - [] meals

--- MenuRoutesFactory class
- [] create class MenuRoutesFactory in ApplicationMenuRoutes.ts
- [] rename ApplicationMenuRoutes.ts to MenuRoutesFactory.ts
- [] move MenuRoutesFactory to factories - folder
- [] create function "getRoutes" in MenuRoutesFactory. Use the MenuRouteFactories to return the MenuRoutes
- [] use MenuRoutesFactory in MenuFactory

--- post processing
- [] merge branch to master