---
title: ワークスペースのクラスを使用してフィールドを必須にする
description: この記事では、ワークスペース クラスを使用して、フィールドを必須にする方法について説明します。
author: jasongre
ms.date: 05/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2017-07-20
ms.dyn365.ops.version: Platform update 3
ms.custom: 255544
ms.assetid: ''
ms.openlocfilehash: 812550879cc63cc1023b9836eebaf120982e8fd1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291744"
---
# <a name="make-fields-mandatory-by-using-workspace-classes"></a>ワークスペースのクラスを使用してフィールドを必須にする

[!include [banner](../../../includes/banner.md)]
[!include [mobile app deprecated](../../../includes/mobile-app-deprecation-banner.md)]

モバイル アプリ デザイナーを使用してアクション用のフィールドを選択するとき、一部のプロパティは推定できます。 これらのプロパティには、フィールドの長さ、タイプ、フィールドが必須かどうかが含まれます。 これらのプロパティを更新するには、ワークスペース クラスを使用します。 たとえば、次の図に示すように、顧客レコードが作成されると **名前** フィールドが必須になるよう指定する場合があります。

![アクションおよびフィールド。](media/workspace-api/MarkFieldAsMandatoryDesigner.png)

![必須フィールドがマークされているアクション。](media/workspace-api/MarkFieldAsMandatoryAction.png)

ワークスペース クラスを使用して **配送条件** フィールドを必須にするには、これらの手順に従います。

1. アプリ デザイナーを使用して、コントロール名を取得します。 この例では、コントロール名は **DynamicDetail_DlvTerm** です。
2. 次のコードを追加して、コントロールの **必須** プロパティを設定します。 このコードでは、リフレクションベースの **setProperty** メソッドを使用して **必須** プロパティを設定しています。

    ```javascript
    public SysAppWorkspaceMetadata getWorkspaceMetadata()
    {
        SysAppWorkspaceMetadata appMetadata;
        appMetadata = super();
        var createCustAction = appMetadata.getAction("createCust");
        this.setCustAccountMandatory(createCustAction);
        return appMetadata;
    }
    private void setCustAccountMandatory(SysAPpActionMetadata _createCustAction)
    {
        var custAccount = +createCustAction.getControl("DynamicDetail_DlvTerm");
        custAccount.setProperty("Mandatory", true);
    }
    ```

3. ソリューションをビルドし、モバイル アプリでアプリのメタデータを更新します。

**配送条件** フィールドは、次の図に示すように **必須** としてマークされるようになりました。

![配送条件フィールドは必須とマークされています。](media/workspace-api/MarkFieldAsMandatoryFinal.png)


[!INCLUDE[footer-include](../../../../../includes/footer-banner.md)]
