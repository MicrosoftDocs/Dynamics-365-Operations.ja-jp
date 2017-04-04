---
title: "原価計算の分析のPower BIの内容のセキュリティを設定します。"
description: "このトピックでは、Microsoft Power BI行レベル セキュリティに原価計算のアクセス レベルのセキュリティを反映する方法を説明します。 この機能は、アクセス許可されているユーザーがPower BIデータのみが表示される保証ができます。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1e42622e7621c645d7eda3299f78c34c7e41a251
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>原価計算の分析のPower BIの内容のセキュリティを設定します。

このトピックでは、Microsoft Power BI行レベル セキュリティに原価計算のアクセス レベルのセキュリティを反映する方法を説明します。 この機能は、アクセス許可されているユーザーがPower BIデータのみが表示される保証ができます。

<a name="overview"></a>概要
--------

Microsoft Power BI **原価計算の分析**内容は、ユーザー アクセスを制限するのにPower BI行レベル セキュリティを使用します。 セキュリティは、原価計算パラメータで設定されたアクセス レベルの組織階層に基づきます。 Power BI **原価計算の分析**内容に関する詳細については、" [原価計算の分析のPower BIの内容] (原価-分析内容pack.md)。

## <a name="setup"></a>段取り
Power BIにアクセス レベルのセキュリティを反映するには、Power BIの内容の所有者は、次の手順にしなければなりません。 **注記: **自動的にPower BI **原価計算の分析**内容を公開するユーザーは、所有者になります。 所有者のみPower BIのセキュリティを設定できます。 また所有者がPower BI **原価計算の分析**内容のデータを表示できる以外の所有者がPowerBI.comから別のユーザーを追加するまで、従業員があります。

1.  Power BIに定義ファイルを公開します。
2.  PowerBI.comに署名します。
3.  Power BI **原価計算の分析**内容のデータセットを検索します。
4.  セキュリティのページを開きます。 

    [セキュリティ]ページ (https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)] (https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)![を開く

5.  **原価のオブジェクトの会計監査役**ロールが既に作成されます。 原価計算のアクセス レベルの組織階層の一部であるそのほかのメンバを追加します。 

    [メンバ] (https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)] (https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)を追加する![

**原価のオブジェクトの会計監査役**ロールに追加するユーザーは、原価計算のアクセス レベルの組織階層の定義に従って、表示を許可するデータのみが表示されます。 **注記: **行レベル セキュリティはPower BIに組み入れる、Microsoft Dynamics 365のタイルおよびレポートに適用されます。

## <a name="updating-security"></a>セキュリティの更新
更新が原価計算のアクセス レベルのセキュリティに行われ、Power BIにそれらの更新を反映する場合Power BI **原価計算の分析**内容のエンティティの店舗を更新する必要があります。 Dynamics 365 for Operationsのエンティティの店舗の更新が完了したら、PowerBI.comのコンポーネントを更新する必要があります。 エンティティ方法の詳細については、"更新を保存します。[更新のエンティティの店舗] (能力Bi統合エンティティstore.md#updateエンティティ店舗)。 Power BI **原価計算の分析**内容の所有者は、新しいユーザーが組織階層へのアクセスを許可するエンティティの店舗の更新を実行する必要があります。 また、所有者はPowerBI.comの**オブジェクトのコントローラを要して。**ロールに行レベル セキュリティがそれらに対して適用されるように、新しいユーザーを追加する必要があります。

## <a name="disabling-security"></a>無効にするセキュリティ
ただし、組織のデータ アクセスを制限するとします。 原価計算を実行すると、何らかの理由で、セキュリティ パラメータが無効な場合、所有者が代わりのPower BI **原価会計係**ロールにユーザーを追加する必要があります。 有効ステータスから無効のステータスにセキュリティを変更すると、**オブジェクトのコントローラを要して。**ロールのユーザーを削除することをお勧めします。 セキュリティを再び有効にするとまたその対象になります。 ユーザーは、両方のロールに属することができます。 連アクセスは、両方のロールの組合です。 Power BI **原価計算の分析**内容の場合、連アクセスが制限されていないデータ アクセスできるのユーザー。 目標を制限付きアクセスを適用する場合は、ユーザーは**オブジェクトのコントローラを要して。**ロールにのみ割り当てる必要があります。 これらの明細レベル セキュリティの更新はすぐに反映されます。 影響を受けるユーザーが自分のブラウザを更新する必要があります。

## <a name="additional-resources"></a>追加リソース
Power BI行レベル セキュリティの詳細については、" "を参照してください[Power BI管理します。] (https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model)のモデルのセキュリティを。


