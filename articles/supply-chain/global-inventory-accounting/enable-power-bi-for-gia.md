---
title: グローバル在庫会計の Power BI を有効にする
description: このトピックでは、グローバル在庫会計の Microsoft Power BI を有効にする方法について説明します。
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d7979ed18b98ee6133774cd91bc866d6fca92d5f
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273185"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a>グローバル在庫会計の Power BI を有効にする

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

[PowerBI.com](https://powerbi.com/) アカウントから Microsoft Dynamics 365 アプリケーション ワークスペースにタイル、ダッシュ ボード、およびレポートをピン留めすることができます。

## <a name="prerequisites"></a>必要条件

Power BI レポートを有効にするには、次の前提条件が満たされている必要があります。

- Dynamics 365 アプリケーションのシステム管理者である必要があります。
- [PowerBI.com](https://powerbi.com/) アカウントが必要です。
- 自分の Power BI アカウントに、少なくとも 1 つのダッシュボードと 1 つのレポートがあることが必要です。
- Azure Active Directory (Azure AD) アカウントの管理者である必要があります。
- Azure AD ドメインは、自分の [PowerBI.com](https://powerbi.com/) アカウントに使用したドメインと同じである必要があります。

## <a name="setup"></a>段取り

Power BI 統合を設定するには、次の手順に従います。

1. [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) にログインします。
1. **共用資産ライブラリ** に移動し、資産タイプとして **Power BI レポート モデル** を選択し、**グローバル在庫会計** パッケージをダウンロードします。 
1. [PowerBI.com](https://app.powerbi.com/) にログインして、次の手順に従って **グローバル在庫会計** Power BI レポート ファイルをアップロードします。

    1. **新規** を選択します。
    1. **ファイルをアップロードする** を選択します。
    1. **グローバル在庫会計** Power BI レポート ファイルを選択します。

1. 次の手順に従って **グローバル在庫会計** Power BI レポートを構成します。

    1. **マイ ワークスペース** に移動し、グローバル在庫会計のデータセットを検索してから **オプション** メニューで **設定** を選択します。
    1. **グローバル在庫会計の設定** で、**パラメーター** を展開し、必要に応じてすべてのパラメーターを更新します。

1. [PowerBI.com 統合のコンフィギュレーション](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process) で説明されているようにアプリケーションを登録します。
1. 次の手順に従って、**グローバル在庫会計** Power BI レポート ファイルを Dynamics 365 Supply Chain Management に統合します。

    1. **システム管理 \> 設定 \> PowerBI.com コンフィギュレーション** の順にクリックします。
    1. **編集** を選択します。
    1. **PowerBI.com 統合を有効にする** を選択します。
    1. **アプリケーション ID** フィールドに、アプリケーション ID を入力します。
    1. **アプリケーション キー** フィールドに、アプリケーション キーを入力します。
    1. **保存** を選択します。

1. ページを更新すると、Power BI サインイン ダイアログ ボックスが表示されます。
1. **オプション** タブで、**レポート カタログを開く** を選択し、先ほどアップロードした **グローバル在庫会計** Power BI レポート ファイルを選択します。
1. ページを更新します。 追加されたレポートが表示されます。
1. **Power BI レポート** の下で、**グローバル在庫会計** リンクを選択します。

詳細については、[PowerBI.com 統合のコンフィギュレーション](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md) を参照してください。
