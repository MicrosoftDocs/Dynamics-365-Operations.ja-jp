---
title: "サンドボックス環境のアップグレード"
description: "このトピックでは、非実稼働サンドボックス環境またはスタンドアロン サンドボックス環境へのデータ アップグレードを実行する手順について説明します。"
author: tariqbell
manager: AnnBe
ms.date: 03/22/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 269234
ms.assetid: feb8ca24-e86d-4101-b77f-c04137e176d0
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 4b7f144f69348f7a11d7a11a533cf11dbfd508d1
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="upgrade-sandbox-environments"></a>サンドボックス環境のアップグレード

[!include [banner](../includes/banner.md)]

このトピックでは、標準またはプレミアの承認テスト (第 2 層または第 3 層) 以上のサンドボックス環境でデータ アップグレードを実行する手順について説明します。

一部の環境では、Microsoft サービス エンジニアリング チーム (DSE) がデータのアップグレードを実行します。 詳細については、[Microsoft Dynamics 365 for Finance and Operations の最新の更新への移動の概要](upgrade-latest-update.md#scenario-3-upgrade-to-the-latest-application-release) で「エンド ツー エンドのアップグレード プロセス」を参照してください。

> [!NOTE]
> この記事では、*サンドボックス* という用語を使用して SQL Azure データベースに接続されている標準またはプレミア承認テスト (レベル 2 または 3)、またはより高度な環境を示します。

## <a name="prerequisites"></a>前提条件

独立したソフトウェア ベンダー (ISV) からのカスタマイズやソリューションがある場合は、開始する前に [コード アップグレード](upgrade-latest-update.md#scenario-2-upgrade-your-custom-code) を完了する必要があります。 アップグレードされた配置可能なパッケージを、Microsoft Dynamics Lifecycle Services (LCS) のアセット ライブラリにも用意する必要があります。

サンド ボックス環境でアップグレードする前に、開発環境でデータのアップグレードを実行することを強くお勧めします。 開発環境でプロセスを修正して再実行するほうが速いです。 したがって、まず開発環境で作業することで、アップグレードに必要な全体的な時間を短縮できます。

## <a name="export-the-database"></a>データベースをエキスポート

Bacpac ファイルにアップグレードする既存のサンド ボックス環境から、データベースをエクスポートします。 詳細については、[後から復元するため Finance and Operations データベースのコピー](../database/copy-operations-database.md) を参照してください。

### <a name="additional-steps-for-management-reporter"></a>Management Reporter 向け追加手順

レポート デザイナーからレポート定義、またはビルディング ブロック グループをエクスポートします。 エクスポートされたファイルを安全な場所に移動し、後でそのファイルを使用してレポート定義を再インポートできます。 詳細については、[レポート パーツ グループ](https://msdn.microsoft.com/en-us/library/dn464326.aspx#Exportabuildingblockgroup) を参照してください。 エクスポートしたファイルを安全な場所にコピーまたはアップロードすることで、後に異なった環境にインポートすることができます。 詳細については、[Windows の AzCopy からデータの転送](https://azure.microsoft.com/en-gb/documentation/articles/storage-use-azcopy/) を参照してください。

> [!IMPORTANT]
> Microsoft は、Microsoft Dynamics 365 for Finance and Operations の契約の一部としてストレージ アカウントを提供しません。 ストレージ アカウントを購入するか、別の Microsoft Azure サブスクリプションからストレージ アカウントを使用する必要があります。
>
> Azure 仮想マシン (VM) 上の D ドライブの動作に注意してください。 エクスポートされたビルディング ブロック グループを失う可能性があるため、D ドライブに永続的に格納しようとしないでください。 詳細については、[Windows Azure 仮想マシン上のテンポラリー ドライブを理解する](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) ブログ投稿を参照してください。

## <a name="redeploy-the-sandbox-environment"></a>サンドボックス環境を再配置

LCS 実装プロジェクトでは、これらの手順に従います。

1. アップグレードするサンドボックス環境を検索し、それを削除します。

    1. **環境**ページで、**割り当て解除**を選択します。 数分後、環境ステータスは、**解除**に更新されます。
    2. **削除** を選択し、環境の名前を入力して削除を確認します。 数分後、環境が削除されます。

2. 主要な LCS プロジェクト ページの、**環境**セクションで、削除された環境に配置を要求するためのオプションを表示します。 オプションを選択し、環境に展開する新しいバージョンを要求します。 環境に配置する必要があるパッケージとして、アセット ライブラリ内のアップグレードされたカスタム配置可能なパッケージを選択します。

## <a name="import-the-database"></a>データベースのインポート

新しく再配置されたサンドボックス環境に bacpac ファイルからデータベースをインポートします。 詳細については、[後から復元するため Finance and Operations データベースのコピー](../database/copy-operations-database.md) を参照してください。

## <a name="run-the-data-upgrade-package"></a>データ アップグレード パッケージを実行

[開発、デモ、またはサンドボックス環境でのデータのアップグレード](upgrade-data-to-latest-update.md) の手順に従って、データ アップグレードの配置可能パッケージを実行します。


## <a name="deploy-retail-customizations"></a>小売りのカスタマイズを展開する 

お客様の環境で、小売チャネル コンポーネントのカスタマイズが必要である場合、データ アップグレード パッケージを実行した後、[クラウド環境への更新プログラムの適用](../deployment/apply-deployable-package-system.md)の手順に従って、小売の結合された配置可能パッケージを再適用します。

## <a name="update-additional-components"></a>追加コンポーネントの更新

追加のコンポーネントが環境で使用される場合は、それらをアップグレードする追加手順を実行する必要があります。

### <a name="additional-steps-for-management-reporter"></a>Management Reporter 向け追加手順

「[データベースを復元した後の財務報告のデータ マートのリセット](../analytics/reset-financial-reporting-datamart-after-restore.md)」の手順に従って、Management Reporter データベースをリセットします。 その後、以前にエクスポートしたビルディング ブロック グループを再度インポートします。

## <a name="limitations"></a>制限

更新プロセス中に、Azure Blob Storage に保存されている既存のドキュメント処理のドキュメントは失われます。 (サンドボックスデータベースをインポートすると、ドキュメントは持ち越されません。) X++ **FileUpload** クラスを使用して BLOB ストレージにドキュメントを配置するカスタムコードがある場合、それらのドキュメントも失われます。

