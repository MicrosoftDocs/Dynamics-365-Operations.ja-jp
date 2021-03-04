---
title: 独立系ソフトウェア ベンダーのライセンス ステータスの表示
description: このトピックでは、Finance and Operations アプリで独立系ソフトウェア ベンダーのステータスを表示する方法について説明します。
author: Peakerbl
manager: AnnBe
ms.date: 01/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: toskaue
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c7c5e2ac7bf0e6fcd30b68d19b6c144ee79f6081
ms.sourcegitcommit: 7cdec5469ff0da145ac4e01caf3287d0627ae2dc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2021
ms.locfileid: "5100016"
---
# <a name="view-independent-software-vendor-license-status"></a>独立系ソフトウェア ベンダーのライセンス ステータスの表示

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 Finance、Dynamics 365 Supply Chain Management、および Dynamics 365 Commerce などの Finance and Operations アプリの独立系ソフトウェア ベンダー (ISV) ライセンスのステータスを表示する方法について説明します。

ライセンス コードとコンフィギュレーション キーは、Finance and Operations アプリの ISV ライセンス　モデルの一部です。

> [!NOTE]
> Microsoft が提供するコンフィギュレーション キーは、Finance and Operations アプリのライセンス モデルの一部ではありません。 キーは、機能を有効または無効にするためにのみ使用されます。

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