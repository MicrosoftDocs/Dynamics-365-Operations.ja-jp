---
title: 電子メール通知プロファイルの設定
description: このトピックでは、Microsoft Dynamics 365 Commerce で電子メール通知プロファイルを作成する方法について説明します。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9e5d90eaf1815bbe54b0bea40d92a0a993a23b75
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113808"
---
# <a name="set-up-an-email-notification-profile"></a>電子メール通知プロファイルの設定


[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce で電子メール通知プロファイルを作成する方法について説明します。

## <a name="overview"></a>概要

チャネルを作成する前に、プロファイルを設定して、発注書の作成、注文出荷の状態、支払不履行など、さまざまなイベントに対して電子メール通知を送信できるようにします。

追加の電子メールのコンフィギュレーションに関する詳細については、[電子メールのコンフィギュレーションおよび送信](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json) を参照してください。

## <a name="create-an-email-notification-profile"></a>電子メール通知プロファイルの作成

電子メール通知プロファイルを作成するには、次の手順を実行します。

1. ナビゲーション ウィンドウで、**モジュール \> 小売りとコマース \> 本社の設定 \> コマース電子メール通知プロファイル**に移動します。
1. アクション ウィンドウで、**新規**をクリックします。
1. **電子メール通知プロファイル** フィールドに、プロファイルを識別する名前を入力します。
1. **説明**フィールドに関連する説明を入力します。
1. **有効な**スイッチを**はい**に設定します。

### <a name="create-an-email-template"></a>電子メール テンプレートを作成する

電子メール通知を作成する前に、送信者の電子メール情報および電子メール テンプレートを含む組織の電子メール テンプレートを作成する必要があります。

電子メール テンプレートを作成するには、次の手順に従います。

1. ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> 本社の設定 \> パラメーター \> 組織の電子メール テンプレート**に移動します。
1. アクション ウィンドウで、**新規**を選択します。
1. **電子メール ID** フィールドに、このテンプレートを識別するための ID を入力します。
1. **送信者名**フィールドに、送信者の名前を入力します。
1. **電子メールの説明**フィールドに、意味のある名前を入力します。
1. **送信電子メール** フィールドに、送信者の電子メール アドレスを入力します。
1. **一般**セクションで、必要なオプション情報すべて (電子メールの優先順位など) を入力します。
1. 電子**メール メッセージのコンテンツ** セクションを**展開**し、新規を選択して、テンプレート コンテンツを作成します。 各コンテンツ項目について、言語を選択し、電子メールの件名行を入力します。 電子メールに本文が含まれる場合、**本文**ボックスがオンになっていることを確認します。
1. アクション ウィンドウで、電子メール**本文テンプレート**を提供する電子メール メッセージを選択します。

次の画像は、電子メール テンプレートの設定例を示しています。

![電子メール テンプレート設定](media/email-template.png)

### <a name="create-an-email-event"></a>電子メール イベントの作成

電子メール イベントを作成するには、次の手順に従います。

1. ナビゲーション ウィンドウで、**モジュール \> 小売りとコマース \> 本社の設定 \> コマース電子メール通知プロファイル**に移動します。
1. 一覧で、目的のレコードを見つけ、選択します。 
1. **電子メール ID** ドロップダウン リストから電子メール テンプレートを選択します。
1. ドロップダウン リストから適切な**電子メール通知タイプ**を選択します。
1. **有効**チェック ボックスをオンにします。
1. アクション ウィンドウで、**保存**を選択します。

次の画像は、イベント通知の設定例を示しています。

![イベント通知設定](media/email-notification-profile.png)

## <a name="additional-resources"></a>追加リソース

[電子メールのコンフィギュレーションと送信](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[チャネルの概要](channels-overview.md)

[チャネル設定の前提条件](channels-prerequisites.md)

[組織と組織階層の概要](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
