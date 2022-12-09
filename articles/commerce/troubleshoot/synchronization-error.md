---
title: 非同期注文の同期の問題
description: この記事では、Microsoft Dynamics 365 Commerce で非同期注文の作成が失敗する一般的な理由について説明し、システム ユーザーおよびパートナーが問題を理解するのに役立つトラブルシューティングの手順を示します。
author: Shajain
ms.date: 11/30/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 27bccced3c07149fe1842524660447a49f86f3fc
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815759"
---
# <a name="asynchronous-order-synchronization-issues"></a>非同期注文の同期の問題

[!include [banner](../../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce で非同期注文の作成が失敗する一般的な理由について説明し、システム ユーザーおよびパートナーが問題を理解するのに役立つトラブルシューティングの手順を示します。

## <a name="symptom"></a>現象

Dynamics 365 Commerce eコマースまたは販売時点管理 (POS) から作成された非同期注文は、Commerce headquarters に反映されません。

## <a name="troubleshooting"></a>トラブルシューティング

注文の作成が headquarters で失敗する理由は、注文作成プロセスが失敗するステージによって異なります。 次のトラブルシューティングの手順では、考えられる根本原因について説明します。

### <a name="validate-that-the-transaction-related-to-the-asynchronous-order-has-reached-headquarters"></a>非同期注文に関連するトランザクションが headquarters に到達したことを検証する

eコマースの注文の場合は、headquarters で **Retail と Commerce \> 照会およびレポート \> オンライン ストアのトランザクション** に移動します。 注文の確認番号がある場合は、**チャンネル参照 ID** フィールドに確認番号を入力してトランザクションをフィルターします。 確認番号がない場合は、顧客アカウント番号を入力してトランザクションをフィルターします。

POS 注文の場合は、**店舗トランザクション** ページを開き、レシート番号または顧客アカウント番号でレコードをフィルターします。 トランザクションが見つからない場合、**P-0001** チャネル トランザクション ジョブを実行し、チャネルから headquarters にトランザクションを同期します。 **P-0001** ジョブが失敗した場合は、ジョブの失敗に対するサポート チケットを開きます。 **P-0001** ジョブが成功してもトランザクションが headquarters に表示されない場合は、関連情報を含むサポート チケットを開きます。
 
### <a name="check-the-synchronization-status-if-the-transaction-is-present-in-headquarters-but-isnt-linked-with-a-sales-order"></a>トランザクションが headquarters にあるが、販売注文とリンクされていない場合、同期ステータスを確認します

トランザクションが headquarters にあるが、販売注文が作成されていない場合は、**オンライン ストアのトランザクション** ページを開き、**同期ステータス** FastTab を選択します。 **注文の同期** ジョブがこのトランザクションを同期しようとした場合、**保留中の注文のステータス** フィールドに **成功** または **失敗** のステータスが表示されます。 ステータスが **成功** の場合、このトランザクションに販売注文フィールドが存在する必要があります。 ステータスが **失敗** の場合は、**同期ステータス** FastTab で **注文エラーの詳細** フィールドにエラーの詳細を表示できます。 いずれのステータスも表示されていない場合、トランザクションの処理が行われていません。 この場合、ページの上部にある **注文の同期** を選択して同期ジョブを実行できます。

**同期注文** ジョブが定期的に実行されるようにスケジュールされていることを確認し、非同期トランザクションを headquarters で注文として作成できるようにします。

以下のセクションでは、一般的なエラーとその修正案を示します。

#### <a name="the-order-error-details-field-shows-the-following-error-message-number-sequence-has-been-exceeded"></a>注文エラーの詳細フィールドに、次のエラー メッセージが表示されます: "番号順序を超えました"

番号順序は、headquarters で販売注文を作成するために使用されます。 番号順序で許可されている番号をすべて使い切った場合、システムはこのエラー メッセージを生成します。 販売注文の作成に使用される番号順序は、**売掛金勘定パラメーター \> 番号順序 \> 販売注文** で確認できます。 このエラーを修正するには、既存の番号順序を修正するか、新しい番号順序に置き換えます。

#### <a name="the-order-error-details-field-shows-the-following-error-message-there-must-be-a-default-payment-service-to-process-credit-card-transactions"></a>注文エラーの詳細フィールドに、次のエラー メッセージが表示されます: "クレジット カード トランザクションを処理するには既定の決済サービスが必要です"

このエラーを修正するには、既定の決済が headquarters で定義されていることを確認します。 既定の決済が定義されていない場合は、定義する必要があります。 **売掛金勘定 \> 決済設定 \> 決済サービス** に移動し、**新しいクレジット カードの既定のプロセッサ** オプションが 1 つの決済サービスに対して **はい** に設定されていることを確認します。
    
#### <a name="the-order-error-details-field-shows-an-account-structure-error-message"></a>注文エラーの詳細フィールドに勘定構造のエラー メッセージが表示される

次の例に示すように、勘定構造のエラー メッセージのテキストは異なる場合があります。 ただし、エラーは勘定構造の構成に関連する一般的な根本原因を共有しています。

- "仕訳帳バッチ番号 0009656328 の転記結果 伝票 ARP-000959899 会社 usrt の伝票 ARP-000959899 に対する 1.00 は、過払いまたは過少支払いとして転記されます"
- "仕訳帳バッチ番号 0009656328 の転記結果 伝票 ARP-000959899 伝票 ARP-000959901 618160 の組み合わせの勘定構造は、元帳の会社の共有主勘定に対して有効ではありません"
- "仕訳帳バッチ番号 0009656328の転記結果 伝票 ARP-000959899 伝票 ARP-000959901 会社コード usrt から報告"
- "仕訳帳バッチ番号 0009656328 の転記結果 伝票 ARP-000959899 の転記はキャンセルされました"
    
これらのエラーを修正するには、勘定構造の正確性を確認します。 詳細については、[勘定構造の構成](/dynamics365/finance/general-ledger/configure-account-structures) を参照してください。
    
エラーを修正した後、失敗したトランザクションを選択し、ページの上部にある **注文の同期** を選択して同期ジョブを実行します。
    
#### <a name="other-types-of-errors-that-might-require-the-transaction-data-to-be-fixed"></a>トランザクション データの修正を必要とする可能性のあるその他のタイプのエラー

トランザクション データの修正を必要とする可能性のあるその他のタイプのエラーを修正するには、"トランザクションの編集と監査" 機能を使用できます。 詳細については、[トランザクションの編集と監査](../edit-order-trans.md) を参照してください。
