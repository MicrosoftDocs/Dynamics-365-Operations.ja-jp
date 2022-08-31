---
title: 独立系ソフトウェア ベンダーのライセンス ステータスの表示
description: この記事では、財務と運用アプリで独立系ソフトウェア ベンダーのステータスを表示する方法について説明します。
author: Peakerbl
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 3544e62ff9d8e673ddd7de31ae9ba2872befb42e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287868"
---
# <a name="view-independent-software-vendor-license-status"></a>独立系ソフトウェア ベンダーのライセンス ステータスの表示

[!include [banner](../includes/banner.md)]


この記事では、Dynamics 365 Finance、Dynamics 365 Supply Chain Management、および Dynamics 365 Commerce などの財務と運用アプリの独立系ソフトウェア ベンダー (ISV) ライセンスのステータスを表示する方法について説明します。

ライセンス コードとコンフィギュレーション キーは、財務と運用アプリの ISV ライセンス モデルの一部です。

> [!NOTE]
> Microsoft が提供するコンフィギュレーション キーは、財務と運用アプリのライセンス モデルの一部ではありません。 キーは、機能を有効または無効にするためにのみ使用されます。

ISV のライセンス キーとコードがインストールされると、対応するコンフィギュレーション キーは、**ライセンス コンフィギュレーション** ページで使用可能になり、有効になります。

## <a name="view-isv-license-status"></a>ISV ライセンス ステータスの表示
ライセンスに関連付けられた各 ISV ソリューションは、有効なライセンス コードが顧客の環境に存在する場合にのみ実行されます。 したがって、ISV がソリューションをライセンスに結び付けても、顧客に有効なライセンス コードがない場合、ソリューションは実行されません。 機能が失われるのを防ぐには、ライセンス コードの有効期限 (該当する場合) を追跡することが重要です。 有効期限を表示するには、**システム管理** > **設定** > **ライセンス コンフィギュレーション** に移動し、**ライセンス コード** のタブを選択します。

ダウンタイムを回避するには、ライセンス キーの有効期限を確認し、該当する場合は、新しいバージョンに移行する前に新しいライセンス キーを取得してインポートします。
**ライセンス コード** のタブには、期限切れのライセンス コードが表示されます。 対応するコンフィギュレーション キーは、**コンフィギュレーション キー** のタブには表示されません。


## <a name="additional-resources"></a>追加リソース
ISV ライセンス機能の詳細については、[独立系ソフトウェア ベンダー (ISV) ライセンス](../dev-tools/isv-licensing.md)を参照してください。

ISV ライセンスを環境内の配置にインポートする方法の詳細については、[独立系ソフトウェア ベンダー (ISV) ライセンス (オンプレミス)](../dev-tools/isv-licensing-on-prem.md) を参照してください。

コンフィギュレーション キーレポートの詳細については、[ライセンス コードとコンフィギュレーション キーのレポート](license-codes-configuration-keys-report.md)を参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

