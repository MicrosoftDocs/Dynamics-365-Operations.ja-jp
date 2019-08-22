---
title: Lifecycle Services (LCS) のライセンス数見積もりツール
description: この記事では、Microsoft Dynamics Lifecycle Services (LCS) のライセンス数見積もりツールに関する情報を提供します。 ライセンス数見積もりツールは、組織の Microsoft Dynamics AX に必要なライセンスの数の予測に役立ちます。 また、データを入力してレポートを生成する方法についても説明します。これで、ツールの使用を開始できます。
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 13381
ms.assetid: 6f5723b9-a2f5-40e1-9a95-2fd5f6b9fd84
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 58ff80f52043a6674504cc7dac346e75ea079d08
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850539"
---
# <a name="license-sizing-estimator-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) のライセンス数見積もりツール

[!include [banner](../../includes/banner.md)]

この記事では、Microsoft Dynamics Lifecycle Services (LCS) のライセンス数見積もりツールに関する情報を提供します。 ライセンス数見積もりツールは、組織の Microsoft Dynamics AX に必要なライセンスの数の予測に役立ちます。 また、データを入力してレポートを生成する方法についても説明します。これで、ツールの使用を開始できます。

Microsoft Dynamics Lifecycle Services (LCS) では、ライセンス数見積もりツールは、組織の Microsoft Dynamics AX に必要なライセンスの数の予測に役立ちます。 これは、既定またはカスタマイズされたロールをモデル化して、必要なクライアント アクセス ライセンス (CAL) を自動的に計算するために使用できる共有ワークスペースを提供します。 ライセンス数見積もりツールは、次の状況で使用できる情報を提供します。

-   顧客が Microsoft DynamicsAX を購入する前に
-   既存の Microsoft DynamicsAX の実装を展開する前に
-   新しいバージョンの Microsoft Dynamics AX にアップグレードする前に

いくつかの方法で、ロールおよびその関連する職務を定義することができます。 ライセンス数見積もりツールは、Microsoft Dynamics AX に含まれる既定のロールを提供します。 顧客の組織内のロールを適切に説明している場合、これらの定義済みロールのいずれかを使用することができます。 定義済みのロールが組織の要件を満たしていない場合は、職務を追加したり、職務を削除してカスタム ロールをモデル化することができます。 使用可能な職務の一覧から新しいロールをモデル化することもできます。 **重要**: ライセンス数見積もりツールで定義したロールは、Microsoft Dynamics AX にエクスポートできません。 Microsoft Dynamics AX でカスタム ロールを実装するには、「[Microsoft Dynamics AX でユーザー セキュリティを設定する](http://technet.microsoft.com/library/a9eea83b-60bf-4690-8442-a459de3c2001(AX.60).aspx)」を参照してください。 組織内のロールを定義した後は、入力した情報を要約したレポートを表示することができます。 このレポートは、組織が必要とするライセンスの数と種類を自動的に推定します。 見積は、各ロールに含まれる職務を実行するために必要な CAL レベル、および各ロールの人数に基づいています。 見積は、ユーザーが Microsoft Dynamics AX にアクセスする方法にも基づいています。 ユーザーは、ネームド ユーザーとして、またはライセンスされたデバイスを介して Microsoft Dynamics AX にアクセスできます。

## <a name="prerequisites"></a>必要条件
None

## <a name="getting-started"></a>はじめに
ライセンス数見積もりツールを使用するには、データを入力し、レポートを生成します。 **重要:** このツールは、各ユーザーが単一のロールを実行すると想定しています。 複数のロールに同じ担当者を入力すると、その人は、レポート上独立した複数のユーザーとしてカウントされるようになります。 たとえば、3 つのロールを持つユーザーは、3 つのユーザーとして見なされます。

### <a name="enter-data"></a>データの入力

1.  [Lifecycle Services に移動](https://lcs.dynamics.com).
2.  プロジェクトで、**ライセンス数見積もりツール**をクリックします。
3.  **編集の概要**ページで、従業員と仕入先ユーザーの番号に関する情報を入力し、新規または既存の実装の見積を作成するかどうかを選択します。
4.  追加する部門を選択するには、**部門の追加**をクリックします。
5.  **ライセンス数見積もりツール**ページで、顧客組織のロールに関する詳細を入力します。 **注記:** **ライセンス数見積もりツール**ページは、パノラマ ページです。 このページのすべての情報を表示するには、マウス ホイールまたはブラウザーの下のスクロールバーを使用して右にスクロールします。

### <a name="generate-a-report"></a>レポートの生成

**ライセンス数見積もりツール**ページで、**レポートの生成**をクリックします。 レポートでは、入力したデータが要約され、見積済ライセンス情報が表形式と円グラフ形式で表示されます。



