---
title: 電子メール通知プロファイルの設定
description: この記事では、Microsoft Dynamics 365 Commerce で電子メール通知プロファイルを作成する方法について説明します。
author: bicyclingfool
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: db6c46d471e3b54982132df3e4819236833cf4a8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292138"
---
# <a name="set-up-an-email-notification-profile"></a>電子メール通知プロファイルの設定

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce で電子メール通知プロファイルを作成する方法について説明します。

チャンネルを作成する場合は、電子メール通知プロファイルを設定できます。 メール通知プロファイルでは、顧客に通知を送る販売取引のイベント (注文作成、注文確定、注文請求などのイベント) を定義します。 

追加の電子メールのコンフィギュレーションに関する詳細については、[電子メールのコンフィギュレーションおよび送信](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json) を参照してください。



## <a name="create-an-email-template"></a>電子メール テンプレートを作成する

メール通知タイプを有効にする前に、サポートする通知タイプごとに Commerce 本部で組織メール テンプレートを作成する必要があります。 このテンプレートは、サポートされている各言語のメールの件名、送信者、既定の言語、メール本文を定義します。

電子メール テンプレートを作成するには、次の手順に従います。

1. ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> 本社の設定 \> パラメーター \> 組織の電子メール テンプレート** に移動します。
1. アクション ウィンドウで、**新規** を選択します。
1. **電子メール ID** フィールドに、このテンプレートを識別するための ID を入力します。
1. **送信者名** フィールドに、送信者の名前を入力します。
1. **電子メールの説明** フィールドに、意味のある名前を入力します。
1. **送信電子メール** フィールドに、送信者の電子メール アドレスを入力します。
1. **一般** セクションで、電子メール テンプレートの既定の言語を選択します。 既定の言語は、指定された言語にローカライズされたテンプレートが存在しない場合に使用されます。
1. 電子 **メール メッセージのコンテンツ** セクションを **展開** し、新規を選択して、テンプレート コンテンツを作成します。 各コンテンツ項目について、言語を選択し、電子メールの件名行を入力します。 電子メールに本文が含まれる場合、**本文** ボックスがオンになっていることを確認します。
1. アクション ウィンドウで、電子メール **本文テンプレート** を提供する電子メール メッセージを選択します。

次の画像は、電子メール テンプレートの設定例を示しています。

![電子メール テンプレート設定。](media/email-template.png)

メールテンプレートの作成についての詳細について、[トランザクション イベントのメールテンプレートの作成](email-templates-transactions.md) を参照してください。 

## <a name="create-an-email-notification-profile"></a>電子メール通知プロファイルの作成

Headquarters で電子メール通知プロファイルを作成するには、次の手順を実行します。

1. ナビゲーション ウィンドウで、**モジュール \> 小売りとコマース \> 本社の設定 \> コマース電子メール通知プロファイル** に移動します。
1. アクション ウィンドウで、**新規** を選択します。
1. **電子メール通知プロファイル** フィールドに、プロファイルを識別する名前を入力します。
1. **説明** フィールドに関連する説明を入力します。
1. **有効な** スイッチを **はい** に設定します。

## <a name="add-a-notification-type"></a>通知タイプの追加

電子メール イベントを作成するには、次の手順に従います。

1. ナビゲーション ウィンドウで、**モジュール \> 小売りとコマース \> 本社の設定 \> コマース電子メール通知プロファイル** に移動します。
1. **小売用の電子メール通知設定** で、**新規** を選択します。
1. ドロップダウン リストから適切な **電子メール通知タイプ** を選択します。
1. 上で作成した電子メール テンプレートを **メール ID** のドロップダウン リストから選択します。
1. **有効** チェック ボックスをオンにします。
1. アクション ウィンドウで、**保存** を選択します。

次の画像は、イベント通知の設定例を示しています。

![イベント通知設定。](media/email-notification-profile.png)


## <a name="schedule-a-recurring-email-notification-process-job"></a>定期的なメール通知処理のジョブをスケジュールする

電子メール通知を送信するには、**小売注文のメール通知を処理する** ジョブが実行されている必要があります。

トランザクション メールを送信するために headquarters でバッチ ジョブを設定するには、次の手順に従います。

1. **小売とコマース  \> 小売とコマース IT \>メールと通知 \> メール通知の送信** に移動します。
1. **小売注文のメール通知を処理する** ダイアログボックスで、**繰り返し** を選択します。
1. **繰り返しの定義** ダイアログボックスで、**終了日なし** を選択します。
1. **繰り返しパターン** 配下で、**分** を選択し、**カウント** フィールドを **1** に設定します。 これらの設定により、メールの通知ができるだけ早く処理されるようになります。
1. **OK** を選択して、**小売注文のメール通知を処理する** ダイアログボックスに戻ります。
1. ジョブのセットアップを完了するには、**OK** を選択します。

## <a name="next-steps"></a>次のステップ

メールを送信する前に、送信メール サービスを構成する必要があります。 詳細については、[電子メールのコンフィギュレーションと送信](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json) を参照してください。

## <a name="additional-resources"></a>追加リソース

[電子メールのコンフィギュレーションと送信](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[チャネルの概要](channels-overview.md)

[チャネル設定の前提条件](channels-prerequisites.md)

[組織と組織階層の概要](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
