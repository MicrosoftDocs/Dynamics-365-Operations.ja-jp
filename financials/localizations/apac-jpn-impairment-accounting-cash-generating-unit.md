---
title: "キャッシュ生成単位の固定資産の減損会計"
description: "この記事では、Microsoft Dynamics AX に含まれる固定資産の減損の機能を紹介します。 この記事の主な目的は、ユーザーに減損会計の概念モデルの概要を示すことです。"
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetAllocationGoodwillSharedAsset_JP, AssetCashGeneratingUnit_JP, AssetCashGeneratingUnitGroup_JP, AssetImpairmentRecognitionMethod1_JP, AssetImpairmentRecognitionMethod2_JP
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25691
ms.assetid: c87ac196-8dc6-4636-99a3-be478ddd8efe
ms.search.region: Japan
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: cc4b2e23c302a16109bd6326e06c15e4a0ce9b5b
ms.lasthandoff: 03/31/2017


---

# <a name="fixed-asset-impairment-accounting-on-cash-generating-units"></a>キャッシュ生成単位の固定資産の減損会計

この記事では、Microsoft Dynamics AX に含まれる固定資産の減損の機能を紹介します。 この記事の主な目的は、ユーザーに減損会計の概念モデルの概要を示すことです。 

固定資産は、管理不良、新規競合、および技術革新などの要因によって、その価値の減損 (減少) の影響を受けやすい場合があります。 減損損失は損益勘定で表示されます。 減損価値は、固定資産または利益生成単位の値を回収可能金額と比較して測定されます。 回収可能金額は、固定資産またはその工程から生成される収益の売上から取得できる最大値です。 日本では、固定資産の障害はに従ってNO実行されます。 二つの手順で方法を使用する日本の一般会計原則 ((GAAP)の6。 最初の手順は、障害の損失が認識テストで、2番目の手順は、障害の損失の測定単位です。 障害後に、および可能な金額は将来の減価償却計算の新しい固定資産の正味簿価額があります。 減損の作業プロセスには次の主要タスクが含まれます。

## <a name="cgu-groups"></a>CGU グループ
基本ページがありますCGU **のグループ (** **固定資産** &gt; **設定** &gt; **障害** &gt; ** CGUのグループ**)。 CGUのグループは、障害プロセス全体の組み合わせです。 特定のCGUのグループで、ユーザーは単位を生成する1の現金のみに一つの特定の固定資産を割り当てることができます。 この制限は、ユーザーが別の CGU グループを作成し、そのグループでキャッシュ生成単位を作成するときに適用されません。 複数の CGU グループの作成は、固定資産の最も適したグループを検索するためのシミュレーションに役立ちます。

## <a name="cash-generating-units"></a>キャッシュ生成単位
基本ページは、**グループを生成するには、現金にキャッシュ インフロー**します (**固定資産** &gt; **設定** &gt; **障害** &gt; **グループを生成するには、現金にキャッシュ インフロー**します)。 ユーザーは CGU グループでキャッシュ生成単位を作成し、個別の固定資産をキャッシュ生成単位に割り当てることができます。 ユーザーは、これらの資産が共有資産または営業権である場合、CGU グループに直接固定資産を割り当てることもできます。 共有資産と無形固定資産の減損は、日本の GAAP のメソッド I に従って、CGU グループ単位でテストおよび測定されます。 ユーザーは、メソッド II も適用できます。 この場合、ユーザーは各キャッシュ生成単位に、共有資産および営業権の正味簿価額を割り当てる必要があります。

### <a name="optional-allocating-the-net-book-value-of-shared-assets-and-goodwill"></a>オプション: 共有資産と営業権の正味簿価額の配賦

基本ページがあります好意**、または資産の正味簿価額の配賦** (**固定資産** &gt; **設定** &gt; **障害** &gt; **好意、または資産の正味簿価額の配賦**)。 ユーザーが CGU グループにメソッド II を適用する場合、共有資産と営業権の正味簿価額を各キャッシュ生成単位に割り当てる必要があります。

## <a name="impairment-recognition-test"></a>減損認識テスト
基本ページが**固定資産** ** &gt; 調整**です。 メソッド I またはメソッド II が適用されるかによってサブメニューが異なります。 減損の最初の手順は、認識テストです。 割引のない将来のキャッシュ フローが、帳簿価額 (または正味簿価額) を比較する基準として使用されます。 この将来のキャッシュ フローが資産の正味簿価額を満たしていない場合、減損の測定では仕訳帳金額が認識されます。

## <a name="measurement-of-the-impairment-amount"></a>減損金額の測定
2 つ目のステップは減損金額の測定です。 回収可能金額は、減損金額を計算するために固定資産の正味簿価額から差し引かれます。 回収可能金額は、使用中の値または資産の市場価値のいずれかより高いほうになります。 2 つのステップは、同じページで行います。

## <a name="posting-the-impairment"></a>減損の転記
減損金額の認識テストおよび測定の後、ユーザーは各固定資産に対する減損金額を転記できます。 転記後に、償却提案では減損金額が考慮され、正しい減価償却金額が提案されます。

## <a name="reports-and-other-required-operations"></a>レポートおよびその他の必要な工程
ユーザーは**減損レポートおよびトランザクション**照会ページを使用して、減損トランザクションに関する詳細情報を取得できます。 会社の税務申告の調整など特定の工程が、減損の転記後に必要です。 ユーザーは、これらの工程を手動で計算して転記する必要があります。

<a name="see-also"></a>参照
--------

[設定されたMicrosoft Dynamics AX 2012 R3の固定資産のローカリゼーション機能]日本] (https://mbs.microsoft.com/partnersource/global/deployment/documentation/white-papers/msdAX2012R3JapanFixedAssets)


