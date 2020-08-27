---
title: Lifecycle Services (LCS) のサブスクリプション試算
description: このトピックでは、Lifecycle Services (LCS) で利用可能なサブスクリプション試算ツールを使用する方法について説明します。
author: angelmarshall
manager: AnnBe
ms.date: 08/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform update 12
ms.openlocfilehash: 7f290b543baa783d4bbc9d1371fefb2a7ce14d16
ms.sourcegitcommit: 47d77535aca36b9f98801cb00e5ad2ae1386b3b9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686579"
---
# <a name="subscription-estimator-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) のサブスクリプション試算

[!include [banner](../includes/banner.md)]

サブスクリプション見積もりツールは、Microsoft Dynamics Lifecycle Services (LCS) で使用できるツールです。 Microsoft は、このツールを使用して、顧客に対して準備する必要がある実稼働環境の初期サイズを見積ります。 顧客が実稼働環境の配置を要求する前に、トランザクション カウントの観点からピーク作業負荷を見積もり、その情報を LCS にアップロードする必要があります。 ユーザー ライセンスの詳細およびトランザクション カウントを使用してサブスクリプション要件を推測することにより、サブスクリプション見積もりツールは、プロビジョニングされた環境が顧客の業務要件を満たしていることを確認できます。

サブスクリプション試算ツールを使用するには、これらの手順に従います。

1. LCS で、実装プロジェクトに関連付けられているプロジェクトを開きます。
2. ページの上部にあるハンバーガー アイコン選択し、**サブスクリプション見積もりツール**を選択します。

    [![サブスクリプション見積もりツール](./media/subscription_estimator_01.png)](./media/subscription_estimator_01.png)

3. サンプルの使用状況プロファイルをダウンロードします。
4. 各タブで必要な質問に回答します。Commerce の顧客の場合は、**Retail と Commerce** タブ上の質問に回答してください。
5. 使用状況プロファイルをローカルに保存します。
6. 使用プロファイルをアップロードするには、**新しい見積もり** を選択し、見積もりに名前を付け、使用プロファイルをアップロードします。
7. アップロードが完了した後、**アクティブとしてマークする**を選択し見積もりを有効にします。 生産の配置をコンフィギュレーションするために有効な見積が必要です。

有効でアクティブな見積があるときは、**構成** ボタンが使用できるようになります。 このボタンを使用すると、製造環境の展開を要求することができます。

> [!NOTE]
> 複数の見積を使用できますが、1 つの見積に**アクティブ**とマークする必要があります。 実稼動環境が配置された後、または環境の配置がサインオフされた後、アクティブな見積もりはロックされます。 別の見積もりを有効見積もりとしてマークするには、LCS のサポート ポータルを使用してサポート要求を作成します。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**質問:** アクティブな見積もりがあるにもかかわらず、実稼動環境の**コンフィギュレーション**ボタンが有効なのはなぜですか。 また、プロジェクト ダッシュ ボード上のアクション センターに警告メッセージが表示されるのはなぜでしょうか。

**回答:** 複数の実装プロジェクトがある場合、**コンフィギュレーション**ボタンを有効にされていない可能性があり、アクション センターに不足しているライセンス数に関する警告メッセージが表示されます。 サポート リクエストを記録すると、サポート チームがこの問題を解決できます。

**質問:** 見積もりに**有効**とマークするとエラーが発生するのはなぜですか。

**回答:** 見積を**有効**とマークすると、次のエラー メッセージが表示されることがあります。

- **見積が作成されますが、要件を満たしていません** - このエラーは、入力されたトランザクション明細行がサブスクリプション見積もりツールの制限内にない場合に発生します。 このエラーを解決するには、サポート要求を作成し、使用プロファイルを添付します。 次に、インスタンスのサイズを手動で変更できます。

その他のエラー メッセージが表示されたり、その他の問題が発生した場合は、サポート チームがその問題に対処できるようにサポート リクエストを作成し、アクティブな見積もりを添付します。
 
 ## <a name="additional-resources"></a>追加リソース
 [サブスクリプション、LCS プロジェクト、および Azure Active Directory テナントに関するよく寄せられる質問](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/subscription-overview)
