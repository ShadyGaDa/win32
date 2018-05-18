---
title: Linked Attributes
description: Linked attributes are pairs of attributes in which the system calculates the values of one attribute (the back link) based on the values set on the other attribute (the forward link) throughout the forest.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\mbaldwin
ms.assetid: '31b7e8f5-e46d-4aff-9b17-c8dec7f19bae'
ms.prod: 'windows-server-dev'
ms.technology: 'active-directory-domain-services'
ms.tgt_platform: multiple
keywords: ["Linked Attributes AD", "Attributes AD ,linked"]
---

# Linked Attributes

Linked attributes are pairs of attributes in which the system calculates the values of one attribute (the back link) based on the values set on the other attribute (the forward link) throughout the forest. A back-link value on any object instance consists of the DNs of all the objects that have the object's DN set in the corresponding forward link. For example, "Manager" and "Reports" are a pair of linked attributes, where Manager is the forward link and Reports is the back link. Now suppose Bill is Joe's manager. If you store the DN of Bill's user object in the "Manager" attribute of Joe's user object, then the DN of Joe's user object will show up in the "Reports" attribute of Bill's user object.

A forward link/back link pair is identified by the [**linkID**](https://msdn.microsoft.com/library/ms676831) values of two [**attributeSchema**](https://msdn.microsoft.com/library/ms680969) definitions. The **linkID** of the forward link is an even, positive, nonzero value, and the **linkID** of the associated back link is the forward **linkID** plus one. For example, the **linkID** for "Manager" is 42 and the **linkID** for "Reports" is 43.

The following is a list of guidelines for defining a new pair of linked attributes:

-   The [**linkID**](https://msdn.microsoft.com/library/ms676831) values must be unique among all [**attributeSchema**](https://msdn.microsoft.com/library/ms680969) objects. To avoid conflicts, you should auto-generate the **linkID** by following the instructions in the topic [Obtaining a Link ID](obtaining-a-link-id.md).
-   A back link must have a corresponding forward link, that is, the forward link must exist before a corresponding back link attribute can be created.
-   A back link is always a multi-valued attribute. A forward link can be single-valued or multi-valued. Use a multi-valued forward link when there is a many-to-many relationship.
-   The [**attributeSchema**](https://msdn.microsoft.com/library/ms680969) value of a forward link must be 2.5.5.1, 2.5.5.7, or 2.5.5.14. These values correspond to syntaxes that contain a distinguished name, such as the [**Object(DS-DN)**](https://msdn.microsoft.com/library/ms684431) syntax.
-   The [**attributeSchema**](https://msdn.microsoft.com/library/ms680969) value of a back link must be 2.5.5.1, which is the [**Object(DS-DN)**](https://msdn.microsoft.com/library/ms684431) syntax.
-   By convention, back link attributes are added to the [**mayContain**](https://msdn.microsoft.com/library/ms677072) value of the [**top**](https://msdn.microsoft.com/library/ms683975) abstract class. This enables the back link attribute to be read from objects of any class because they are not actually stored with the object, but are calculated based on the forward link values.

 

 



