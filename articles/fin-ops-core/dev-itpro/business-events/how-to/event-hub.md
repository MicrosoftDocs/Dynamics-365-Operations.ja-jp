---
title: ビジネス イベント と Azure イベントのハブ
description: このチュートリアルでは、 Microsoft Azure イベント ハブでビジネス イベントを機能させるために実行する必要のある手順を扱います。
author: Sunil-Garg
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: Platform update 28
ms.dyn365.ops.version: 2019-07-31
ms.openlocfilehash: e492866fdb291d5b3ba249009abd8f11c9a5438c
ms.sourcegitcommit: 85141b21ac90f3db1b378c21f9c7f3d8f74e182f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129447"
---
# <a name="business-events-and-azure-event-hubs"></a>ビジネス イベント と Azure イベントのハブ

[!include[banner](../../includes/banner.md)]

このチュートリアルでは、 Microsoft Azure イベント ハブでビジネス イベントを機能させるために実行する必要のある手順を扱います。

1. Azure ポータルで、 Active Directory アプリケーションの登録を行います。 アプリケーション ID をメモします。

    ![アプリケーション (クライアント) ID の値。](../../media/BE_EH_aad.PNG)

2. アプリケーションに Azure Key Vault アプリケーション プログラミング インタフェース (API) の許可を付与します。

    ![Azure Key Vault API にアプリのアクセス許可を付与する。](../../media/BE_EH_api.png)

3. アプリケーションの登録で、アプリケーションの秘密を作成します。 値をメモします。

    ![アプリケーションのシークレットの作成。](../../media/BE_EH_secret.jpg)

4. key vaultにて、新規アプリの登録に許可を付与します。

    ![アプリ登録に Key Vault のアクセス許可を付与する。](../../media/BE_EH_permission.jpg)

5. key vault にて、新たな秘密を作成します。 この秘密に格納される値は、ご利用のイベントハブへの接続文字列である必要があります。 値をメモします。

    ![接続文字列。](../../media/BE_EH_connectionstring.jpg)

6. イベント ハブのエンドポイント構成を作成します。 **システム管理 \> 設定 \> ビジネス イベント \> ビジネス イベント カタログ** へと移動し、 **エンドポイント** タブにて、 **新規** を選択して **新規エンドポイントの構成** ウィザードを起動します。

    ![新規エンドポイント ウィザードを構成します。](../../media/BE_EH_endpointconfig.jpg)

7. **エンドポイントの種類** フィールドで、 **Azure イベント ハブ** を選択します。
8. **次へ** を選択します。
9. **エンドポイント名称** フィールドで、エンドポイントの名前を入力します。
10. **ハブの名称** フィールドで、イベントハブの名前を入力します。
11. **Azure Active Directory アプリケーション ID** フィールドで、上記で作成したアプリケーションIDを入力します。
12. **Azure アプリケーションの秘密** フィールドで、上記で作成した値を入力します。
13. **Key Vault のDNS名称** フィールドで、Key Vault の ドメインネームシステム (DNS)の名前を入力します。 この値は、Azure ポータルの key vault 設定の **概要** タブで確認することができます。
14. **AKey Vault の秘密の名称** フィールドで、上記で作成した秘密の名称を入力します。
15. **OK** を選択します。
16. 以上で、このエンドポイントに送信する1つ以上のビジネス イベントを有効化することができます。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
