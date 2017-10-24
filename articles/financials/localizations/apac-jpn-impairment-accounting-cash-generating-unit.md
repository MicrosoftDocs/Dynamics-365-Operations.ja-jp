---
title: "キャッシュ生成単位の固定資産の減損会計"
description: "この記事では、Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition に含まれる固定資産の減損の機能を紹介します。 この記事の主な目的は、ユーザーに減損会計の概念モデルの概要を示すことです。"
author: rake-gui
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetAllocationGoodwillSharedAsset_JP, AssetCashGeneratingUnit_JP, AssetCashGeneratingUnitGroup_JP, AssetImpairmentRecognitionMethod1_JP, AssetImpairmentRecognitionMethod2_JP
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 25691
ms.search.region: Japan
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1655a1b2d62fefc1f46fee6dceea3180e103e6e0
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="fixed-asset-impairment-accounting-on-cash-generating-units"></a>キャッシュ生成単位の固定資産の減損会計

[!include[banner](../includes/banner.md)]


この記事では、Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition に含まれる固定資産の減損の機能を紹介します。 この記事の主な目的は、ユーザーに減損会計の概念モデルの概要を示すことです。 

固定資産は、管理不良、新規競合、および技術革新などの要因によって、その価値の減損 (減少) の影響を受けやすい場合があります。 減損損失は損益勘定で表示されます。 減損価値は、固定資産または利益生成単位の値を回収可能金額と比較して測定されます。 回収可能金額は、固定資産またはその工程から生成される収益の売上から取得できる最大値です。 日本では、固定資産の減損は、日本の一般会計原則 (GAAP) の 第 6 項目に従って行い、2 つのステップがある方法を使用します。 最初のステップは、減損損失の認識テストで、2 つ目のステップは減損損失の測定です。 減損後、回収可能金額は、将来の減価償却計算のための固定資産の新しい正味簿価額となります。 減損の作業プロセスには次の主要タスクが含まれます。

## <a name="cgu-groups"></a>CGU グループ
基本ページは、**CGU グループ**です (**固定資産** &gt; **設定** &gt; **減損** &gt; **CGU グループ**)。 CGU グループは、減損プロセスの組み合わせ全体です。 特定の CGU グループでは、1 つのキャッシュ生成単位のみに 1 つの特定の固定資産を割り当てることができます。 この制限は、ユーザーが別の CGU グループを作成し、そのグループでキャッシュ生成単位を作成するときに適用されません。 複数の CGU グループの作成は、固定資産の最も適したグループを検索するためのシミュレーションに役立ちます。

## <a name="cash-generating-units"></a>キャッシュ生成単位
基本ページは、**キャッシュ生成グループ**です (**固定資産** &gt; **設定** &gt; **減損** &gt; **キャッシュ生成グループ**)。 ユーザーは CGU グループでキャッシュ生成単位を作成し、個別の固定資産をキャッシュ生成単位に割り当てることができます。 ユーザーは、これらの資産が共有資産または営業権である場合、CGU グループに直接固定資産を割り当てることもできます。 共有資産と無形固定資産の減損は、日本の GAAP のメソッド I に従って、CGU グループ単位でテストおよび測定されます。 ユーザーは、メソッド II も適用できます。 この場合、ユーザーは各キャッシュ生成単位に、共有資産および営業権の正味簿価額を割り当てる必要があります。

### <a name="optional-allocating-the-net-book-value-of-shared-assets-and-goodwill"></a>オプション: 共有資産と営業権の正味簿価額の配賦

基本ページは、**営業権と共有資産の正味簿価額の配賦**です (**固定資産** &gt; **設定** &gt; **減損** &gt; **営業権と共有資産の正味簿価額の配賦**)。 ユーザーが CGU グループにメソッド II を適用する場合、共有資産と営業権の正味簿価額を各キャッシュ生成単位に割り当てる必要があります。

## <a name="impairment-recognition-test"></a>減損認識テスト
基本ページは、**固定資産** &gt; **調整**です。 メソッド I またはメソッド II が適用されるかによってサブメニューが異なります。 減損の最初の手順は、認識テストです。 割引のない将来のキャッシュ フローが、帳簿価額 (または正味簿価額) を比較する基準として使用されます。 この将来のキャッシュ フローが資産の正味簿価額を満たしていない場合、減損の測定では仕訳帳金額が認識されます。

## <a name="measurement-of-the-impairment-amount"></a>減損金額の測定
2 つ目のステップは減損金額の測定です。 回収可能金額は、減損金額を計算するために固定資産の正味簿価額から差し引かれます。 回収可能金額は、使用中の値または資産の市場価値のいずれかより高いほうになります。 2 つのステップは、同じページで行います。

## <a name="posting-the-impairment"></a>減損の転記
減損金額の認識テストおよび測定の後、ユーザーは各固定資産に対する減損金額を転記できます。 転記後に、償却提案では減損金額が考慮され、正しい減価償却金額が提案されます。

## <a name="reports-and-other-required-operations"></a>レポートおよびその他の必要な工程
ユーザーは**減損レポートおよびトランザクション**照会ページを使用して、減損トランザクションに関する詳細情報を取得できます。 会社の税務申告の調整など特定の工程が、減損の転記後に必要です。 ユーザーは、これらの工程を手動で計算して転記する必要があります。

## <a name="additional-resources"></a>その他のリソース
- [固定資産の減損会計](apac-jpn-impairment-accounting-fixed-assets.md)
- [資産グループの減損損失の提案と転記](./tasks/propose-post-impairment-amount-cash-generating-unit.md)


