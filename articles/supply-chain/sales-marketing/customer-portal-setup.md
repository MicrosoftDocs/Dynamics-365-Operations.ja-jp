---
title: 顧客ポータルのインストール、設定、更新
description: このトピックでは、顧客ポータルのライセンスの詳細と設定手順を説明します。
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 2153bbca2be7c72e48b9dc51b1f7fdbe2ab89903
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977741"
---
# <a name="install-set-up-and-update-the-customer-portal"></a>顧客ポータルのインストール、設定、更新

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a>ライセンス要件

顧客ポータルの実装には、次のライセンスを所有している必要があります :

- **Power Apps ポータル** - このライセンスは、顧客ポータルのホストに必要です。 ポータルは、使用率に基づいてライセンス供与されます。 詳細については、[Power Apps ポータルのライセンス要件](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals) を参照してください。
- **デュアル書き込み** - Supply Chain Management のテーブルにデュアル書き込みを有効にするには、必要なライセンスを所有している必要があります。 詳細については、[デュアル書き込みのシステム要件](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md) を参照してください。

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a>デュアル書き込みと、Power Apps ポータルの依存関係

顧客ポータルは、次の図に示すように、Power Apps ポータルとデュアル書き込みと依存関係があります。

![顧客ポータルの依存関係](media/customer-portal-elements.png "顧客ポータルの依存関係")

Supply Chain Management の他の機能とは異なり、顧客ポータルのテンプレートは Power Apps ポータルに存在します。 したがって、顧客ポータルは、Power Apps ポータルやデュアル書き込みのテーブルが提供する機能や能力によって制限されます。

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a>顧客ポータルを有効化する設定が必要です

必要なライセンスを確認した後は、デュアル書き込みを設定し、[デュアル書き込みの初回同期](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md)に記載の指示に従って設定することができます。

デュアル書き込みでは、以下のテーブル マッピングを有効化してください:

- 販売注文ヘッダー
- 販売注文の詳細
- アカウント
- 連絡先
- 製品

この設定の完了後、顧客ポータル テンプレートを準備できます。

## <a name="provision-the-customer-portal"></a>顧客のポータルを準備する

開始する前に、[必要な設定](#required-setup)が完了していることを確認してください。 続いて、以下の手順に従って顧客ポータルを準備します。

1. [make.powerapps.com](https://make.powerapps.com/) に移動します。
2. デュアル書き込みを有効化した環境を使用していることを確認します。
3. **作成** タブで、**テンプレートから開始する** セクションにスクロールダウンして、**顧客ポータル** という名前のテンプレートを選択します。
4. 画面に表示される指示に従ってください。

プロビジョニングが完了したら、**ホーム** ページの **自分のアプリ** セクションで顧客ポータルにアクセスできます。

> [!NOTE]
> デュアル書き込みソリューションが、作業をする環境にインストールされていない場合は、エラーメッセージが表示され、顧客ポータルを準備することはできません。

## <a name="update-the-customer-portal"></a>顧客のポータルを更新する

後から顧客ポータルにその他機能を追加する場合があります。 基となるソリューション コンポーネントに行われた変更は、自動的に環境に反映されます。 ただし、環境内で準備された Webサイトに対しては、構成データに加えられた変更は自動的に反映されません。 新しいテンプレートからコードを取得し、それをプロビジョニングされた Web サイトにマージすることで、これらの変更を手動で適用する必要があります。

## <a name="additional-resources"></a>追加リソース

顧客ポータルを設定してカスタマイズする方法の詳細については、次のドキュメントを参照して基礎となるテクノロジーについて確認してください :

- [Power Apps ポータル ドキュメント](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [デュアル書き込みのドキュメント](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

ポータルを効果的に管理するには、Power Appsポータルと Microsoft Dataverse のライフサイクルを理解しておく必要があります。 詳細については、次のリソースを参照してください :

- [ポータルのライフ サイクルについて](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [ポータルのアップグレード](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [ポータルの構成の移行](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [ソリューションのライフサイクル管理 : Dynamics 365 for Customer Engagement アプリ](https://www.microsoft.com/download/details.aspx?id=57777)
