---
title: Dynamics 365 財務と運用バージョン 8.1.3 (2019 年 1 月) の新機能および変更された機能
description: この記事では、Dynamics 365 財務と運用バージョン 8.1.3 の新機能または変更された機能について説明します。 このバージョンは、2019 年 1 月にリリースされます。
author: sericks007
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Release 8.1.3
ms.custom: ''
ms.assetid: b364a31d-34de-45c5-b698-64c5262c592e
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: b8298cfdc129f63a07e2843fc26f22b3a88a4325
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279366"
---
# <a name="whats-new-or-changed-in-dynamics-365-finance-and-operations-version-813-january-2019"></a>Dynamics 365 財務と運用バージョン 8.1.3 (2019 年 1 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 財務と運用バージョン 8.1.3 の新機能または変更された機能について説明します。 このバージョンは 2019 年 1 月にリリースされ、ビルド番号は 8.1.227 です。

Retail の新機能または変更された機能についての最新のリリースについては、[Dynamics 365 for Retail の新機能または変更された機能](../../../commerce/get-started/whats-new.md) を参照してください。

### <a name="dynamics-365-october-18-release-notes"></a>Dynamics 365 2018 年 10 月リリース ノート

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[2018 年 10 月リリース ノートを確認](/dynamics365/release-plans/). あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="bug-fixes"></a>バグ修正

Finance and Operations 8.1.3 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://go.microsoft.com/fwlink/?linkid=2049362)を参照してください。

### <a name="platform-update-23"></a>プラットフォーム update 23

プラットフォーム更新プログラム 23 を含む Microsoft Dynamics 365 財務と運用バージョン 8.1.3。 プラットフォーム更新プロフラム 23 の詳細ついては、[Dynamics 365 Finance プラットフォーム更新プログラム 23 の新機能や変更 (2019 年 1 月)](whats-new-platform-update-23.md) を参照してください。

## <a name="extensibility-enhancements"></a>拡張性の強化

Finance and Operations の今回のリリースでは、列挙、メタデータ、メソッドの強化など、拡張性をサポートするために、さまざまな拡張機能の強化が加えられています。 詳細については、[Dynamics 365 Finance バージョン 8.1.3 の拡張機能の変更](../../dev-itpro/extensibility/extensibility-changes-813.md) を参照してください。

## <a name="collection-letters"></a>督促状

各トランザクションの督促状コードが追跡されるが、顧客に保存されている単一の督促状レベルに基づいて督促状の処理が行われるように、顧客レベルで督促状を設定することができるようになりました。 詳細については、[督促状の処理](../../../finance/accounts-receivable/tasks/process-collection-letters.md)を参照してください。

## <a name="settle-remainder"></a>残余決済

その金額を勘定科目または他の顧客に適用することで、決済活動から残りの金額を決済することができます。 仕訳帳に入力された金額を決済するとき、または未処理トランザクションのみを決済するときに、残りの部分を決済できます。 詳細については、[残余決済](../../../finance/cash-bank-management/settle-remainder.md)を参照してください。

## <a name="globalization"></a>グローバリゼーション

### <a name="electronic-reporting-import-from-files-in-json-format"></a>電子申告: JSON 形式のファイルからのインポート

JSON 形式の受信ファイルを解析するために電子的なレポート (ER) 形式を構成できるようになりました。 その場合、アプリケーション データを更新するために JSON ファイルからの情報がどのように使用されるかを指定する ER マッピングを設定することができます。

### <a name="electronic-reporting-support-country-context-specific-er-model-mappings"></a>電子申告: 国コンテキスト固有の ER モデル マッピングのサポート
ER モデル マッピングの国コンテキストを指定することができます。 また、1 つの ER データ モデルの複数の国固有のマッピングを管理することもできます。 これにより、1 つの ER モデル マッピングにおけるデータ アクセスの国固有のロジックを特定できます。 法人の基本住所によっては、ER 形式が電子ドキュメントを生成するために使用される場合、該当する国/地域固有のモデル マッピングが使用されます。 

## <a name="russian-specific-features"></a>ロシア固有の機能
今回のリリースには、ロシアの次の機能が含まれています。

### <a name="accounts-receivable"></a>売掛金管理
- 税登録では、ロシア税会計原則に従って課税利益および損失を追跡して管理できます。 次の税登録を使用できるようになりました。
  -  **売掛金勘定の棚卸資産活動** の引当 
  -  **売掛金 – 貸倒損失引当** の引当
  -  **売掛金 – 貸倒損失引当の移動** の引当 
  -  **売掛金勘定の棚卸資産の移動** の引当 
- 売掛金貸倒損失を損金処理できるようになりました。
 
### <a name="accounts-payable"></a>買掛金管理
 - 税登録では、ロシア税会計原則に従って課税利益および損失を追跡して管理できます。 次の税登録を使用できるようになりました。
   - **買掛金勘定の棚卸資産活動** の引当
   - **買掛金勘定の借入金移動** の引当 
 - 買掛金貸倒損失を損金処理できるようになりました。

### <a name="client-bank-interface-and-reconciliation-procedure"></a>クライアント-銀行のインターフェイスと調整手順
今回のリリースでは、クライアント-銀行機能を使用するために必要なインターフェイスと電子レポートのコンフィギュレーション例を追加します。
この機能を使用するには、次の電子レポート構成を Lifecycle Services からインポートし、次の設定で選択してください。
- 支払モデル model.version.22
- 出力先 (RU).version.22.4への支払モデル マッピング
- 口座取引明細書 (RU).version.22.6
- 支払指示 (RU).version.22.4


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

