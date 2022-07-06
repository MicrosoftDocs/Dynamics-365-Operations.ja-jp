---
title: Adyen 向け Dynamics 365 Payment Connector のトラブルシューティング
description: この記事では、Adyen 向け Microsoft Dynamics 365 Payment Connector に関連する一般的な問題に対するトラブルシューティングのガイダンスを提供します。
author: rassadi
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 570ed221fd82d43467f0f2ab3f139edf054f8f5a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893041"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen"></a>Adyen 向け Dynamics 365 Payment Connector のトラブルシューティング

[!include [banner](../includes/banner.md)]

この記事では、Adyen 向け Microsoft Dynamics 365 Payment Connector に関連する一般的な問題に対するトラブルシューティングのガイダンスを提供します。 Adyen 向け Dynamics 365 Payment Connector の概要については [Adyen 向け Dynamics 365 Payment Connector の概要](adyen-connector.md)を参照してください。

## <a name="pos-payment-terminals"></a>POS 支払端末

### <a name="general-issues"></a>一般的な問題

すべての一般的な問題については、Modern POS または IIS ハードウェア ステーション イベント ログを常に参照してください。 以下のログは、Microsoft Windows イベント ログの以下のノードにあります。

- アプリケーションおよびサービス ログ \> Microsoft \> Dynamics \> Commerce-ModernPOS
- アプリケーションおよびサービス ログ \> Microsoft \> Dynamics \> Commerce-Hardware Station

### <a name="failing-payment-transactions"></a>失敗する支払トランザクション

支払取引が Adyen 支払端末を介して適切に処理されないとき、Dynamics 365 POS 内の対応するエラー メッセージには PSP 参照番号 が含まれます (PSP は各取引を一意に識別するために使用される、Adyen が提供する参照 ID です)。 特定の取引について Adyen サポートに連絡するとき、この参照番号を提供します。

### <a name="the-eft-terminal-id-isnt-set"></a>EFT ターミナル ID が設定されていません。

<table>
<tbody>
<tr>
<td><strong>肩書き</strong></td>
<td>EFT ターミナル ID が設定されていません。</td>
</tr>
<tr>
<td><strong>現象</strong></td>
<td>支払承認呼び出しが失敗し、ハードウェア エラーが発生します。 イベント ログ内のエラー メッセージは、<strong>EFT ターミナル ID</strong> 値が設定されていないことを示しています。</td>
</tr>
<tr>
<td><strong>根本原因</strong></td>
<td>この問題は、<strong>EFT POS 登録番号</strong>フィールドが レジスターまたは IIS ハードウェア ステーション上で設定されていないときに発生する場合があります。 また、値が設定されていても、POS 端末に正しく同期されていない場合に発生する場合があります。 さらに、値がキャッシュされるときに発生する場合があります。</td>
</tr>
<td><strong>固定</strong></td>
<td><a href="adyen-connector-setup.md#set-up-a-dynamics-365-register"> Dynamics 365 レジスターの設定</a>にある手順に従ってください。 次に、<strong>1070</strong> および <strong>1090</strong> 配送スケジュールを実行します。 問題が解決されない場合は、<strong>EFT POS 登録番号</strong>フィールドがキャッシュされてリセットする必要がある可能性があるため、Modern POS の再アクティブ化を考慮します。</td>
</tr>
</tbody>
</table>

### <a name="the-modern-pos-or-iis-hardware-station-configuration-isnt-updated"></a>Modern POS または IIS ハードウェア ステーションのコンフィギュレーションが更新されない

<table>
<tbody>
<tr>
<td><strong>タイトル</strong></td>
<td>Config が更新されない</td>
</tr>
<tr>
<td><strong>現象</strong></td>
<td>Modern POS エラー: 「サインイン エラー。 初期化データを読み込むことができませんでした。」</td>
</tr>
<tr>
<td><strong>根本原因</strong></td>
<td>POS が再配置されていても、dllhost.config ファイルが更新されていない場合に、この問題が発生する場合があります。</td>
</tr>
<td><strong>固定</strong></td>
<td><a href="adyen-connector-setup.md#update-the-modern-pos-or-iis-hardware-station-configuration"> Modern POS または IIS ハードウェア ステーションのコンフィギュレーションの更新</a>にある手順に従います。 次に、タスク マネージャーの<strong>詳細</strong>タブで dllhost.exe タスクを終了して、Modern POS を再度開きます。 IIS ハードウェア ステーションを使用している場合は、IIS をリセットします。</td>
</tr>
</tbody>
</table>

### <a name="invoicing-sales-orders-failed-due-to-stale-authorization"></a>古い承認のため、販売注文の請求に失敗

| 肩書き | 古い認証のため、キャプチャに失敗 |
|---|---|
| 現象 | 以下の理由で販売注文の請求に失敗しました。「呼び出しのターゲットによって例外がスローされました。 System.ArgumentException: 値を NULL にすることはできません。」 ログの基になるエラーは次の通りです。「キャプチャ呼び出しの間に次のエラーが発生しました - Adyen 用 Dynamics 365 Payment Connector: 古い認証のため、エラー コードの拒否メッセージのキャプチャに失敗しました。」 |
| 根本原因 | このエラーは、**認証の対象期間 (日数)** よりも古い認証を支払コネクタに送信してキャプチャするときに発生します。 |
| 固定 | **売掛金パラメータ、クレジット カード** の **期限切れから日数** の値が、すべてのチャンネルの販売プロパティで設定されている値よりも **1 日少ない日数** に設定され、請求を再試行することを確認します。 **認証の対象期間 (日数)** の推奨値は、Adyen の販売プロパティで 14、売掛金管理パラメータで 13 になります。 |

## <a name="additional-resources"></a>追加リソース

[Adyen 向け Dynamics 365 Payment Connector の概要](adyen-connector.md)

[Adyen 向け Dynamics 365 Payment Connector の設定](adyen-connector-setup.md)

[Adyen 向け Dynamics 365 Payment Connector に関するよく寄せられる質問](adyen-connector-faq.md)

[支払に関するよく寄せられる質問](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
