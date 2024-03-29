---
title: 電子メールによるクライアント警告通知
description: この記事では、定義済のイベントが発生する電子メール通知を送信するルールを設定する方法について説明します。
author: RichdiMSFT
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 469c7fdda40780d6e559819103d73d7a4e7132a1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878281"
---
# <a name="client-alert-notifications-by-email"></a>電子メールによるクライアント警告通知

[!include [banner](../includes/banner.md)]

データのフィルター処理されたビューを監視し、定義済のイベントが発生した場合に、電子メール通知を自動的に送信するカスタム警告ルールを定義できます。 電子メール通知を送信するオプションは、サポートされているすべての警告タイプで使用可能であり、既存の警告ルールでも有効にできます。

組み込みのコントロールを使用して、システム バッチ ジョブのフィルタ処理されたビューを監視する警告ルールを作成できます。 **ステータス** フィールドの値を監視することで、バッチ ジョブが失敗したときに電子メールを送信する警告ルールも設定できます。 これらの警告ルールを作成した後は、ビジネス データへの変更についてレポートを確認する必要はなくなりました。 代わりに、インテリジェントな変更検出サービスに監視させることができます。

クライアントの警告は、Microsoft Office との統合を通じて提供される電子メール サブシステムによって異なります。 電子メールの配信がローカル メール クライアントに依存する必要がないように、Simple Mail Transfer Protocol (SMTP) プロバイダーを使用することをお勧めします。

電子メールで通知を送信するには、顧客が統合電子メール サービスをコンフィギュレーションする必要があります。 電子メール通知は、警告の所有者に代わって受信者に送信されます。

電子メールをコンフィギュレーションする方法の詳細については、[電子メールのコンフィギュレーションと送信](../organization-administration/configure-email.md)をご覧ください。

次の図は、**電子メールの送信** オプションを含む **警告ルールの作成** ダイアログ ボックスを示しています。

[![ 電子メールの送信オプションがはいに設定されている警告ルールのダイアログ ボックスを作成します。](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> **電子メールの送信** オプションが **はい** に設定されている場合、警告通知はアクション センターから配信され続けます。

## <a name="alert-notification-email-templates"></a>警告通知用電子メール テンプレート

このサービスは、警告通知の基本詳細情報を配信する定義済の電子メール テンプレートを使用して、電子メール通知を送信します。

次の図は、電子メールで受信された時の警告通知の構造を表示します。

[![レコードの作成、フィールドの変更、およびテンプレート削除のためのテンプレートに基づく警告通知。](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]