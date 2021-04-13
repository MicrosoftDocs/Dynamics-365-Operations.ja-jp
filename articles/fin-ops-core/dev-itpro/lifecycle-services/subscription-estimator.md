---
title: Lifecycle Services (LCS) のサブスクリプション試算
description: このトピックでは、Lifecycle Services (LCS) で利用可能なサブスクリプション試算ツールを使用する方法について説明します。
author: angelmarshall
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform update 12
ms.openlocfilehash: 28761664196d325689d11eb30efa019691b0056a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752264"
---
# <a name="subscription-estimator-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) のサブスクリプション試算

[!include [banner](../includes/banner.md)]

サブスクリプション見積もりツールは、Microsoft Dynamics Lifecycle Services (LCS) で使用できるツールです。 Microsoft は、このツールを使用して、顧客に対して準備する必要がある実稼働環境の初期サイズを見積ります。 顧客が実稼働環境の配置を要求する前に、トランザクション カウントの観点からピーク作業負荷を見積もり、その情報を LCS にアップロードする必要があります。 ユーザー ライセンスの詳細およびトランザクション カウントを使用してサブスクリプション要件を推測することにより、サブスクリプション見積もりツールは、プロビジョニングされた環境が顧客の業務要件を満たしていることを確認できます。

サブスクリプション試算ツールを使用するには、これらの手順に従います。

1. LCS で、実装プロジェクトに関連付けられているプロジェクトを開きます。
2. ページの上部にあるハンバーガー アイコン選択し、**サブスクリプション見積もりツール** を選択します。

    [![サブスクリプション見積もりツール](./media/subscription_estimator_01.png)](./media/subscription_estimator_01.png)

3. サンプルの使用状況プロファイルをダウンロードします。
4. 各タブで必要な質問に回答します。Commerce の顧客の場合は、**Retail と Commerce** タブ上の質問に回答してください。
5. 使用状況プロファイルをローカルに保存します。
6. 使用プロファイルをアップロードするには、**新しい見積もり** を選択し、見積もりに名前を付け、使用プロファイルをアップロードします。
7. アップロードが完了した後、**アクティブとしてマークする** を選択し見積もりを有効にします。 生産の配置をコンフィギュレーションするために有効な見積が必要です。

有効でアクティブな見積があるときは、**構成** ボタンが使用できるようになります。 このボタンを使用すると、製造環境の展開を要求することができます。

> [!NOTE]
> 複数の見積を使用できますが、1 つの見積に **アクティブ** とマークする必要があります。 実稼動環境が配置された後、または環境の配置がサインオフされた後、アクティブな見積もりはロックされます。 別の見積もりを有効見積もりとしてマークするには、LCS のサポート ポータルを使用してサポート要求を作成します。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="why-isnt-the-configure-button-for-deploying-a-production-environment-available-even-though-there-is-an-active-estimate-and-why-does-a-warning-message-appear-in-the-action-center-on-the-project-dashboard"></a>アクティブな見積があるにもかかわらず、実稼動環境の **コンフィギュレーション** ボタンが有効なのはなぜですか? また、プロジェクト ダッシュ ボード上のアクション センターに警告メッセージが表示されるのはなぜでしょうか?

複数の実装プロジェクトがある場合、**コンフィギュレーション** ボタンを有効にされていない可能性があり、アクション センターに不足しているライセンス数に関する警告メッセージが表示されます。 サポート リクエストを記録すると、サポート チームがこの問題を解決できます。

### <a name="why-does-an-error-occur-when-i-mark-an-estimate-as-active"></a>見積に **有効** とマークするとエラーが発生するのはなぜですか?

見積を **有効** とマークすると、次のエラー メッセージが表示されることがあります。

*見積が作成されましたが、要件を満たしていません*

このエラーは、入力されたトランザクション明細行がサブスクリプション見積ツールの制限内にない場合に発生します。 このエラーを解決するには、サポート要求を作成し、使用プロファイルを添付します。 次に、インスタンスのサイズを手動で変更できます。

### <a name="how-can-i-update-my-subscription-if-my-production-environment-is-deployed"></a>実稼動環境が配置されている場合、どのようにサブスクリプションを更新ことができますか?

[サブスクリプション見積](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/subscription-estimator) は、実働の要求をする前に必要なステップです。 複数の見積を使用できますが、1 つは **アクティブ** とマークする必要があります。 有効なサブスクリプション見積を使用して、実稼働環境のサイズを変更することができます。 実稼動環境が配置された後、または環境の配置がサインオフされた後、アクティブな見積もりはロックされます。 別の見積もりを有効見積もりとしてマークするには、LCS のサポート ポータルを使用してサポート要求を作成します。 プロジェクトのライセンス量が増加した場合、新しいサブスクリプション見積を作成し、サポート リクエストを記録して、有効としてマークする必要があります。 サイズ変更をする場合、新しいサブスクリプション見積に基づいて適用されることがあります。

### <a name="what-should-i-do-to-activate-my-subscription-estimate-if-i-have-multiple-projects-in-the-same-tenant"></a>同じテナントに複数のプロジェクトがある場合、サブスクリプション見積を有効にするには何をする必要がありますか?

同じテナント内に複数のプロジェクトを実装する場合、LCS のアクション センターに「*サブスクリプションの見積が完了していない*」ことを示す警告が表示されることがあります。 このエラーは、すべての実装プロジェクトの見積ユーザーの数が、購入したライセンスの数を超えないようにする必要があることを示しています。 これは、有効なサブスクリプション見積のユーザーの合計が、同じタイプのテナント ライセンス数を上回っている場合に発生することがあります。 これを修正するには、できるだけ早く Microsoft にサポート リクエストを送信し、ライセンス配賦に関する情報を含め、サブスクリプション見積を修正するよう求める必要があります。 サポート チームにより、見積エディションのプロセスは有効になります。

リクエストを送信する前に、必要なすべてのライセンスが有効にされていることを確認し、実稼働環境のサイズ変更が必要な場合には、ダウンタイムが必要になることがあることに注意してください。

> [!NOTE] 
> FastTrack ソリューション アーキテクトは、サブスクリプション見積のアップロードまたは更新に関与していません。 LCS のサブスクリプション見積に関する警告が特定された場合、上記の指示に従ってください。 問題が継続する場合、Microsoft サポートに問い合わせてください。 

その他のエラー メッセージが表示されたり、その他の問題が発生した場合は、サポート チームがその問題に対処できるようにサポート リクエストを作成し、アクティブな見積を添付します。
 
 ## <a name="additional-resources"></a>追加リソース
 [サブスクリプション、LCS プロジェクト、および Azure Active Directory テナントに関するよく寄せられる質問](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/subscription-overview)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
