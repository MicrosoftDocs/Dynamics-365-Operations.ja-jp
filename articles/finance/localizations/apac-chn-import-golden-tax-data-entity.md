---
title: 中国金税ファイルのインポート
description: この記事では、中国金税ファイルを Microsoft Microsoft Dynamics 365 Finance にインポートする方法について説明します。
author: mrolecki
ms.date: 12/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.region: China (PRC)
ms.author: mrolecki
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 261394
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr
ms.openlocfilehash: f9fc6e32b80be4d10acf83404a47b5cb9916c494
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286667"
---
# <a name="import-the-chinese-golden-tax-files"></a>中国金税ファイルのインポート

[!include [banner](../includes/banner.md)]
  
この記事では、外部請求書番号を持つファイルをプロバイダ (Aisino または BaiWang) から Dynamics 365 Finance にインポートする方法について説明します。 txt と xml ファイルを BaiWang プロバイダから、txt と txt ファイルを Aisino プロバイダからインポートできます。

外部請求書番号を含むプロバイダからファイルをインポートするには、次の手順を実行します。

1. **売掛金勘定** > **定期処理タスク** > **VAT 請求書統合** の順で移動します。
2. アクション ウィンドウで、**インポート** を選択します。 
3. エクスポートされた請求書を統合するプロバイダのソフトウェアに応じて、Aisino または BaiWang のどちらかのプロバイダのから 1 つインポート ファイルのモデル マッピングを選択します。 
   - BaiWang プロバイダからテキスト ファイル (\<file name\>_invoicing result.TXT) をインポートするには、**インポート BaiWang TXT ファイル** オプションを **はい** に設定します。 次に、**モデル マッピング** フィールドで、**BaiWang – txt ファイル** を選択します。
   - テキスト ファイルを BaiWang の Aisino または XML ファイルからインポートするには、**BaiWang txt ファイルをインポート** オプションを **いいえ** に設定します。 **モデル マッピング** フィールドで、**Asimo - txt** または **BaiWang-xml ファイル** を選択します。
6. アップロードのファイルを選び、**アップロード** を選択します。
7.  **OK** を選択します。
  
 > [!NOTE] 
 > ファイルをインポートするには、インポート形式をアップロードします。 詳細については、[コンフィギュレーションをインポートする](apac-chn-tax-integration.md) を参照してください。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
