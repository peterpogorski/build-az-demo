---
services: service-fabric
platforms: dotnet
author: pepogors
---

# Service Fabric Visual Objects across Availability Zones
This repository contains a modified version of the [VisualObjects sample](https://github.com/Azure-Samples/service-fabric-dotnet-getting-started/tree/classic/Actors/VisualObjects) and a Service Fabric template for a cluster which spans across availability zones. Each actor in the application will be given a different color based on the node type that it is deployed to. As each of the node types is deployed to a separate availability zone, the color will also correspond to a unique availability zone. This application requires that the node type names are "nt1", "nt11", and "nt12" to work as expected.

## Work still to be done
* Store the node type that each actor is running on in a dictionary. 
* Remove hardcoded color names and node type names. 

## More information
The [Service Fabric cross availability zone documentation](https://docs.microsoft.com/azure/service-fabric/service-fabric-cross-availability-zones) will provide more guidance on how to design an Azure based Service Fabric cluster which can span availability zones.

The [Service Fabric documentation][service-fabric-docs] includes a rich set of tutorials and conceptual articles, which serve as a good complement to the samples.

<!-- Links -->

[service-fabric-samples]: http://aka.ms/servicefabricsamples
[service-fabric-programming-models]: https://azure.microsoft.com/en-us/documentation/articles/service-fabric-choose-framework/
[app-upgrade-tutorial]: https://azure.microsoft.com/en-us/documentation/articles/service-fabric-application-upgrade-tutorial/
[service-fabric-docs]: http://aka.ms/servicefabricdocs
