---
title: 電子メール通知プロファイルの設定
description: このトピックでは、Microsoft Dynamics 365 Commerce で電子メール通知プロファイルを作成する方法について説明します。
author: bicyclingfool
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7504b2b36f6869f90de196bf32c09e7bdd51e7b5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792660"
---
# <a name="set-up-an-email-notification-profile"></a>電子メール通知プロファイルの設定

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce で電子メール通知プロファイルを作成する方法について説明します。

チャンネルを作成する場合は、電子メール通知プロファイルを設定できます。 このようにして、発注書の作成、注文出荷の状態、支払不履行など、さまざまなトランザクション イベントについて顧客に電子メールを送信できます。

追加の電子メールのコンフィギュレーションに関する詳細については、[電子メールのコンフィギュレーションおよび送信](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json) を参照してください。

## <a name="create-an-email-notification-profile"></a>電子メール通知プロファイルの作成

電子メール通知プロファイルを作成するには、次の手順を実行します。

1. ナビゲーション ウィンドウで、**モジュール \> 小売りとコマース \> 本社の設定 \> コマース電子メール通知プロファイル** に移動します。
1. アクション ウィンドウで、**新規** をクリックします。
1. **電子メール通知プロファイル** フィールドに、プロファイルを識別する名前を入力します。
1. **説明** フィールドに関連する説明を入力します。
1. **有効な** スイッチを **はい** に設定します。

### <a name="create-an-email-template"></a>電子メール テンプレートを作成する

電子メール通知タイプを有効にする前に、Commerce 本社で組織の電子メール テンプレートを作成する必要があります。 このテンプレートでは、サポートする各言語の電子メールの件名、送信者、既定の言語、および電子メールの本文を定義します。

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

![電子メール テンプレート設定](media/email-template.png)

### <a name="create-an-email-event"></a>電子メール イベントの作成

電子メール イベントを作成するには、次の手順に従います。

1. ナビゲーション ウィンドウで、**モジュール \> 小売りとコマース \> 本社の設定 \> コマース電子メール通知プロファイル** に移動します。
1. 一覧で、目的のレコードを見つけ、選択します。 
1. **電子メール ID** ドロップダウン リストから電子メール テンプレートを選択します。
1. ドロップダウン リストから適切な **電子メール通知タイプ** を選択します。
1. **有効** チェック ボックスをオンにします。
1. アクション ウィンドウで、**保存** を選択します。

次の画像は、イベント通知の設定例を示しています。

![イベント通知設定](media/email-notification-profile.png)

### <a name="next-steps"></a>次のステップ

メールを送信する前に、送信メール サービスをコンフィギュレーションし、バッチ ジョブを設定する必要があります。 詳細については、[電子メールのコンフィギュレーションと送信](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json) を参照してください。


## <a name="additional-resources"></a>追加リソース

[電子メールのコンフィギュレーションと送信](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[チャネルの概要](channels-overview.md)

[チャネル設定の前提条件](channels-prerequisites.md)

[組織と組織階層の概要](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
