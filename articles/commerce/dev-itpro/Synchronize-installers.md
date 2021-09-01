---
title: Dynamics 365 Commerce のセルフサービス インストーラーの同期
description: このトピックでは、標準のセルフサービス ダウンロード メカニズムで使用できるように、セルフサービス インストーラーをアップロードおよび同期する方法について説明します。
author: jashanno
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, RetailTransactionServiceProfile
audience: IT Pro
ms.reviewer: sericks
ms.custom: 44351
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 99b165d32bf8f3c7429eb11e9062fb54c5cf2bac7aac8cc6b578e77330bb21b9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756567"
---
# <a name="synchronize-self-service-installers-in-dynamics-365-commerce"></a>Dynamics 365 Commerce のセルフサービス インストーラーの同期

[!include [banner](../../includes/banner.md)]

このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) と Dynamics 365 Headquarters でアセット ライブラリと共有アセット ライブラリを使用して、セルフサービス インストーラーをアップロードおよび同期し、標準セルフサービス ダウンロード メカニズムで使用できるようにする方法について説明します。

> [!IMPORTANT]
> セルフサービス パッケージをアップロードする以前の方法は、現在もサポートされています。 ただし、これは廃止され、今後削除される予定です。

## <a name="key-terms"></a>重要な用語

| 期間 | 説明 |
|---|---|
| 共有アセット ライブラリ | LCS では、共有アセット ライブラリとプロジェクト レベルのアセット ライブラリの 2 種類のアセット ライブラリを使用できます。 これらのライブラリの詳細については、[Lifecycle Services (LCS) のアセット ライブラリ](../../fin-ops-core/dev-itpro/lifecycle-services/asset-library.md) を参照してください。 |
| 資産ライブラリ | 詳細については、[Lifecycle Services (LCS) のアセット ライブラリ](../../fin-ops-core/dev-itpro/lifecycle-services/asset-library.md) を参照してください。 |
| セルフ サービス インストーラー | セルフサービス インストーラーは Dynamics 365 Commerce コンポーネントです。 インストーラーの詳細については、このトピックの最後にあるリンクを参照してください。 |

## <a name="overview"></a>概要

**共有アセット ライブラリ** の **Retail セルフサービス パッケージ** サブセクションには、セルフサービス インストーラーのすべての月次リリースが格納されます。 これらのインストーラーには、Modern POS (オフライン バージョンを含む)、Commerce Scale Unit (旧 Retail Store Scale Unit \[RSSU\])、ハードウェア ステーションが含まれます。 また、カスタマイズされたインストーラーを、このライブラリとプロジェクト レベルのアセット ライブラリの両方にアップロードすることもできます。 これらの場所を使用することで、Dynamics 365 Headquarters で 使用可能なインストーラーを同期できます。 同期が完了すると、これら 2 つのライブラリ (および以前に環境に存在していたもの) 間で使用可能なすべてのインストーラーは、個別のトピック (このトピックで前述した用語の表のリンクを参照してください) で詳細に説明されている標準セルフサービス ダウンロード プロセスでアクセスできるようになります。

次の図は、共有アセット ライブラリ (またはアセット ライブラリ) の **Retail セルフサービス パッケージ** サブセクションの一般的な例を示しています。

![共有アセット ライブラリの Retail セルフサービス パッケージ サブセクション。](media/SharedAssets.jpg)

## <a name="upload-or-modify-the-self-service-installer-packages"></a>セルフサービス インストーラー パッケージのアップロードまたは変更

**共有資産ライブラリ** で **Retail セルフサービス パッケージ ファイル** のサブセクションを表示すると、リストには Microsoft が公開したコンテンツと、プロジェクトの所有者およびユーザーがアップロードしたコンテンツがリストに含まれます。 パッケージ ファイルのアップロード者 (Microsoft またはユーザー) に関係なく、そのファイルを編集して詳細を追加することができます。 パッケージ一覧の最上部にボタンがあります。 1 つ目のボタンは **アップロード** ボタン、2 つ目は **削除** ボタン、3 つ目は **編集** ボタンです。 ユーザーは **アップロード** ボタンを使用して、特定のプロジェクトに必要なカスタマイズ パッケージまたはカスタム インストーラー/ファイルをアップロードできます。 ファイルのアップロード方法に関係なく、任意のパッケージを選択したり、**編集** ボタンを使用して、フレンドリ名を変更したり、情報をファイルに追加することができます。 Microsoft またはプロジェクト ユーザー/開発者によってアップロードされるレガシ セルフサービス インストーラー パッケージは、有用な説明を追加することによって、より簡易な読み取り、理解、詳細を提供します。 その後、同期すると、表示されたインストーラーをより容易に表示、理解、使用することができます。

## <a name="synchronize-installers-in-dynamics-365-headquarters"></a>Dynamics 365 Headquarters のインストーラーの同期

1. **Retail とコマース** &gt; **バックオフィスの設定** &gt; **パラメーター** &gt; **コマース パラメーター** の順に移動します。
2. **チャンネル配置** タブで **パッケージの更新の確認** を選択して、同期を実行します。 (標準セルフサービス プロセスを通じて) ダウンロード可能なインストーラーは、現在 LCS で利用可能などのインストーラーが環境に適用されるかに応じて、同期および更新されます。

    > [!IMPORTANT]
    > 以前は、RetailSelfService テーブルは、すべてのインストーラー情報が取得されるソースとして使用されていました。 このテーブルには、以前のパッケージ アプリケーション メソッドを使用して Headquarters にアップロードされたインストーラーに基づいて情報が入力されています。 新しいセルフサービスの作成方法では、RetailSelfService テーブル (以前のセルフサービス パッケージのアップロード方法) のすべての値を、LCS 共有アセット ライブラリで使用可能なすべてのインストーラーと結合します。 セルフサービス ドロップダウン パッケージ セレクターには、この新しく同期された結合ソースからオプションが表示されます。
    >
    > このトピックの冒頭で説明したように、以前のセルフサービス パッケージのアップロード方法は廃止されましたが、今後削除されるまで引き続きサポートされます。

3. 同じページで、関連する場所 (**デバイス**、**すべての店舗**、および **チャネル データベース**) の Headquarters 全体で使用される既定のパッケージを選択できます。
4. 次のテーブルのリンクを使用して、Modern POS、ハードウェア ステーション、または Commerce Scale Unit の標準コンフィギュレーション フローとインストール フローを実行します。

> [!NOTE]
> いくつかのインストーラーがあります。  Modern POS (オフラインでの Modern POS)、Commerce Scale Unit (自己ホスト、以前は *Retail Store Scale Unit* と呼ばれる)、ハードウェア ステーション、および頻繁には使用されないインストーラー (AX 2012 R3 サポート インストーラーと周辺機器シミュレーター)。

| コンポーネント | リンク |
|---|---|
| Modern POS | [Modern POS (MPOS) のコンフィギュレーション、インストール、および有効化](../retail-modern-pos-device-activation.md) |
| Hardware station | [Retail Hardware Station のコンフィギュレーションおよびインストール](../retail-hardware-station-configuration-installation.md) |
| Commerce Scale Unit (旧 Retail Store Scale Unit) | [Commerce Scale Unit のコンフィギュレーションとインストール](retail-store-scale-unit-configuration-installation.md) |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
