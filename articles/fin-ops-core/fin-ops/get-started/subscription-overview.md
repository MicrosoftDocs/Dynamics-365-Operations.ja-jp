---
title: サブスクリプション、LCS プロジェクト、Azure Active Directory テナントに関するよく寄せられる質問
description: このトピックでは、定期売買およびライセンス、Azure AD テナントおよび LCS 実装プロジェクトに関するよく寄せられる質問に対する回答を提供します。
author: ClaudiaBetz-Haubold
manager: AnnBe
ms.date: 08/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: chaubold
ms.search.validFrom: 2018-05-30
ms.dyn365.ops.version: AX 7.0
ms.openlocfilehash: 2ce9e09e6f9fbca6f0db0f4f2cd0ef121da10197
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798162"
---
# <a name="subscriptions-lcs-projects-and-azure-active-directory-tenants-faq"></a>サブスクリプション、LCS プロジェクト、Azure Active Directory テナントに関するよく寄せられる質問

[!include [banner](../includes/banner.md)]

顧客が Microsoft ボリューム ライセンス契約または Microsoft クラウド ソリューション プロバイダー (CSP) 契約を通じて加入すると、通常、Microsoft Azure Active Directory (Azure AD) テナント、Microsoft Dynamics Lifecycle Services (LCS) 実装プロジェクト、および任意の数のサンドボックス環境とがあります。それらは顧客が選択した 1 つのデータ センターおよび 1 つの実稼働環境に展開されています。 これらのコア概念の詳細については、[Finance and Operations アプリケーション アーキテクチャ](../imp-lifecycle/architecture-overview.md) を参照してください。 この設定は、ほとんどのプロジェクトで適切に動作しますが、さらに高度なシナリオが必要な場合もあります。または、導入ライフサイクル中の変更に対応する必要もあります。

このトピックでは、定期売買およびライセンス、Azure AD テナントおよび LCS 実装プロジェクトに関するよく寄せられる質問に対する回答を提供します。

詳細については、次のトピックを参照してください。

- [データ センター間で環境を移動する](move-environments-data-center.md)
- [契約タイプ間でライセンスを移動する](move-licenses-between-agreement-types.md)
- [LCS 実装プロジェクトを別の Azure AD テナントに移動する](move-lcs-implementation-project-tenant.md)
- [1 つの Azure AD テナントにおける複数の LCS プロジェクトおよび実稼働環境](implement-multiple-projects-aad-tenant.md)

## <a name="do-i-have-to-move-azure-ad-tenants-when-i-move-from-a-csp-agreement-to-a-volume-licensing-agreement"></a>CSP 契約からボリューム ライセンス契約に移行する際、Azure AD テナントを移行する必要がありますか？

一連番号 既存の Azure AD テナントを維持できますが、ボリューム ライセンスのサブスクリプションは CSP サブスクリプションと同じ Azure AD テナントに対して行う必要があります。

## <a name="do-i-get-a-new-lcs-implementation-project-when-i-move-from-a-csp-agreement-to-a-volume-licensing-agreement"></a>CSP 契約からボリューム ライセンス契約に移行した際、新しい LCS 実装プロジェクトを取得しますか？

一連番号 LCS プロジェクトは変わりません。

## <a name="can-i-keep-the-existing-lcs-implementation-project-when-i-move-to-different-azure-ad-tenant"></a>異なる Azure AD テナントに移動する際、既存の LCS 実装プロジェクトを維持することはできますか？

一連番号 新しい LCS プロジェクトが作成されます。

## <a name="how-long-does-it-take-to-move-from-a-csp-agreement-to-a-volume-licensing-agreement"></a>CSP 契約からボリューム ライセンス契約に移行するには、どのくらいの時間がかかりますか？

ボリューム ライセンスの購入では、注文の処理と定期売買の有効化に数日かかることがあります。 アドオン環境の再配置には、2 営業日のサービス レベル契約 (SLA) があります。 古いアドオン環境を割り当て解除し削除するには数時間かかります。

## <a name="what-if-i-forget-to-delete-the-existing-environments-before-i-suspend-the-existing-subscription"></a>既存のサブスクリプションを一時停止する前に既存の環境を削除するのを忘れた場合はどうすればよいですか。

サブスクリプションを中断する前に、既存の環境の割り当てを解除して削除しないと、環境は **配置済み** 状態のままになります。 ただし、これらの環境の全詳細にアクセスしようとすると、エラー メッセージが表示されます。

## <a name="can-i-have-a-csp-agreement-and-a-volume-licensing-agreement-in-parallel"></a>CSP 契約とボリューム ライセンス契約を並行して締結することはできますか？

はい。 ただし、各プログラムで必要なライセンスの最低限の数を維持する必要があります。

## <a name="how-can-i-find-the-tenant-name-and-tenant-id-within-lcs"></a>LCS 内のテナント名とテナント ID をどのように見つけますか?
1. LCS のプロジェクト ホーム ページに移動します。
2. **環境** セクションで、**利用可能なサブスクリプション** を選択します。
3. **利用可能なサブスクリプション** ページで、**テナント名** および **テナント ID** が表示されます。

## <a name="how-can-i-find-the-subscription-status"></a>サブスクリプションのステータスをどのように見つけますか?
1. LCS のプロジェクト ホーム ページに移動します。
2. **環境** セクションで、**利用可能なサブスクリプション** を選択します。
3. **利用可能なサブスクリプション** ページで、テナントへが利用できるすべての **サービス プラン** が表示されます。  
4. **割り当てられた日** は、サービス プランのステータスが変更された日付を示します。 

## <a name="how-would-the-subscription-status-impact-the-environment"></a>サブスクリプション ステータスは環境にどのように影響しますか?
環境の操作の一部は、次のサブスクリプション ステータスにより影響を受ける可能性があります:
- **有効** - サブスクリプションは稼働状態です。 すべての環境操作を実行できます。 
- **支払猶予期間** - サブスクリプションの期限が切れていますが、支払猶予期間内です。 今すぐサブスクリプションを更新する必要があります。 サブスクリプション ステータスは、ライセンス数、新しい環境の展開機能、または環境操作の実行機能には影響しません。
- **中断** - サブスクリプションが支払猶予期間を過ぎて期限切れになりました。 このサブスクリプション ステータスはライセンス数を削減し、新しい環境の展開機能、または環境操作の実行機能に影響を与える場合があります。 
- **削除済** - サブスクリプションは削除されました。 これにより、新しい環境を展開したり環境操作を実行したりする機能に影響を与えます。  

