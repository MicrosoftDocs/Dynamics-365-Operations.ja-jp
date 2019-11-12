---
title: Common Data Service 統合のコンフィギュレーション
description: このトピックでは、Microsoft Dynamics 365 Talent と Common Data Service 間の統合を有効または無効にする方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: IT Pro
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-10-08
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: a4209c91042347d00ba538d0336988c34e4dd69a
ms.sourcegitcommit: dd991154231280aff9c9c5799e42799e2bfc02fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622836"
---
# <a name="configure-common-data-service-integration"></a>Common Data Service 統合のコンフィギュレーション

[!include[banner](../includes/banner.md)]

Common Data Service と Microsoft Dynamics 365 Talent のインスタンス間の統合を、有効または無効にすることができます。 また、同期の詳細を表示したり、追跡データをクリアしたり、エンティティを再同期して、2 つの環境間のデータ問題をトラブルシューティングすることもできます。

統合をオフにすると、ユーザーは人材または Common Data Service に変更を加えることができますが、これらの変更は 2 つの環境間で同期されません。

既定では、環境のデモ データの有無に応じて、人材と Common Data Service 間の統合は有効または無効になります。

- デモ データを含まない新しい環境において、**無効**
- デモ データを含む新しい環境において、**有効**

デモ データが含まれる新しい環境では、データの準備時にデータの同期が開始されます。

次のような場合は、統合を無効にすることもできます。

- Data Management Framework を介したデータに入力し正しい状態にするには、データを複数回インポートする必要があります。
- 人材または Common Data Service のいずれかのデータに問題があります。 統合を無効にする場合、他では削除せず、もう一方の環境でレコードを削除することができます。 統合を有効に戻すと、削除されていない環境のレコードは、削除された環境に同期されます。 同期は次に、**同期リクエストを失敗した Common Data Service 統合**バッチ ジョブが実行するときに開始されます。

> [!WARNING]
> データ統合を無効する場合、両方の環境で同じレコードを編集しないようにしてください。 統合を有効に戻すと、最後に編集したレコードが同期されます。 したがって、両方の環境でレコードに同じ変更を加えていない場合は、データが失われる可能性があります。

## <a name="access-the-common-data-service-integration-page"></a>Common Data Service 統合のページにアクセス

1. Common Data Service による統合の設定を表示または構成を希望する人材インスタンスで、**システム管理**のタイルを選択します。

    [![システム管理のタイル](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. **リンク**タブを選択します。

    [![リンク タブ](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. **統合**で、**Common Data Service 統合**を選択します。

    [![Common Data Service コンフィギュレーション リンク](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)

## <a name="turn-data-integration-between-talent-and-common-data-service-on-or-off"></a>人材とCommon Data Service 間でのデータ統合を有効化また無効化

- 統合を有効にするには、**Common Data Service に統合を有効化** オプションを**はい**に設定します。

    > [!NOTE]
    > 統合を有効にすると、データは次に **Common Data Service 統合が要求の同期を逃した**バッチ ジョブが実行する時に同期されます。 バッチ ジョブが完了すると、すべてのデータを使用できるようになります。

- 統合を無効にするには、オプションを**いいえ**に設定します。

[![Common Data Service 統合を有効化または無効化](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)

## <a name="view-data-integration-details"></a>データ統合の詳細を表示

**Common Data Service 統合**ページの**管理**クイックタブで、レコードが人材と Common Data Service 間でどのようにリンクされているか確認できます。

- エンティティのレコードを表示するには、**CDS エンティティ名**フィールドでエンティティを選択します。 グリッドには、選択したエンティティにリンクされているすべてのレコードが表示されます。

[![エンティティのレコードを表示](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)

> [!NOTE]
> すべての Common Data Service エンティティが、現在リストにあるわけではありません。 カスタム フィールドの使用をサポートしているエンティティだけが、グリッドに表示されます。 新しいエンティティは、人材の継続的リリースによって利用可能になります。

グリッドには、次のフィールドが含まれています。

- **CDS エンティティ名** – Common Data Service のエンティティ名。
- **CDS エンティティ参照** – レコードを識別するために Common Data Service を使う識別子。 この値は、人材 **RecId** 値と同じです。 Microsoft Excel で Common Data Service エンティティうぃ開くと、識別子を確認できます。
- **人材エンティティ名** - 最後にデータを Common Data Service に同期したエンティティ。 エンティティは、Common Data Service の接頭語または別の接頭語を持つことが可能です。
- **人材参照** - 人材のレコードに関連付けられる **Recld** 値。
- **CDS から削除されました** - Common Data Service から削除されたレコードかどうか示す値。

## <a name="remove-the-association-of-a-record-in-talent-from-common-data-service"></a>Common Data Service から人材のレコードのアソシエーションを削除

人材と Common Data Service 間のデータ同期中に問題が発生した場合、追跡をクリアにして追跡テーブルを再同期させることで、問題を解決できるかもしれません。 アソシエーションを削除し、Common Data Service のレコードを変更または削除する場合、その変更は人材に同期されません。 人材に変更を加える場合、新しい追跡レコードが作成され、レコードは Common Data Service に更新されます。

- 人材と Common Data Service 間でレコードのアソシエーションを削除するには、**CDS エンティティ名**フィールドでエンティティを選び、**追跡情報をクリアにする**を選択します。

[![追跡情報をクリア](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)

追跡をクリアにした後、エンティティの完全同期を実行するには、次の手順を参照してください。

## <a name="sync-an-entity-between-talent-and-common-data-service"></a>人材と Common Data Service 間のエンティティを同期

Common Data Service からの変更が人材に表示するにはあまりにも長い場合、または追跡をクリアした後に追跡テーブルを更新する必要がある場合は、この手順を使用します。

- 人材と Common Data Service 間のエンティティで完全同期を実行するには、**CDS エンティテ名**フィールドでエンティティを選び、**今すぐ同期**を選択します。

[![完全同期の実行](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)
