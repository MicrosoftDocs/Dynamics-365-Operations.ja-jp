---
title: Application update 10.0.25 での電子申告フレームワーク API の変更
description: このトピックでは、Microsoft Dynamics 365 Finance バージョン 10.0.25 で電子申告 (ER) フレームワークの API がどのように変更されたのかについて説明します。
author: NickSelin
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 2ad09d205cacb0a736477671ca769caf4ddf9040
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462255"
---
# <a name="electronic-reporting-framework-api-changes-for-application-update-10025"></a>Application update 10.0.25 での電子申告フレームワーク API の変更

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Finance バージョン 10.0.25 で[電子申告 (ER)](general-electronic-reporting.md) フレームワークのアプリケーション プログラミング インターフェイス (API) がどのように変更されたかについて説明します。

## <a name="api-to-enable-a-model-mapping-to-be-run-in-batch-mode"></a>モデル マッピングをバッチ モードで実行できるようにする API

ER フレームワークの[初期](er-apis-app73.md#code-to-run-a-format-mapping-for-data-import) API を使用すると、インタラクティブ モードでデータをインポートするための ER [モデル マッピング](er-overview-components.md#model-mapping-component)を実行できます。 受信ファイル解析用の ER [形式](er-overview-components.md#format-component)と、アプリケーション データ更新用の ER モデル マッピングを指定するために、この API は形式名と統合ポイントを使用します。

ER フレームワークの新しい `ERIModelMappingDestinationWithVirtualSourceRun` パブリック インターフェイスを使用すると、ER モデル マッピングをバッチ モードで実行して、受信ファイルのデータをインポートできます。 ファイルを提供するには、ER ユーザー インターフェイス (UI) でファイルを手動で選択するか、プログラムで提供します。

`ERModelMappingDestinationRun` クラスのコードは、新しい API を使用して、ダイヤログ ボックスの **バックグラウンドで実行** タブを含め、データのインポートをバッチ モードで実行できるようにする方法を示しています。

```xpp
private ERModelMappingDestinationRunController getControllerInternal()
    {
        if (!controller)
        {
            controller = ERModelMappingDestinationRunController::construct();
            controller.parmShowDialog(showPromptDialog);
            controller.showBatchTab(showPromptDialog && showBatchTab && this.isBatchEnabledForFileSource());
            controller.parmDialogCaption(this.getBatchJobCaption());
            controller.parmModelMappingRun(this);
            controller.parmModelDefinitionParameters(parameters);
            controller.parmHiddenParameters(hiddenParameters);
            controller.parmIsImportLoadingFilesFromSource(this.getImportFormatFileSourceContract() != null);
        }
        return controller;
    }

    private boolean isBatchEnabledForFileSource()
    {
        var fileSource = this.getImportFormatFileSourceContract();
        if (ERCast::asAny(fileSource) is ERImportFormatDatasourceByVirtualFileSourceContract)
        {
            return useVirtualImportFormatSource;
        }
        else
        {
            return ERCast::asAny(fileSource) is ERImportFormatDatasourceByFileSourceContract;
        }
    }
```

このインターフェイスの詳細については、[バッチ モードで手動で選択したファイルからデータをインポートする](er-configure-data-import-batch.md)例を完了してください。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]