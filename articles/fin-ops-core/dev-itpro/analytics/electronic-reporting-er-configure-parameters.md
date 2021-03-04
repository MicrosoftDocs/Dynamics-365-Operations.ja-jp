---
title: 電子申告 (ER) フレームワークの構成
description: このトピックでは、電子レポート (ER) フレームワークのパラメーターを構成する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace, ERParameters, ERFormatDestinationTable
audience: Developer, IT Pro
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: 3c1291de-230c-4e31-96c4-ba69a310690a
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 7dd4e7208bebc05ce49bc00b8d9980d0c92c9a31
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687144"
---
# <a name="configure-the-electronic-reporting-er-framework"></a>電子申告 (ER) フレームワークの構成

[!include [banner](../includes/banner.md)]

このトピックでは、電子申告 (ER) の基本機能を設定する方法について説明します。 また、ER を設定する前に完了する必要のある手順も説明します。

## <a name="prerequisites-for-er-setup"></a>ER セットアップの前提条件
ER を設定する前に、ドキュメント管理で必要な [ドキュメント タイプ](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) を設定する必要があります。

- ER レポート テンプレートとして使用される Microsoft Office ドキュメントのドキュメント タイプ。
- ジョブ アーカイブに ER レポートの出力を保存するために使用するドキュメント タイプ。
- 他のプログラムで表示できるように、ER レポートの出力を保存するために使用するドキュメント タイプ。
- ER コンフィギュレーションの出力のベースラインを保持するために使用されるドキュメント タイプ。
- その他のすべての目的で、ER フレームワーク内のファイルを処理するために使用されるドキュメント タイプ。

各ドキュメント タイプについては、次の属性値を選択できます。

| 属性名 | 属性値                     |
|----------------|-------------------------------------|
| クラス          | **ファイルの添付**                     |
| グループ化          | **ファイル**                            |
| 保管場所       | **Azure Storage** もしくは **SharePoint** |

## <a name="set-up-er"></a>ER の設定
すべての法人に対して ER の基本機能を設定するには、次の手順を使用します。

1. **電子申告** ワークスペース ページを開きます。
2. **電子申告のパラメーター** をクリックします。

## <a name="main-parameters"></a>主なパラメーター

**電子申告のパラメーター** ページの **一般** タブで、次の ER パラメーターを設定します:

- **デザイン モードを有効にする**

    - このオプションを **はい** に設定すると、埋め込み ER デザイナーが有効になり、ユーザーが独自の ER コンフィギュレーションを作成できるようになります。
    - ユーザーが [コンフィギュレーション サービス](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) にサインアップして ER デザイナーの機能にアクセスすることを要求するには、このオプションを **いいえ** に設定します。

- **データ処理の ER パフォーマンスの追跡を無効にします**

    - このオプションを **いいえ** に設定すると、Microsoft Telemetry は単一の着信または送信レコードを ER コンフィギュレーションとして処理するために必要な平均時間に関する情報を収集できます。 この情報は、環境の特定の正常性指標として追跡され、Microsoft が ER フレームワークを使用するお客様に影響する問題をすばやく特定して対処するのに役立ちます。
    - テレメトリ情報の収集を停止するには、このオプションを **はい** に設定します。

[![電子申告パラメーター ページの一般タブ](./media/er-configure-parameters-main.png)](./media/er-configure-parameters-main.png)

## <a name=""></a><a name="ManageDocumentsParameters">ドキュメントを管理するためのパラメーター</a>

**電子申告のパラメーター** ページの **添付ファイル** タブで、次の ER パラメーターを設定します:

- **コンフィギュレーション** – ドキュメント タイプを選択して、ER 形式のテンプレートの保存場所を指定します。 このドキュメント タイプは、特定の会社の範囲内で選択されます。 ER 形式が使用されている間、ユーザーがサインインしている会社に関係なく、このドキュメント タイプが使用されます。
- **ジョブ アーカイブ** – ドキュメント タイプを選択して、ER ジョブ [アーカイブ](er-destination-type-archive.md) のレコードに添付される生成済みドキュメントの保存場所を指定します。 このドキュメント タイプは、会社固有のドキュメント タイプとして選択されます。 選択したドキュメント タイプが、ER 形式を実行する予定のすべての会社に設定されていることを確認し、その結果を ER ジョブ アーカイブに保存する必要があります。
- **一時** – ドキュメント タイプを選択して、他の目的に使用される生成されたドキュメントの保存場所を指定します。 たとえば、他のサービスによる [プレビュー](er-destination-type-screen.md) 用にドキュメントが生成される場合があります。 このドキュメント タイプは、会社固有のドキュメント タイプとして選択されます。 選択したドキュメント タイプが、ER 形式を実行する予定のすべての会社に設定されていることを確認し、その結果を ER ジョブ アーカイブに保存する必要があります。
- **ベースライン** – ドキュメント タイプを選択して、ER コンフィギュレーションの自動テスト中に [ベースライン](er-trace-reports-compare-baseline.md) として使用されるドキュメントの保存場所を指定します。 このドキュメント タイプは、会社固有のドキュメント タイプとして選択されます。 選択したドキュメント タイプが、ER 形式を実行する予定のすべての会社に設定されていることを確認し、その結果を ER ジョブ アーカイブに保存する必要があります。
- **その他** – ドキュメント タイプを選択して、他のすべての目的に使用される生成されたドキュメントの保存場所を指定します。 このドキュメント タイプは、会社固有のドキュメント タイプとして選択されます。 選択したドキュメント タイプが、ER 形式を実行する予定のすべての会社に設定されていることを確認し、その結果を ER ジョブ アーカイブに保存する必要があります。
- **テンプレートのバックアップ コピーの作成を停止**

    - このオプションを **いいえ** に設定すると、ER 形式のコンフィギュレーション テンプレートのバックアップ コピーを自動的に作成し、データベース ストレージにそのコピーを保存します。
    - ER 形式のコンフィギュレーション テンプレートのバックアップ コピーを停止するには、このオプションを **はい** に設定します。

    詳細については、[ER テンプレートのバックアップストレージ](er-backup-storage-templates.md) を参照してください。

[![電子申告パラメーター ページの添付ファイル タブ](./media/er-configure-parameters-documents.png)](./media/er-configure-parameters-documents.png)

## <a name="lcs-parameters"></a>LCS パラメーター

**電子申告のパラメーター** ページの **LCS** タブで、Microsoft Dynamics Lifecycle Services (LCS) のリポジトリから ER コンフィギュレーションの読み込みに使用する必要がある並列スレッドの数を定義し、最も効率的な方法でコンフィギュレーションが読み込まれます。 値の範囲は、現在のプログラムで使用可能なリソースに応じて、**1** から **15** です。 この設定とその他のタスクの数とその優先順位に基づいて、スレッドの実際の数が自動的に定義されます。

[![電子申告パラメーター ページの LCS タブ](./media/er-configure-parameters-lcs.png)](./media/er-configure-parameters-lcs.png)

## <a name="rcs-parameters"></a>RCS パラメーター

**電子申告のパラメーター** ページの **RCS** タブで、[コンフィギュレーション サービス](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) にサインアップします。

[![電子申告パラメーター ページの RCS タブ](./media/er-configure-parameters-rcs.png)](./media/er-configure-parameters-rcs.png)

## <a name="active-er-configurations-provider"></a>アクティブな ER コンフィギュレーション プロバイダー

**コンフィギュレーション プロバイダー テーブル** ページで、ER プロバイダー レコードを作成します。 各プロバイダーは、**アクティブ** として [マーク](tasks/er-configuration-provider-mark-it-active-2016-11.md) されます。 アクティブなプロバイダーの名前とインターネット アドレスは、コンフィギュレーション所有者の属性として ER コンフィギュレーションに格納されます。

## <a name="optional-setup-for-er"></a>ER のオプションの設定
基本機能に加えて、ER に設定できる他の機能があります。

- **電子申告の送信先** ページで、各 ER 形式コンフィギュレーションの各ファイル出力の ER 出力先を定義します。 以前に設定したドキュメント管理フレームワークの [ドキュメント タイプ](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) を使用します。 また、各法人に対して ER のオプション機能を設定するためにこのページを使用することもできます。 詳細については、[電子申告 (ER) の送信先](electronic-reporting-destinations.md) を参照してください。
- 新しいアプリケーション オブジェクト ツリー (AOT) のコンポーネントを追加するか、ER でデータ ソース (テーブル、ビュー、またはデータ エンティティ) として使用される既存の AOT コンポーネントを更新する場合は、**テーブル参照の再構築** メニュー項目 (**組織管理** \> **電子申告** \> **テーブル参照の再構築**) を使用して、AOT の変更を ER メタデータに反映します。

## <a name="frequently-asked-questions"></a>よく寄せられる質問
**質問:** LCS から ER コンフィギュレーションを読み込むのに最適な並列スレッド数はどれくらいですか。

**回答:** 最適な並行スレッドの数を計算するには、次の経験式を使用します。コア ÷ 2 + 1(2)。 たとえば、プログラムが 2 つの CPU を持つ仮想マシン (VM) を実行する場合、各 CPU には 4 つのコアが含まれ、最適な数は 5 または 6 の並列スレッドです。

**質問:** AOT にカスタム テーブルを追加しました。 ER データ モデルの新しい ER モデル マッピング コンフィギュレーションを作成しました。 モデルのマッピングの設計中に、個人のテーブルを指す、新しいデータ ソース タイプ **テーブル レコード** を追加しようとします。 テーブル名を **テーブル** ルックアップに手動で追加し、ER モデル マッピングではエラーまたは警告なしで承認されました。 ただし、個人のテーブル名は、このデータ ソースの **テーブル** ルックアップが提供する利用可能な選択肢の一覧に含まれていません。 テーブルの名前をどのように含めますか。

**回答**: カスタムテーブルの名前を **テーブル** ルックアップに含めるには、このトピックの前半の「ER のオプション設定」セクションで説明されているように、**テーブル参照の再構築** メニュー項目を使用してください。

**質問:** 実稼動環境の **電子申告** ワークスペースで、Microsoft プロバイダーを **有効** としてマークできないのはなぜですか。

**回答:** Microsoft プロバイダーは、Microsoft が設計および管理している ER コンフィギュレーションをマークするために使用されます。 Microsoft は、今後、構成の新しいバージョンをリリースすることを考えてています。 Microsoft プロバイダーを **有効** とマークしないことをお勧めします。 それ以外の場合、構成を更新できます。 (たとえば、コンテンツを変更して新しいバージョンを登録することができます。) これらのアップデートにより、Microsoft がコンフィギュレーションの新しいバージョンを提供するときに、今後問題が発生します。これらの新しいバージョンをインポートして採用する必要があります。 代わりに、会社の新しい ER プロバイダーを登録し、ER 構成の管理に使用します。 Microsoft 構成を再利用するには、派生コピーのベースとして選択します。 Microsoftによって提供される変更を組み込むには、構成が新しいバージョンの Microsoft 構成に使用可能になったときに、その構成をリベースします。

**質問:** 1 つの会社で ER 形式を正常に実行しました。 ただし、別の会社で同じ ER 形式を実行して同じ設定を使用すると、次のエラー メッセージが表示されます: "指定されたドキュメント タイプはファイル タイプではありません。" なぜですか。

**回答:** ほとんどの場合、2 番目の会社には、**ジョブ アーカイブ**、 **一時**、 **ベースライン**、 **その他**、 [ERパラメータ](#ManageDocumentsParameters) で選択されたドキュメント タイプが含まれていません。 この問題を修正するには、2 番目の会社でこれらのドキュメント タイプを設定します。

## <a name=""></a><a name="AdditionalResources">追加リソース</a>

- [電子申告 (ER) の概要](general-electronic-reporting.md)
- [電子申告 (ER) の送信先](electronic-reporting-destinations.md)
- [Regulatory Services のコンフィギュレーション サービス](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]