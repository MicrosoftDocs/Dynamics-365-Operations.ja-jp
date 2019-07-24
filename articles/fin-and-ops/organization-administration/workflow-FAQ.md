---
title: ワークフローに関するよく寄せられる質問
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のワークフロー システムについてよく寄せられる質問に回答します。
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adcc9bbc422a3fddfd51d248daf95c0da6d4c9bb
ms.sourcegitcommit: 8cf77e9171d6cad8ae6c8bfad9e4f9a46fef6d23
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/19/2019
ms.locfileid: "1689003"
---
# <a name="workflow-faq"></a>ワークフローに関するよく寄せられる質問

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations のワークフロー システムについてよく寄せられる質問に回答します。

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>作業項目が否認された場合に複数の通知が受信されるのはなぜですか。
作業項目が否認されると、その作業項目は否認済として完了します。 別の作業項目が作成され、作成者に割り当てられます。 これは、否認された作業項目に関する発信者への通知と、新しい「変更要求済」の作業項目に割り当てられたユーザーへの個別の通知があることを意味します。 

各通知は異なる作業項目に対するものですが、類似性により混乱が生じる可能性があります。 将来のリリースでこれを改善する方法を検討しています。

## <a name="why-are-my-workflow-exports-failing"></a>ワークフローのエクスポートが失敗するのはなぜですか。
現在、ワークフローのエクスポート機能には、ワークフロー名が 48 文字を超えないようにする制限があります。 48 文字を超える名前を使用すると、「サーバーは要求の認証に失敗しました」というエラーが発生するか、またはファイルがファイル タイプなしでエクスポートされるのを防ぐことができます。 詳細については、次のブログ記事を参照してください [ワークフローのエクスポートに関するトラブルシューティング](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting)。

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>ワークフローの送信者はワークフローを承認することもできますか。
はい、そのように構成されている場合、ワークフローの送信者は、ワークフローを承認することもできます。 この動作を回避するには、**ワークフロー パラメーター > 一般 > 承認者 > 送信者による承認を許可しない**を**はい**に設定します。

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>ユーザーに通知を行うためにワークフローに警告を追加することはできますか?
通知を行うワークフローへの警告の追加に関する注意事項の重要な領域を次に示します。
- 警告とワークフロー通知のメカニズム
    - 警告はレコードの変更に設定することができます。 ワークフローがレコードを変更するので、ワークフローによって発生するレコードの変更に関連付けられた警告を設定することが可能です。 ただし、ワークフローにはさまざまな組み込み通知オプションがあるので、警告を使用することは理想的ではありません。
- ワークフローからの標準通知 
    - ワークフローには電子メール通知が組み込まれています。 顧客は通知を構成できるので、ユーザーに電子メールが送信されます。 それらの通知は、ユーザーに対するアクション センター メッセージにはなりません。
    - 今後の更新で、ユーザーにワークフロー 作業項目が割り当てられるようにアクション センター メッセージを追加します。 
- ワークフローへの通知の追加
    - アクション センター メッセージは、X++ のワークフローから作成されたメッセージのように、特定のユーザーに対して作成されます。
    - [ビジネス イベントのあるワークフロー](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) 顧客は探している通知のあるフローをトリガーがすることができました。   

要約すると、ユーザーがワークフロー作業項目を割り当てられた時、アクション センターから適切な通知を取得できなかった場合、[ワークフロー ビジネス イベント](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) と Microsoft Flow を活用して、追加のまたは異なる通知を行います。
