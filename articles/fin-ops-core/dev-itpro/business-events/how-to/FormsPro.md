---
title: ビジネス イベントおよび Microsoft Forms Pro
description: この記事では、製品の出荷時に調査がユーザーに送信されるシナリオについて説明します。
author: murrayfife
ms.date: 08/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global for most topics. Set Country/Region name for localizations
ms.author: mufife
ms.search.validFrom: Platform update 27
ms.dyn365.ops.version: 2019-6-30
ms.openlocfilehash: adc729f4726bf1529f554fd1e641a9c801920aed
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906561"
---
# <a name="business-events-and-microsoft-forms-pro"></a>ビジネス イベントおよび Microsoft Forms Pro

[!include[banner](../../includes/banner.md)]

この記事では、Microsoft Forms Pro を使用してビジネス イベントで使用できる調査を作成するシナリオを説明します。 特にここで説明するシナリオでは製品が出荷されたときに調査が顧客に送信されます。 調査情報は Forms Pro を使用して収集されます。

## <a name="prerequisites"></a>必要条件

Forms Pro を使用したことがない場合は、まず [Forms Pro のドキュメント](/forms-pro/) を読んで使用方法を学習します。

## <a name="scenario"></a>シナリオ

1. 調査の作成 調査に入力したタイトルに基づいて Forms Pro はアンケートの質問を提案します。

    ![Forms Pro で推奨される調査の質問。](../../media/Forms_Pro1.png)

2. 販売注文は出荷を追跡します。 製品が出荷されると、販売注文のステータスが **配送済** に変更されます。

    ![ステータスが配送済となっている販売注文。](../../media/SalesOrder1.png)

    そのため、**ステータス** フィールドの値が変更されるたびにアラートを作成するように、販売注文でアラートを構成します。 アラートがビジネス イベントとして送信されるように、必ず **外部に送信** オプションを **はい** に設定してください。

    ![警告。](../../media/Alerts1.png)

3. 販売注文のステータスが更新されるたびにビジネス イベントにトリガーされるフローを設定します (次のステップの図を参照してください)。 トリガーされた後、フローはフォーム コネクタを使用して、販売注文に登録されている顧客の電子メール アドレスに調査を送信します。

    シナリオに必要な顧客の電子メール アドレスとその他の情報は、ビジネス イベント ペイロードに含まれる必要があります。 ペイロードにこのデータがない場合は、適切なフィールドが含まれるように拡張できます。 詳細については [ビジネス イベント開発者ドキュメント](../business-events-dev-doc.md) を参照してください。

4. このシナリオの調整には Microsoft Power Automate が使用されるため、アプリケーションで **変更ベースのアラートが発生した場合** ビジネス イベントを有効化しないでください。 代わりに、ビジネス イベントを直接サブスクライブするように Power Automate を設定します。

    ![フロー。](../../media/Flow1.png)

5. フローは設定が完了するとトリガーされ、販売注文のステータスが更新されるたびに調査が送信されます。

    ![調査。](../../media/Survey1.png)

    ユーザーが調査に入力して送信すると Forms Pro に分析が表示されます。

    ![Forms Pro の調査分析。](../../media/Forms_Pro2.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
