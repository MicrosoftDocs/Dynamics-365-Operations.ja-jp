---
title: Application update 7.3 での ER フレームワーク API の変更
description: この記事では、Dynamics 365 Finance、Enterprise Edition のアプリケーション更新プログラム 7.3 での電子申告フレームワークの API における変更について説明します。
author: kfend
ms.date: 11/28/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: a208a3a76bb2e59e0fc68b3b5d52e768cc5943a8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280942"
---
# <a name="er-framework-api-changes-for-application-update-73"></a>Application update 7.3 での ER フレームワーク API の変更

[!include [banner](../includes/banner.md)]

この記事では、Dynamics 365 Finance、Enterprise Edition のアプリケーション更新プログラム 7.3 での電子申告 (ER) フレームワークの API における変更について説明します。

ER API には 2 つのタイプの変更があります。

- いくつかの X++ クラスが外部アセンブリに X++ から移行されました。
- X++ クラスの残りの部分は、内部としてマークされています。

## <a name="how-to-access-classes-that-were-moved-from-x-to-an-external-assembly"></a>外部アセンブリに X++ から移行されたクラスへのアクセス方法

外部クラスにアクセスするには、ファイルの先頭に **using** ディレクティブを追加する必要があります。

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
```

たとえば、追加の変更をせずに外部クラスにアクセスすることができます。

```xpp
var destination = new ERFileDestinationMemory();
```

名前空間のエイリアスを作成することもできます。

```xpp
using LF = Microsoft.Dynamics365.LocalizationFramework;
```

作成した名前空間のエイリアスを使用して、外部のクラスを参照することができます。

```xpp
var destination = new LF.ERFileDestinationMemory();
```

## <a name="how-to-access-internal-x-objects-by-using-erobjectsfactory"></a>ERObjectsFactory を使用して内部 X++ オブジェクトにアクセスする方法

アプリケーションの更新プログラム 7.3 以降では、呼び出し元のコードは **ERObjectsFactory** クラスのメソッドを使用して ER オブジェクトにアクセスする必要があります。 これらの変更の例をいくつか示します。

### <a name="code-to-display-a-format-mapping-lookup"></a>フォーマット マッピング ルックアップを表示するコード

アプリケーション 更新 7.3 より前

```xpp
// pattern
ERFormatMappingTableLookup::lookupFormatMapping(<form control>, <model name>[, <data container name>]);
// sample code
ERFormatMappingTableLookup::lookupFormatMapping(_referenceGroupControl, bankLCMiscChargeReportERModelName);
```

アプリケーション更新プログラム 7.3 以降

```xpp
// pattern
ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(<form control>, <model name>[, <data container name>]).performFormLookup();
// sample code
ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(_referenceGroupControl, bankLCMiscChargeReportERModelName).performFormLookup();
```

### <a name="code-to-run-a-format-mapping-for-data-export"></a>データ エクスポート用のフォーマット マッピングを実行するためのコード

アプリケーション 更新 7.3 より前

```xpp
// pattern
ERFormatMappingRun::constructByFormatMappingId(<format mapping id>, <file name>, <show prompt dialog>).run();
// sample code
ERFormatMappingRun::constructByFormatMappingId(erBinding, '', true).run();
```

アプリケーション更新プログラム 7.3 以降

```xpp
// pattern
ERObjectsFactory::createFormatMappingRunByFormatMappingId(<format mapping id>, <file name>, <show prompt dialog>).run();
// sample code
ERObjectsFactory::createFormatMappingRunByFormatMappingId(erBinding, '', true).run();
```

### <a name="code-to-run-a-format-mapping-for-data-import"></a>データ インポート用の形式マッピングを実行するためのコード

アプリケーション 更新 7.3 より前

```xpp
// pattern
ERModelMappingDestinationRun::constructByImportFormatMappingId(<mapping id>, <integration point>).run();
// sample code
ERModelMappingDestinationRun::constructByImportFormatMappingId(custPaymModeTable.ERModelMappingTable, CustVendOutPaymConstants::IntegrationPoint).run();
```

アプリケーション更新プログラム 7.3 以降

```xpp
// pattern
ERObjectsFactory::createMappingDestinationRunByImportFormatMappingId(<mapping id>, <integration point>).run();
// sample code
ERObjectsFactory::createMappingDestinationRunByImportFormatMappingId(custPaymModeTable.ERModelMappingTable, CustVendOutPaymConstants::IntegrationPoint).run();
```

### <a name="code-to-create-a-browser-file-destination"></a>ブラウザー ファイルの宛先を作成するためのコード

アプリケーション 更新 7.3 より前

```xpp
// sample code
new ERFileDestinationBrowser();
```

アプリケーション更新プログラム 7.3 以降

```xpp
// sample code
ERObjectsFactory::createFileDestinationBrowser();
```

### <a name="code-to-create-an-attachment-file-destination"></a>添付ファイルの宛先を作成するためのコード

アプリケーション 更新 7.3 より前

```xpp
// pattern
ERFileDestinationAttachment::construct(<record>, ERDocuManagement::instance().otherDocuType());
// sample code
ERFileDestinationAttachment::construct(_cashRegisterFiscalTrans_W, ERDocuManagement::instance().otherDocuType());
```

アプリケーション更新プログラム 7.3 以降

```xpp
// pattern
ERObjectsFactory::createFileDestinationAttachmentWithOtherDocuType(<record>);
// sample code
ERObjectsFactory::createFileDestinationAttachmentWithOtherDocuType(_cashRegisterFiscalTrans_W);
```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
