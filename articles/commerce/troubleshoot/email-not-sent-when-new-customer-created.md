---
title: 新規顧客の作成時にようこそメールが送信されない
description: この記事では、Microsoft Dynamics 365 Commerce で新規顧客が作成された時に、ようこそメール通知が送信されない場合に役立つトラブルシューティング ガイドを提供します。
author: gvrmohanreddy
ms.date: 08/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 5aa7d864555f96194500989e2d7ad200d8892121
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219407"
---
# <a name="welcome-email-isnt-sent-when-new-customers-are-created"></a>新規顧客の作成時にようこそメールが送信されない

[!include [banner](../../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce で新規顧客が作成された時に、ようこそメール通知が送信されない場合に役立つトラブルシューティング ガイドを提供します。

## <a name="description"></a>Description

Commerce 本部で新規顧客が作成された時に、**顧客が作成した** メール通知のタイプに電子メール通知が構成されていたとしても、ようこそメールが顧客に送信されません。

## <a name="resolution"></a>解決策

### <a name="associate-an-email-notification-profile-under-commerce-parameters"></a>Commerce パラメーターでの電子メール通知プロファイルの関連付け

1. Headquarters で、**小売とコマース \> 本社の設定 \> パラメーター \> コマース パラメーター \> 全般** に移動します。
2. **電子メール通知プロファイル** ドロップダウン リストで、顧客作成の通知タイプと顧客作成の電子メール テンプレートとのマッピングを含む電子メール通知プロファイルを選択します。  

> [!NOTE] 
> 顧客作成通知を有効にすると、法人内のすべてのチャネルで作成された顧客は、顧客作成メールを受け取ります。 現在、顧客作成通知を 1 つのチャネルに制限することはできません。

詳細については、[トランザクション イベント用の電子メール テンプレートの作成](../email-templates-transactions.md)を参照してください。 

## <a name="additional-resources"></a>追加リソース

[電子メール通知プロファイルの設定](../email-notification-profiles.md)
