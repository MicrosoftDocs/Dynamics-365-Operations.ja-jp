---
title: 委託販売の設定
description: このトピックでは、入庫委託販売在庫工程をコンフィギュレーションする方法を説明します。
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 04b3fb3038a1373e203ec240a0163cf67de655cc
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813856"
---
# <a name="set-up-consignment"></a>委託販売の設定

[!include [banner](../includes/banner.md)]

このトピックでは、入庫委託販売在庫工程をコンフィギュレーションする方法を説明します。

委託販売在庫は、仕入先によって所有されているが、サイトで保管されている在庫です。 在庫を消費するか、または使用する準備ができたら、在庫の所有権を引き継ぎます。 このトピックでは、委託販売プロセスを有効にするのに必要な設定について説明します。 委託販売プロセスに関する詳細については、[委託販売の設定](consignment.md) を参照してください。

## <a name="inventory-owners"></a>在庫所有者
現物入庫の委託販売の在庫を記録するには、仕入先の所有者を定義する必要があります。 これは、**在庫所有者**のページで行われます。 **仕入先口座**を選択すると、**名前**と**所有者**のフィールドの規定値が生成されます。 **所有者**フィールドの値が仕入先に表示されるので、仕入先口座名が外部ユーザーに認識されにくい場合は変更することができます。 **所有者**フィールドを編集できますが、**在庫所有者**記録を保存する時点までです。 **名前**フィールドには、仕入先口座が関連付けられている当事者名を入力できますが、変更できません。

[![在庫所有者](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>追跡用分析コード グループ
委託販売プロセスで使用される品目は、**所有者**分析コードが**有効**に設定されている**追跡用分析コード グループ**に関連付けられている必要があります。 所有者分析コードは、常に**現物在庫**と**資産在庫**オプションが選択されます。 **分析コード別補充計画**は選択されません。

[![追跡用分析コード グループ](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)

## <a name="inventory-ownership-change-journal"></a>在庫所有権変更仕訳
**在庫所有権変更**仕訳張は、委託販売在庫の所有権の仕入先から消費している法人への移転の記録に使用されます。 在庫仕訳帳のように、在庫仕訳帳の名前で識別する必要があります。 これらの名前は、**在庫仕訳帳の名前**ページで作成され、**仕訳帳タイプ**は、**所有権変更**に設定する必要があります。

[![在庫所有権変更仕訳](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>委託販売プロセスでの仕入先コラボレーション
仕入先コラボレーション インターフェイスを使用している仕入れ先は、サイトで在庫の消費を監視するために、これを使用することもできます。 仕入先コラボレーションを使用する仕入先の設定については、[仕入先ポータルのユーザー セキュリティ](../procurement/configure-security-vendor-portal-users.md) を参照してください。
