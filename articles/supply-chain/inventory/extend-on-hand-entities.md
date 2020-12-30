---
title: 手持在庫データ エンティティの拡張
description: このトピックでは、INVENTORSITEONHANDENTITY と INVENTWAREHOUSEONHANDENTITY ビューに拡張フィールドを追加して、手持在庫データ エンティティの機能が拡張で使用できるようにする例を示します。
author: sherry-zheng
manager: tfehr
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e3bf3a7d48b0aa3e48845882be0ee86da17ed040
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432034"
---
# <a name="extend-inventory-on-hand-data-entities"></a>手持在庫データ エンティティの拡張

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management には、[拡張機能を使用してテーブルにフィールドを追加](../../fin-ops-core/dev-itpro/extensibility/add-field-extension) できる [拡張性](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) 機能が用意されています。 このトピックでは、`INVENTORSITEONHANDENTITY` と `INVENTWAREHOUSEONHANDENTITY` ビューに拡張フィールドを追加して、手持在庫データ エンティティの機能が拡張で使用できるようにする例を示します。 データ エンティティの詳細については、[データ管理の概要](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md) を参照してください。

> [!NOTE]
> 手持在庫データ エンティティの一覧を以下に示します:
>
> - サイトごとの手持在庫
> - サイトごとの手持在庫 V2
> - 倉庫ごとの手持在庫
> - 倉庫別手持在庫 v2

`inventSiteOnHandView` ビューによって使用されるテーブルにフィールドを追加した後、拡張機能が正しく認識されるようにエンジンを同期する必要があります。

1. 拡張子フィールドを追加して、`InventSiteOnHandView` ビューを拡張します。
1. 拡張子フィールドで `InventSiteOnHandAggregatedView` ビューを拡張します。
1. `getExtensionFields()` メソッドを変更して、`InventSiteOnHandAggregatedViewBuilder` viewBuilder クラスを拡張します。 このようにして、viewBuilder の同期が実行されたときに、古いビュー フィールドを新しいビュー フィールドにマップします。

たとえば、拡張機能を使用して、次の 4 つのフィールドを `InventTable` テーブルに追加したとします。

- カスタム フィールド 1
- カスタム フィールド 2
- カスタム フィールド 3
- カスタム フィールド 4

この場合は、次の方法で `getExtensionFields()` メソッドを変更する必要があります。

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

これらの手順を完了した後で、新しいフィールドを追加することで、サイト別の手持在庫と倉庫データ エンティティ別の手持在庫を拡張できます。 このようにして、これらのデータ エンティティを使用するデータ移行中に、拡張フィールドが認識されて含まれるようにします。
