---
title: 購買入庫におけるプロジェクト費用見越し額
description: この記事では、購買入庫での未収プロジェクト費用を、Microsoft Microsoft Dynamics 365 Finance で追跡する方法について説明します。
author: mukumarm
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: twheeloc
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: mukumarm
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 56b8b5a6f91c6a18b53739b1e9369bda64131a06
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715859"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a>購買入庫におけるプロジェクト費用見越し額

[!include [banner](../includes/banner.md)]

この記事では、購買入庫での未収プロジェクト費用を、Microsoft Microsoft Dynamics 365 Finance で追跡する方法について説明します。 

プロジェクトの請求書は、商品やサービスが提供された後に到着することが多く、プロジェクトの主要業績評価指標 (KPIs) に重大な影響を及ぼす可能性があります。 財務およびプロジェクト レポート両方におけるトランザクションを追跡できるのは重要なことです。

次のシナリオはこのような例を示しています。 

Contoso コンサルティングは新しいクラウド配置プロジェクトを開始しました。 プロジェクトのためのコンピューターを購入するために発注書が作成されます。 コンピューターは 1500 ドル、インストール サービスは 150 ドルかかります。 仕入先からコンピュータが届き、インストールしましたが、請求書がまだ Contoso コンサルティングに届いていません。 プロジェクト マネージャーは、請求書が送信される前にプロジェクト費用が 1650 ドルであることを期待しています。 この原価は会社の月末財務諸表にも反映される必要があります。 

未払費用は、報告目的のために財務レベルとプロジェクトレベルの両方に記録する必要があります。 製品入庫における財務更新は品目および調達カテゴリに対して追跡できます。 

品目に対して、**買掛金勘定パラメーター** ページで、**製品入庫を元帳に転記** オプションを選択します。
[![買掛金勘定パラメーター ページ。](./media/accruals1-1024x409.png)](./media/accruals1.png) 

調達カテゴリに対して、**カテゴリのポリシー ルール** ページで、**購入** ポリシーを選択し、各調達カテゴリに対して **入庫時の未収購買経費** を選択します。
[![カテゴリ ポリシー ルールのページ。](./media/accruals2-1024x569.png)](./media/accruals2.png) 

**転記設定** の **購買支出、未請求** と **購買見越計上** 勘定は、製品の入庫に関連付けられている伝票が転記されるときに使用されます。

この同じシナリオを使用して、製品入庫の転記が、総勘定元帳とプロジェクト情報へどのような影響を与えるかを見てみます。 

**ステップ 1:** プロジェクトの新規発注書を作成して確認し、購入したコンピューターを 1500 ドル、インストール サービスを 150 ドルで記録します。
[![新しい発注書の作成。](./media/accruals4-1024x497.png)](./media/accruals4.png) 

発注書が確定されると、確定済費用のトランザクションが、プロジェクトに対して作成されます。 
[![作成されたトランザクション。](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> 確定済費用のトランザクションには、**発注書** に対して設定された **トランザクションの発生元** フィールドがあります。 発注書を登録し、確認しても、プロジェクトのトランザクションは登録されません。 

**ステップ 2:** 商品とサービスが提供され、製品入庫が登録されます。 

製品入庫を転記すると、元帳に伝票が生成され、転記されます。 伝票により、購買支出、未請求済発注の勘定、貸方額勘定は借方転記されます。 
[![伝票トランザクション。](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> 製品入庫が転記されると、プロジェクト カテゴリに対して、転記設定が使用されるのではなく、調達カテゴリおよび製品に対して転記設定が使用されます。 購買見越しの財務的影響を正確に反映させるためには、この設定を調整する必要があります。 

調達カテゴリを **調達カテゴリ ページ** のプロジェクト カテゴリにマップすることができます。
[![調達カテゴリ ページ。](./media/accruals7-1024x390.png)](./media/accruals7.png)

**ステップ 3:** 仕入先請求書の下書きを作成します。 

製品入庫を転記しても、プロジェクト情報には影響しません。 回避手段として、購買入庫の転記の直後に仕入先請求書の下書きを生成できます。 **発注書** ページ &gt; **請求書のタブ** &gt; **生成** &gt; **請求書** の順に移動します。 これにより、プロジェクト情報を更新する保留中の請求書ドキュメントが作成されます。 

仕入先請求書の草案を作成すると、保留中のプロジェクト トランザクションが生成されます。 
[![保留中のプロジェクト トランザクション。](./media/accruals8-1024x225.png)](./media/accruals8.png) 

**確定済費用** ページでは、ステップ 1 で作成されたレコードが閉まり、保留中の仕入先請求書から取得される費用の約定を反映する新しいレコードが作成されます。 確定済費用の **トランザクションの発生元** フィールドは **仕入先請求書** に対して設定されます。
[![確定済み費用のページ。](./media/accruals9-1024x200.png)](./media/accruals9.png)

仕入先請求書は、実際の仕入先請求書が到着するまで保留中のステータスとして保持されます。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
