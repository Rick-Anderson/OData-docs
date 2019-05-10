---
title : "14.6 OData Web API 7.1.0 (.NET Core and .NET Classic)"
description: "7.1.0 release notes"
category: "14. 7.x Features "
ms.date: 11/19/2018
---
# 14.6 OData Web API 7.1.0 (.NET Core and .NET Classic)

The NuGet packages for ASP.NET Web API OData v7.1.0 are available on the [NuGet gallery](https://www.nuget.org/).

You can install or update the NuGet packages for OData Web API v7.1.0 using the [Package Manager Console](https://docs.nuget.org/docs/start-here/using-the-package-manager-console):

```
PM> Install-Package Microsoft.AspNetCore.OData -Version 7.1.0 
```
or
```
PM> Install-Package Microsoft.AspNet.OData -Version 7.1.0
```

>[!Notes]:
>[issue #1591](https://github.com/OData/WebApi/issues/1591) fixes an issue where types created by the ODataModelBuilder did not respect the namespace of the >ModelBuilder and instead used the namespace of the CLR type. With [PR #1592](https://github.com/OData/WebApi/pull/1592), OData WebAPI 7.1.0 now correctly uses the namespace on the ModelBuilder, if it has been explicitly set. In order to retain the old behavior of using the namespace of the CLR type, do not set the namespace on the ModelBuilder, or set the namespace on the ModelBuilder to null or to the desired namespace of the CLR type.

## What’s in this release?

### New Features:

* [ [#1631](https://github.com/OData/WebApi/issues/1631) ] Don't require keys for singleton instances

* [ [#1628](https://github.com/OData/WebApi/pull/1628) ] Allow adding new members to a collection through a POST request

* [ [#1591](https://github.com/OData/WebApi/issues/1591) ] Support namespaces in OData ModelBuilder

* [ [#1656](https://github.com/OData/WebApi/issues/1656) ] Allowing the definition of partner relationships


### Improvements and fixes:

* [ [#1543](https://github.com/OData/WebApi/issues/1543) ] Json batch response body if 404

* [ [#1555](https://github.com/OData/WebApi/issues/1555) ] aspnetcore ETagMessageHandler throws then ClrType property name and EdmModel property name differs

* [ [#1559](https://github.com/OData/WebApi/issues/1559) ] Don't assume port 80 for nextLink when request was HTTPS

* [ [#1579](https://github.com/OData/WebApi/issues/1579) ] Star select ( $select= * ) not returning dynamic properties

* [ [#1588](https://github.com/OData/WebApi/pull/1588) ] Null check on ODataQueryParameterBindingAttribute for Net Core

* [ [#736](https://github.com/OData/WebApi/issues/736) ] EDMX returned from $metadata endpoint has incorrect "Unicode" attributes

* [ [#850](https://github.com/OData/WebApi/issues/850) ] ODataConventionModelBuilder takes into account [EnumMember] on enum members, but ODataPrimitiveSerializer (?) does not, causing mismatch in the payload.

* [ [#1612](https://github.com/OData/WebApi/pull/1612) ] Add the iconUrl to the nuget spec

* [ [#1615](https://github.com/OData/WebApi/pull/1615) ] fix compile error in sample project

* [ [#1421](https://github.com/OData/WebApi/issues/1421) ] Improve error message when structured type is received and properties are in incorrect case

* [ [#1658](https://github.com/OData/WebApi/pull/1658) ] Fix the security vulnerabilities in project dependencies

* [ [#1637](https://github.com/OData/WebApi/issues/1637) ] Change Request: Remove null check on 'ODataFeature().TotalCount' property

* [ [#1673](https://github.com/OData/WebApi/pull/1673) ] Respect preference header for paging

* [ [#1600](https://github.com/OData/WebApi/issues/1600) ] ActionDescriptorExtensions is not thread safe

* [ [#1617](https://github.com/OData/WebApi/issues/1617) ] Take and Top query use wrong Provider.CreateQuery Method

* [ [#1659](https://github.com/OData/WebApi/issues/1659) ] Odata V4 group by with Top and skip not working

* [ [#1679](https://github.com/OData/WebApi/issues/1679) ] Fix typo routePrerix

---

## Questions and feedback

You and your team are warmly welcomed to try out this new version if you are interested in the new features and fixes above. You are also welcomed to contribute your code to [OData Web API repository](https://github.com/OData/WebApi). For any feature request, issue or idea please feel free to reach out to us at 
[GitHub Issues](https://github.com/OData/WebApi/issues). 