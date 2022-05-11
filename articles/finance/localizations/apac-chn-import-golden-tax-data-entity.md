---
title: 中国金税ファイルのインポート
description: このトピックでは、中国金税ファイルを Microsoft Microsoft Dynamics 365 Finance にインポートする方法について説明します。
author: ilkond
ms.date: 12/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr
audience: IT Pro
ms.reviewer: kfend
ms.custom: 261394
ms.search.region: China (PRC)
ms.author: ilyako
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 443a62e55865da9ea443eadf8f3602dec96236af
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2022
ms.locfileid: "8565807"
---
# <a name="import-the-chinese-golden-tax-files"></a>中国金税ファイルのインポート

[!include [banner](../includes/banner.md)]
  
このトピックでは、外部請求書番号を持つファイルをプロバイダ (Aisino または BaiWang) から Dynamics 365 Finance にインポートする方法について説明します。 txt と xml ファイルを BaiWang プロバイダから、txt と txt ファイルを Aisino プロバイダからインポートできます。

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
