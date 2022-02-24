---
title: 電子申告 (ER) 拡張形式の検索
description: このトピックでは、必要な形式がグローバル リポジトリに格納されている場合に、ER 形式参照を ER 形式検索で設定する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f7c6cb99a6c5cc6fb92ce52041296af2d0c6722e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679489"
---
# <a name="allow-users-to-set-up-an-er-format-reference-inquiring-a-format-from-the-global-repository"></a>ユーザーがグローバル リポジトリから形式を照会する ER 形式の参照を設定できるようにする

[!include [banner](../includes/banner.md)]

[電子申告](general-electronic-reporting.md) (ER) フレームワークを使用して、さまざまな国/地域の法的要件に従って送信ドキュメントの [形式](general-electronic-reporting.md#FormatComponentOutbound) をコンフィギュレーションできます。 ER フレームワークを使用して、受信ドキュメントを解析するための [形式](general-electronic-reporting.md#FormatComponentInbound) をコンフィギュレーションすることができ、またそれらのドキュメントの情報を使用してアプリケーション データの追加または更新を行うこともできます。 これらの各形式は、特定のビジネス プロセスの一部として受信または送信ビジネス ドキュメントを処理するために、Dynamics 365 Finance インスタンス内で使用できます。

通常、特定のビジネス プロセスで使用する必要がある ER 形式を指定する必要があります。 この操作を行うには、ビジネス プロセス固有のパラメーターの一部としてコンフィギュレーションされているルックアップ フィールドで 1 つの ER 形式を選択します。 通常、これらのルックアップ フィールドは ER フレームワークの適切な API を使用することにより実装されます。 詳細については、[ER フレームワーク API - 形式マッピングのルックアップを表示するコード](er-apis-app73.md#code-to-display-a-format-mapping-lookup) を参照してください。

たとえば、[対外貿易パラメーター](https://docs.microsoft.com/dynamics365/finance/localizations/emea-intrastat#set-up-foreign-trade-parameters) をコンフィギュレーションする場合、イントラスタット申告およびイントラスタット申告理レポートの生成に使用される個別の ER 形式への参照を設定する必要があります。 下のスクリーンショットは、**対外貿易パラメーター** のページの ER 形式のルックアップ フィールドの外観を示しています。

現在の Finance インスタンスにイントラスタット業務プロセスに関連する ER 形式が含まれていない場合、このルックアップ フィールドは空になります。

[![対外貿易パラメーターのページ](./media/ER-ExtLookup-Lookup1.gif)](./media/ER-ExtLookup-Lookup1.gif)

現在の Finance インスタンスにイントラスタット業務プロセスに関連する ER 形式が含まれている場合、このルックアップ フィールドでは ER 形式が提供されます。

[![対外貿易パラメーターのページ](./media/ER-ExtLookup-Lookup2.png)](./media/ER-ExtLookup-Lookup2.png)

このルックアップでは、現在の Finance インスタンスに既にインポートされている ER 形式のみが提供されます。 ER ソリューションを現在の Finance インスタンスに [インポート](./tasks/er-import-configuration-lifecycle-services.md) するには、ER 形式を含む ER ソリューションの [ライフサイクル](general-electronic-reporting-manage-configuration-lifecycle.md) をサポートする ER フレームワークの適切な機能を実行するためのアクセス許可を持っている必要があります。

Finance 10.0.9 (2020 年 4 月リリース) 以降では、ER フレームワーク API を使用して実装される ER 形式検索のユーザー インターフェイスが拡張されました。 **形式のコンフィギュレーションの選択** クイックタブで既存の ER 形式を選択することもできます。 さらに、拡張検索は、グローバル レポジトリ (GR) を検索して特定の ER 形式を見つけるための新しいオプションを提供します。 GR のすべての ER 形式は、**グローバル リポジトリからのインポート** クイックタブで提供されます。

[![対外貿易パラメーターのページ](./media/ER-ExtLookup-Lookup3.png)](./media/ER-ExtLookup-Lookup3.png)

**形式のコンフィギュレーションの選択** クイックタブと同様に、**グローバル リポジトリからのインポート** クイックタブには、このルックアップ フィールドで ER 形式が選択されている業務プロセスに適用される ER 形式のみが表示されます。 この例では、イントラスタット申告の生成です。 ER 形式は、会社の国コンテキストに応じて、ユーザーが現在ログインしている会社に対して適用されます。

**グローバル リポジトリからのインポート** クイックタブで ER 形式を選択した場合、選択した ER 形式 [コンフィギュレーション](general-electronic-reporting.md#Configuration) は GR から現在の Finance インスタンスにインポートされます。

[![対外貿易パラメーターのページ](./media/ER-ExtLookup-FormatImport.png)](./media/ER-ExtLookup-FormatImport.png)

インポートが正常に完了すると、インポートされた ER 形式への参照が、このルックアップ フィールドに格納されます。 初めて GR にアクセスする場合、提供されたリンクに従って、GR ストレージへのアクセスを管理するために使用される [Regulatory Configuration Service](https://aka.ms/rcs) (RCS) にサインアップする必要があります。

[![対外貿易パラメーターのページ](./media/ER-ExtLookup-RepoSignUp.png)](./media/ER-ExtLookup-RepoSignUp.png)

既定では、**グローバル リポジトリからのインポート** クイックタブには、パフォーマンス向上のために GR コンテンツに基づいて自動的に作成される一時的な記憶域から ER 形式のリストが表示されます。 これは、**グローバル リポジトリからのインポート** クイックタブを初めて開いた時に発生し、数秒かかることがあります。

**グローバル リポジトリからのインポート** クイックタブで必要な ER 形式が表示されないが、この ER 形式が GR に保存されていることが確実な場合、**同期** オプションを選択します。 このオプションは、一時的な記憶域を更新し、GR の現在のコンテンツと同期します。

## <a name="feature-activation"></a>機能の有効化

この機能の可用性は、できるかどうかは、**機能の管理** の **グローバル リポジトリを照会できるようにする ER 形式コンフィギュレーションの拡張ルックアップ** 機能によって制御されます。 この機能は、既定で有効になっています。

[![機能管理のページ](./media/ER-ExtLookup-FeatureMngt.png)](./media/ER-ExtLookup-FeatureMngt.png)

## <a name="security-considerations"></a>セキュリティ上の注意事項

**コンフィギュレーション リポジトリのメンテナンス** (**ERMaintainSolutionRepositories**) 権限により、有効化された **グローバル リポジトリからのインポート** クイックタブで、ER 形式検索を開いているユーザーの GR へのアクセス許可が制御されます。 ユーザーが ER 形式検索から GR コンテンツにアクセスできるようにするには、**ERMaintainSolutionRepositories** 権限をユーザーに与えることにより、またはすでに割り当てられているロールと職務を使用することによりセキュリティ設定を変更する必要があります。

次のスクリーンショットは、**経理担当** ロールに割り当てられているユーザーにこの権限を与える方法を示しています。 このロールにより、ユーザーは対外貿易パラメーターをコンフィギュレーションして、**対外貿易パラメーター** ページの **ファイル形式マッピング** および **レポート形式マッピング** フィールドで ER 形式への参照を設定できます。

[![セキュリティのコンフィギュレーションのページ](./media/ER-ExtLookup-SecuritySetting.png)](./media/ER-ExtLookup-SecuritySetting.png)

## <a name="limitations"></a>制限

ER 形式検索の GR へのアクセスは、現在、送信ドキュメントの生成に使用される ER 形式の選択にのみサポートされます。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="why-cant-i-access-the-global-repository-from-the-er-format-lookup"></a>ER 形式検索からグローバル リポジトリにアクセスできないのはなぜですか?

**機能管理** ページで **グローバル リポジトリを照会できるようにする ER 形式コンフィギュレーションの拡張ルックアップ** を有効にしているが、**グローバル リポジトリからのインポート** クイックタブで ER 形式が表示されず、**同期** オプションが表示されていても無効化されている場合、**コンフィギュレーション リポジトリのメンテナンス** (**ERMaintainSolutionRepositories**) 権限がユーザーに与えられているか確認してください。 システム管理者に問い合わせて、権限を受けてください。

## <a name="additional-resources"></a>追加リソース

- [電子申告 (ER) の概要](general-electronic-reporting.md)
- [電子申告 (ER) のフレームワーク API](er-apis-app73.md)
- [電子申告 (ER) コンフィギュレーション ライフサイクルの管理](general-electronic-reporting-manage-configuration-lifecycle.md)
