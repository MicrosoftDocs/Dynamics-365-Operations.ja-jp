---
title: Common Data Service 統合のコンフィギュレーション
description: Common Data Service と Microsoft Dynamics 365 Human Resources のインスタンス間の統合を、有効または無効にすることができます。 また、同期の詳細を表示したり、追跡データをクリアしたり、エンティティを再同期して、2 つの環境間のデータ問題をトラブルシューティングすることもできます。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 042daf3fdf7a906086af726472da050467d217e3
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009648"
---
# <a name="configure-common-data-service-integration"></a>Common Data Service 統合のコンフィギュレーション

Common Data Service と Microsoft Dynamics 365 Human Resources のインスタンス間の統合を、有効または無効にすることができます。 また、同期の詳細を表示したり、追跡データをクリアしたり、エンティティを再同期して、2 つの環境間のデータ問題をトラブルシューティングすることもできます。

統合をオフにすると、ユーザーは Human Resources または Common Data Service に変更を加えることができますが、これらの変更は 2 つの環境間で同期されません。

既定では、環境のデモ データの有無に応じて、Human Resources と Common Data Service 間の統合は有効または無効になります。

- デモ データを含まない新しい環境において、**無効**
- デモ データを含む新しい環境において、**有効**

デモ データが含まれる新しい環境では、データの準備時にデータの同期が開始されます。

次のような場合は、統合を無効にすることもできます:

- Data Management Framework を介したデータに入力し正しい状態にするには、データを複数回インポートする必要があります。

- Human Resources または Common Data Service のいずれかのデータに問題があります。 統合を無効にする場合、他では削除せず、もう一方の環境でレコードを削除することができます。 統合を有効に戻すと、削除されていない環境のレコードは、削除された環境に同期されます。 同期は次に、 **同期リクエストを失敗した Common Data Service 統合** バッチ ジョブが実行するときに開始されます。

> [!WARNING]
> データ統合を無効する場合、両方の環境で同じレコードを編集しないようにしてください。 統合を有効に戻すと、最後に編集したレコードが同期されます。 したがって、両方の環境でレコードに同じ変更を加えていない場合は、データが失われる可能性があります。

## <a name="access-the-common-data-service-integration-page"></a>Common Data Service 統合のページにアクセス

1. Common Data Service による統合の設定を表示または構成を希望する Human Resources インスタンスで、**システム管理**のタイルを選択します。

    [![システム管理のタイル](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. **リンク**タブを選択します。

    [![リンク タブ](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. **統合**で、**Common Data Service 統合**を選択します。

    [![Common Data Service コンフィギュレーション リンク](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a>Human Resources とCommon Data Service 間でのデータ統合を有効化また無効化

- 統合を有効にするには、 **Common Data Service に統合を有効化** オプションを **はい** に設定します。

    > [!NOTE]
    > 統合を有効にすると、データは次に **同期リクエストを失敗した Common Data Service 統合** バッチ ジョブを実行する時に同期されます。 バッチ ジョブが完了すると、すべてのデータを使用できるようになります。

- 統合を無効にするには、オプションを **いいえ** に設定します。

[![Common Data Service 統合を有効化または無効化](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)

## <a name="view-data-integration-details"></a>データ統合の詳細を表示

**Common Data Service 統合**ページの**管理**クイック タブで、レコードが Human Resources と Common Data Service 間でどのようにリンクされているか確認できます。

- エンティティのレコードを表示するには、**CDS エンティティ名**フィールドでエンティティを選択します。 グリッドには、選択したエンティティにリンクされているすべてのレコードが表示されます。

[![エンティティのレコードを表示](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)

> [!NOTE]
> すべての Common Data Service エンティティが、現在リストにあるわけではありません。 カスタム フィールドの使用をサポートしているエンティティだけが、グリッドに表示されます。 新しいエンティティは、Human Resources の継続的リリースによって利用可能になります。

グリッドには、次のフィールドが含まれています。

- **CDS エンティティ名** – Common Data Service のエンティティ名。
- **CDS エンティティ参照** – レコードを識別するために Common Data Service を使う識別子。 この値は、Human Resources **RecId** 値と同じです。 Microsoft Excel で Common Data Service エンティティうぃ開くと、識別子を確認できます。
- **Human Resources エンティティ名** – 最後にデータを Common Data Service に同期したエンティティ。 エンティティは、Common Data Service の接頭語または別の接頭語を持つことが可能です。
- **Human Resources 参照** – Human Resources のレコードに関連付けられる **Recld** 値。
- **CDS から削除されました** - Common Data Service から削除されたレコードかどうか示す値。

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a>Common Data Service から Human Resources のレコードのアソシエーションを削除

Human Resources と Common Data Service 間のデータ同期中に問題が発生した場合、追跡をクリアにして追跡テーブルを再同期させることで、問題を解決できる可能性があります。 アソシエーションを削除し、Common Data Service のレコードを変更または削除する場合、その変更は Human Resources に同期されません。 Human Resources に変更を加える場合、新しい追跡レコードが作成され、レコードは Common Data Service に更新されます。

- Human Resources と Common Data Service 間でレコードのアソシエーションを削除するには、**CDS エンティティ名**フィールドでエンティティを選び、**追跡情報をクリアにする**を選択します。

[![追跡情報をクリア](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)

追跡をクリアにした後、エンティティの完全同期を実行するには、次の手順を参照してください。

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a>Human Resources と Common Data Service 間のエンティティを同期

Common Data Service からの変更が Human Resources に表示されるのに長くかかる場合、または追跡をクリアした後に追跡テーブルを更新する必要がある場合は、この手順を使用します。

- Human Resources と Common Data Service 間のエンティティで完全同期を実行するには、**CDS エンティティ名**フィールドでエンティティを選び、**今すぐ同期**を選択します。

[![完全同期の実行](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)


