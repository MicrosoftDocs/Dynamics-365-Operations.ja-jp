---
title: ワークフローに関するよく寄せられる質問
description: このトピックでは、ワークフロー システムについてよく寄せられる質問に回答します。
author: ChrisGarty
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 98d67e240cdd5e64fef1aaf24b4907d1af42056a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567982"
---
# <a name="workflow-faq"></a>ワークフローに関するよく寄せられる質問

[!include [banner](../includes/banner.md)]

このトピックでは、ワークフロー システムについてよく寄せられる質問に回答します。

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>作業項目が否認された場合に複数の通知が受信されるのはなぜですか。
作業項目が否認されると、その作業項目は否認済として完了します。 別の作業項目が作成され、作成者に割り当てられます。 これは、否認された作業項目に関する発信者への通知と、新しい「変更要求済」の作業項目に割り当てられたユーザーへの個別の通知があることを意味します。 

各通知は異なる作業項目に対するものですが、類似性により混乱が生じる可能性があります。 将来のリリースでこれを改善する方法を検討しています。

## <a name="why-are-my-workflow-exports-failing"></a>ワークフローのエクスポートが失敗するのはなぜですか。
現在、ワークフローのエクスポート機能には、ワークフロー名が 48 文字を超えないようにする制限があります。 48 文字を超える名前を使用すると、「サーバーは要求の認証に失敗しました」というエラーが発生するか、またはファイルがファイル タイプなしでエクスポートされるのを防ぐことができます。 詳細については、次のブログ記事を参照してください [ワークフローのエクスポートに関するトラブルシューティング](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting)。

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>ワークフローの送信者はワークフローを承認することもできますか。
はい、そのように構成されている場合、ワークフローの送信者は、ワークフローを承認することもできます。 この動作を回避するには、**システム管理 > ワークフロー > ワークフロー パラメーター > 一般 > 承認者 > 送信者による承認を許可しない** を **はい** に設定します。

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>ユーザーに通知を行うためにワークフローに警告を追加することはできますか?
通知を行うワークフローへの警告の追加に関する注意事項の重要な領域を次に示します。
- 警告とワークフロー通知のメカニズム
    - 警告はレコードの変更に設定することができます。 ワークフローがレコードを変更するので、ワークフローによって発生するレコードの変更に関連付けられた警告を設定することが可能です。 ただし、ワークフローにはさまざまな組み込み通知オプションがあるので、警告を使用することは理想的ではありません。
- ワークフローからの標準通知 
    - ワークフローには電子メール通知が組み込まれています。 顧客は通知を構成できるので、ユーザーに電子メールが送信されます。 それらの通知は、ユーザーに対するアクション センター メッセージにはなりません。
    - 今後の更新で、ユーザーにワークフロー 作業項目が割り当てられるようにアクション センター メッセージを追加します。 
- ワークフローへの通知の追加
    - アクション センター メッセージは、X++ のワークフローから作成されたメッセージのように、特定のユーザーに対して作成されます。
    - 顧客が探している通知を持つフローをトリガーするために使用できる [ビジネス イベントのあるワークフロー](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow)。   

要約すると、ユーザーがワークフロー作業項目を割り当てられた時、アクション センターから適切な通知を取得できなかった場合、[ワークフロー ビジネス イベント](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) と Microsoft Power Automate を活用して、追加のまたは異なる通知を行います。

## <a name="why-is-workflow-editor-not-able-to-start-under-ad-fs"></a>AD FS 下でワークフロー エディターを起動できないのはなぜですか。
アップグレードされた環境で Active Directory フェデレーション サービス (AD FS) を実行している場合、ワークフロー エディターで問題が発生する可能性があります。 その場合、ADFS 設定の **Microsoft Dynamics 365 for Operations オンプレミス - ワークフロー - ネイティブ アプリケーション** プロパティに、URL 「https://dynamicsaxworkfloweditor/」が追加されていることを確認してください。

## <a name="why-am-i-getting-sql-deadlocks-on-workflow-processing"></a>ワークフロー処理で SQL デッドロックが発生するのはなぜですか。 
**ワークフロー パラメーター** ページの **バッチごとのワークフロー項目数** のフィールドの既定値は 0 です。 値が 0 の場合、既定がバッチあたり 20 項目に変更されます。 バッチごとの項目数が大きいと (> 40) SQL デッドロックが発生することがあるため、この値を調整する場合は注意が必要です。

## <a name="what-is-the-workflow-enhanced-error-feature"></a>ワークフロー拡張エラー機能とは ?
Version 10.0.13 のワークフロー拡張エラー機能によって、さまざまなクラスのワークフロー エラーを区別するためのエラー コードが追加されます。 報告されたエラーメッセージは、多くの場合、若干の違いがあるため、わかりやすくすることができます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]