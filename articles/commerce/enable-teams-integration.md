---
title: Dynamics 365 Commerce と Microsoft Teams の統合を有効化する
description: このトピックでは、Microsoft Dynamics 365 Commerce と Microsoft Teams の統合を有効化する方法について説明します。
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c0dbf7a3c7fa3532e35cac240c1abb8adbdbe489
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842696"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>Dynamics 365 Commerce と Microsoft Teams の統合を有効化する

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce と Microsoft Teams の統合を有効化する方法について説明します。

Teams に Dynamics 365 Commerce からの情報を提供し、Teams と 販売時点管理 (POS) のアプリケーション間でタスク管理機能を同期させるには、Commerce 本部で統合機能を有効にする必要があります。

> [!NOTE]
> Teams の 統合を有効にした場合、Teams とデータを共有することに同意することになります。 Teams と共有するデータは、ご利用の Commerce データとは異なる国に存在する可能性があり、また、異なるコンプライアンス基準の対象となる可能性があります。 詳細については、[Microsoft トラストセンター](https://www.microsoft.com/trust-center) を参照してください。 マイクロソフトのプライバシー ポリシーについては、 [Microsoft プライバシー ステートメント](https://aka.ms/privacy)を参照してください。

## <a name="enable-teams-integration"></a>Teams との統合を有効化する

Microsoft Teams と Commerce との統合を有効にする前に、Azure ポータルで Teams アプリケーションをテナントに登録する必要があります。

Azure ポータルで Teams アプリケーションをテナントに登録するには、以下の手順に従います。

1. [クイック スタート : Microsoft IDプラットフォームにアプリを登録する](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) に記載の手順に従い、Azure ポータルで Teams アプリケーションをテナントに登録します。
1. 登録されたアプリケーションの **概要** ページから **アプリケーション (クライアント) ID** 値をコピーします。 この値は、Commerce 本部で Teams を有効にするために使用します。
1. 手順 1 で[証明書を追加](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate)した際に入力した証明書の値をコピーします。 証明書は、公開鍵やアプリケーション キーとも呼ばれます。 この値は、Commerce 本部で Teams を有効にするために使用します。

Commerce 本部で Teams の統合を有効にするには、以下の手順に従います。

1. **Retail と Commerce \> チャネル設定 \> Microsoft Teams 統合の構成** に移動します。
1. アクション ウィンドウで、**編集** を選択します。
1. **有効化 Microsoft Teams 統合** オプションを **はい** に設定します。
1. **アプリケーション ID** と **アプリケーション キー** の各フィールドで、Azure ポータルで Teams アプリケーションを登録した際に取得した値を入力します。
1. アクション ウィンドウで、**保存** を選択します。

次の図は、Commerce 本部での Teams 統合の設定例です。

![Commerce 本部の Teams 統合構成](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a>Teams との統合を無効化する

Commerce 本部で Microsoft Teams の統合を無効にするには、以下の手順に従います。

1. **Retail と Commerce \> チャネル設定 \> Microsoft Teams 統合の構成** に移動します。
1. アクション ウィンドウで、**編集** を選択します。
3. **有効化 Microsoft Teams 統合** オプションを **いいえ** に設定します。
4. **アプリケーションID** フィールドと **アプリケーション キー** フィールドから値をクリアします。
1. アクション ウィンドウで、**保存** を選択します。

> [!NOTE]
> Commerce と Teams の統合を無効にすると、POS 端末には Teams アプリケーションから発行されたタスクが表示されなくなります。

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce と Microsoft Teams データ統合の概要](commerce-teams-integration.md)

[Dynamics 365 Commerce から Microsoft Teams へのプロビジョニング](provision-teams-from-commerce.md)

[Microsoft Teams と Dynamics 365 Commerce の POS 間でタスク管理を同期させる](synchronize-tasks-teams-pos.md)

[Microsoft Teams でユーザーとロールを管理する](manage-user-roles-teams.md)

[Microsoft Teams に既存のチームがある場合は、店舗とチームをマッピングします](map-stores-existing-teams.md)

[Dynamics 365 Commerce と Microsoft Teams の統合に関する FAQ](teams-integration-faq.md)
