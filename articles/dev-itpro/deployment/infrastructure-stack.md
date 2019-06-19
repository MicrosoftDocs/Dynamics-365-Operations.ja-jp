---
title: セルフサービス配置
description: このトピックでは、Finance and Operations のセルフ サービス配置の概要を示します。
author: sarvanisathish
manager: AnnBe
ms.date: 12/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: a35b24f06745945009271168a54ed699d22e1be5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544216"
---
# <a name="self-service-deployment"></a>セルフサービス配置

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

Dynamics 365 for Finance and Operationsクラウド環境では、セルフサービス配置が可能です。 セルフ サービス配置により、簡単な配置が可能になり配置時間が大幅に減少します。

> [!IMPORTANT]
> この機能は、Microsoft Azure の国/地域に基づいて段階的にリリースされます。 ただし、この機能は現在、Finance and Operations のサインアップ過程にいる**新しい顧客**のみ利用可能です。 現在の顧客の既存の環境に変更はありません。
>
> すべての新しい顧客にこの機能が表示されるわけではない点に注意してください。 ただし、アクセス権を持つ新しい顧客の数は、徐々に増加します。 

## <a name="whats-new-or-changed"></a>新規または変更

セルフ サービス機能を使用する顧客は、LCS エクスペリエンスにおいて次の変更が見られます。 

- 配置はセルフ サービスであり、平均 30 分以内に完了することができます。 配置のリード タイムや待機時間はなくなります。 いつ配置するかを制御し、環境が展開されていることを確認できます。 このエクスペリエンスは、現在のエクスペリエンスと同じです。 詳細については、[配置に関するよく寄せられる質問](deploymentFAQ.md)を参照してください。

   ![配置設定](media/deployment-settings.png)

- レベル 2 以上のサンドボックス環境へのリモート デスクトップ アクセスがなくなります。 リモート デスクトップ アクセスが必要なすべての操作は、セルフ サービス アクションとして使用可能になりました。 次の図に、環境の **メンテナンス** \> **データベース メニュー オプションの移動** における操作の一部を示します。 詳細については、[配置のメンテナンス操作](maintenanceoperationsguide-newinfrastructure.md)を参照してください。

> [重要] リモート デスクトップ アクセスは、セルフ サービス展開を使用して配置された環境にのみ制限されます。 既存の環境または既存の顧客に変更はありません。 

   ![セルフ サービス アクション](media/Self-service-actions.png)

- 診断機能は、同じままです。リモート デスクトップ アクセスなしでトラブルシューティングが可能になります。 詳細については、[セルフサービス配置で配置された環境のトラブルシューティング](troubleshoot-newinfrastructure.md)を参照してください。 

   ![環境の監視](media/environment-monitoring.png)

- レベル 2 以上では SQL Server アクセスはありません。 Just-In-Time アクセスを使用して SQL データベース アクセスすることは引き続きできます。

- カスタマイズのための結合された配置可能パッケージを提供する必要があります。 つまり、ISV パッケージを含む、すべてのカスタム拡張機能パッケージは、1 つのソフトウェア配置可能パッケージとして配置する必要があります。 一度に 1 つのモジュールを配置することはできません。 これは常に推奨されるベスト プラクティスであり、適用されるようになりました。
