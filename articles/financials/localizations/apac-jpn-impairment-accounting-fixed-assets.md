---
title: 日本の固定資産の減損会計
description: このトピックでは、日本の固定資産の減損会計に関する情報について説明します。
author: yijialuan
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetImpairmentAssetTransInquire_JP, AssetImpairmentIndicator_JP, AssetImpairmentManageTestResult_JP
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 28811
ms.search.region: Japan
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb9dc86b3c12ca29ec249319483bc37ca7c71db6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552777"
---
# <a name="impairment-accounting-for-fixed-assets-for-japan"></a>日本の固定資産の減損会計

[!include [banner](../includes/banner.md)]

このトピックでは、日本の固定資産の減損会計に関する情報について説明します。

Microsoft Dynamics 365 for Finance and Operations を使用して、固定資産の減損を設定および計算するには、次のタスクを実行できます。

-   減損された可能性のある固定資産の一覧を生成します。 一覧の各資産の値引き前キャッシュ フロー、公正価額、復旧可能な金額を手動で確認し、計算して、固定資産が減損されるかどうかを決定できます。
-   固定資産の値引き前キャッシュ フローなど減損のインジケーターを更新します。
-   減損のインジケーターを使用して減損の認識テストを実行し、減損された固定資産の一覧を生成します。
-   固定資産が減損される程度を示す回収可能金額を指定し、減損された固定資産の仕訳帳トランザクションを作成できます。 仕訳帳を転記する前に、減損に関する詳細を指定できます。
-   固定資産の減損のトランザクションの詳細を表示します。

## <a name="how-can-i-identify-impairments-in-fixed-assets"></a>固定資産の減損をどのように識別できますか。
固定資産の減損を識別するために減損のインジケーターを使用できます。 **減損の確認**ページで、減損しているとみられる固定資産の一覧を生成できます。 値引き前キャッシュ フローを手動で計算し、**減損インジケーターの更新**ページで固定資産の減損インジケーターを更新します。 減損の認識テストの実行時に、固定資産の減損を識別するには、更新した減損インジケーターを使用できます。

## <a name="can-i-select-which-assets-to-test-for-impairment"></a>減損をテストする資産を選択できますか。
減損をテストする資産を選択できます。 基準を指定するには、**減損認識のテスト**ページの**クエリ**をクリックします。

## <a name="how-often-can-i-check-fixed-assets-for-impairment"></a>減損について固定資産をどれほどの頻度で確認できますか。
バッチ ジョブを作成して、スケジュールに基づいて減損について固定資産を確認するよう Finance and Operations を設定できます。

## <a name="are-there-types-of-fixed-assets-that-are-excluded-from-impairment-testing-and-accounting"></a>減損のテストおよび会計から除外された固定資産のタイプがありますか。
固定資産の次のタイプは、減損のテストおよび会計から除外されます。

-   リースした固定資産
-   共有資産
-   無形固定資産の固定資産

営業権と共有資産を計算するために資産グループの減損を使用する必要があります。

## <a name="can-i-generate-reports-that-i-can-use-to-review-impaired-assets-and-impairment-amounts"></a>減損された資産と減損金額を確認するために使用するレポートを生成できますか。
減損された資産と減損の会計に関する情報を含む次のレポートを生成できます。

-   固定資産トランザクション レポート
-   固定資産減損トランザクション レポート
-   減損損失レポートのための固定資産の確認

## <a name="additional-resources"></a>その他のリソース
- [キャッシュ生成単位の固定資産の減損会計](apac-jpn-impairment-accounting-cash-generating-unit.md)
- [個別資産の減損インジケーターの管理](./tasks/maintain-impairment-indicators-individual-assets.md)
- [バッチごとの減損損失の提案と転記](./tasks/propose-post-impairment-amount-batch.md)
- [固定資産仕訳帳を使用した減損損失の提案と転記](./tasks/propose-post-impairment-amount-fixed-asset-journal.md)
- [認識テストの実行と個別資産の減損損失の計算](./tasks/run-recognition-test-calculate.md)
- [減損会計の共通パラメーターおよび転記プロファイルの設定](./tasks/impairment-accounting.md)


