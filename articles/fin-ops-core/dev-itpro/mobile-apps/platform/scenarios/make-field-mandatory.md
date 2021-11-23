---
title: ワークスペースのクラスを使用してフィールドを必須にする
description: このトピックでは、ワークスペース クラスを使用して、フィールドを必須にする方法について説明します。
author: tonyafehr
ms.date: 07/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 255544
ms.assetid: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-07-20
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: fcfb4162130fb31b0acceb8b6cdbeb8ad3ae8e99
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781504"
---
# <a name="make-fields-mandatory-by-using-workspace-classes"></a>ワークスペースのクラスを使用してフィールドを必須にする

[!include [banner](../../../includes/banner.md)]

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