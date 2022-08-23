---
title: インドネシア向け源泉徴収税レポート
description: この記事では、インドネシアの源泉徴収税レポートを構成および生成する方法について説明します。
author: AdamTrukawka
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-12-02
ms.dyn365.ops.version: 10.0.20
ms.search.scope: ''
ms.openlocfilehash: 732db563532ebc46c7b9fc69c2aaa128640084f5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282438"
---
# <a name="withholding-tax-report-for-indonesia-id-00005"></a>インドネシア向け源泉徴収税レポート (ID-00005)

[!include [banner](../includes/banner.md)]

この記事では、インドネシアの法人が e-Bupot アプリケーションで源泉徴収税トランザクションを報告するために使用する、PPH 源泉徴収税ファイルの設定と生成を行う方法を説明します。

インドネシア税所轄官庁 (DGT) は課税対象の事業主 (PKP) を決定し、e-Bupot アプリケーションを使用して所得税レポートを電子申告する必要があるため、所得税の源泉徴収者/徴収者 (PPh) は KPP Pratama に登録されます (第 23 条および第 26 条)。 

- **第 23 条** – このレポートは、プライマリ住所の国/地域コードがインドネシアのコードに設定されたベンダーの、源泉徴収トランザクションをすべて含みます。
- **第 26 条** – このレポートは、プライマリ住所の国/地域コードがインドネシアのコードに設定されていないベンダーの、源泉徴収トランザクションをすべて含みます。

## <a name="prerequisites"></a>必要条件

- 法人のプライマリ住所がインドネシアである必要があります。
- **機能の管理** ワークスペースで **グローバル源泉徴収税** 機能を有効化する必要があります。 この機能を有効にする方法についての詳細は、[機能管理の概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。

### <a name="download-electronic-reporting-configurations"></a>電子申告構成のダウンロード

インポート ファイルの生成は電子申告 (ER) 構成に基づきます。 構成可能なレポートの機能および概念に関する詳細については、[電子申告](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) を参照にしてください。

生産およびユーザー受け入れテスト (UAT) 環境については、[Lifecycle Services から電子申告構成をダウンロードする](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md) の手順に従ってください。

インポート ファイルを生成する場合は、リポジトリから次の構成をアップロードします。

- **Tax declaration model.version.93.xml** 以降のバージョン
- **Tax declaration model mapping.version.93.153.xml** 以降のバージョン
- **WHT PPh schema import (ID).version.93.14** 以降のバージョン

## <a name="set-up-general-ledger-parameters"></a>総勘定元帳パラメーターの設定

1. **税** \> **設定** \> **総勘定元帳パラメーター** の順に移動します。
2. **源泉徴収税** タブの **WHT 申告フォーマット マッピング** フィールドで、**WHT PPh schema import (ID)** を選択します。 
3. **税** \> **設定** \> **源泉徴収税** \> **源泉徴収税の収益タイプ** に移動して、源泉徴収税の収益タイプ **Kode Bukti Potong** を設定し、関連する品目の源泉徴収税グループにコードを割り当てます。 e-Bupot アプリケーションを使用して統合ファイルを生成する場合には、コードが必要です。 

## <a name="generate-the-withholding-import-file"></a>源泉徴収インポート ファイルを生成する

特定の期間に対して e-Bupot ファイルの準備と生成を行うプロセスは、決済または支払後の税務で転記した源泉徴収税トランザクションに基づきます。

次の手順に従ってファイルを生成します。

1. **税** \> **申告** \> **源泉徴収税** \> **PPH インポート ファイル e-bupot 23 および 26** に移動します。
2. レポートの "開始" 日と "終了" 日を選択し、決済期間を選択します。
3. トランザクションの日付を入力して **OK** を選択します。
4. 言語を選択します。 すべてのレポートは米国英語 (**en-us**) とインドネシア語 (**id**) に翻訳されます。
5. ビジネス タイプを選択し、チェック番号および文書番号を入力します。 
6. マネージャーがレポートに署名したかどうかを確認します。 この情報はファイルで報告されます。 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
