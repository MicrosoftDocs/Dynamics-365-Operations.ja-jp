---
title: Modern POS を Store Commerce に移行する
description: この記事では、Microsoft Dynamics 365 Commerce Modern POS (MPOS) から Microsoft Dynamics 365 Commerce Store Commerce アプリに移行する方法について説明します。
author: josaw1
ms.date: 06/01/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-05-24
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: c0d13c3691da4d36ce0ced862484482213f60d64
ms.sourcegitcommit: 6fd44fc6e9a7bad197cab58c36ec25a555724cf1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410398"
---
# <a name="migrate-modern-pos-to-store-commerce"></a>Modern POS を Store Commerce に移行する

[!include [banner](../../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce Modern POS (MPOS) から Microsoft Dynamics 365 Commerce Store Commerce アプリに移行する方法について説明します。 Store Commerce アプリでは、統合されたハードウェア サポートおよびオフライン モードなど、Modern POS のすべての機能が提供されます。

Store Commerce アプリの詳細については、[Store Commerce アプリ](../store-commerce.md)を参照してください。

## <a name="setup-and-configuration-differences-between-mpos-and-store-commerce"></a>MPOS と Store Commerce の設定およびコンフィギュレーションの違い

| 機能 | Store Commerce | MPOS |
| ------ | ------ |------ |
| システム要件 | 使用可能な最新の更新プログラムを含む Windows 11、Windows 10 (Pro、Enterprise、Enterprise LTSC、および IoT エンタープライズ エディション)、または Windows Server 2019 | 使用可能な最新の更新プログラムを含む Windows 11、Windows 10 (Pro、Enterprise、Enterprise LTSC、および IoT エンタープライズ エディション)、または Windows Server 2019 |
| オフライン | はい。 SQL Express、SQL Standard、および SQL Enterprise がサポートされています。 | はい。 SQL Express、SQL Standard、および SQL Enterprise がサポートされています。 |
| ローカルまたは専任の HWS サポート | 有効 | 有効 | 
| Dynamics 365 Commerce headquarters でのデバイスの設定 | Commerce headquarters の **デバイス** ページで、アプリケーションを Store Commerce として使用します。 | Commerce headquarters の **デバイス** ページで、アプリケーションを Retail Modern POS として使用します。 |
| デバイスの有効化 | 必須 | 必須 |
|  インストーラー | [Microsoft Dynamics Lifecycle Services (LCS) の共有資産ライブラリ](https://lcs.dynamics.com/V2/SharedAssetLibrary)からダウンロードします。 **共有アセット ライブラリ** ページで、**Retail セルフサービス パッケージ** をアセット タイプとして選択し、**Store Commerce** で終わるファイルを検索します。 | [LCS 共有資産ライブラリ](https://lcs.dynamics.com/V2/SharedAssetLibrary)からダウンロードします。 **共有資産ライブラリ** ページで、**Retail セルフサービス パッケージ** を資産タイプとして選択し、**Modern POS (SEALED)** で終わるファイルを検索します。 |
| 拡張子 | [Commerce SDK](https://github.com/microsoft/Dynamics365Commerce.InStore) | シールドされていない MPOS の [Retail SDK](../retail-sdk/retail-sdk-overview.md) およびシールドされた MPOS の [Commerce SDK](https://github.com/microsoft/Dynamics365Commerce.InStore) |
 
## <a name="migrate-to-the-store-commerce-app-from-mpos"></a>MPOS から Store Commerce アプリに移行する

1. チャネル データベースから Commerce headquarters に、すべてのトランザクションおよびカスタム データを同期します。 このデータには、オフライン トランザクションおよびカスタム データが含まれます。
1. すべての明細書を Commerce headquarters に転記し、同期または転記する保留中トランザクションがないことを確認します。
1. [Commerce headquarters で新しいデバイスを作成します](../../tasks/create-associate-device.md)。 または、既存のデバイスを移行するために、Commerce headquarters の **デバイス** ページで既存のデバイスを選択し、アプリケーション タイプを **Store Commerce** に変更します。その後、**レジスター** (**1070**) および **チャネルのコンフィギュレーション** (**1090**) ジョブを実行します。
1. MPOS をアンインストールします。 オフライン データベースをアンインストールする必要はありません。
1. Store Commerce インストーラーを、[LCS 共有資産ライブラリ](https://lcs.dynamics.com/V2/SharedAssetLibrary)からダウンロードします。 **共有アセット ライブラリ** ページで、**Retail セルフサービス パッケージ** をアセット タイプとして選択し、**Store Commerce** で終わるファイルを検索します。
1. 必要なパラメーターと関連する詳細を渡して、Store Commerce アプリをインストールします。 オフライン モードでの設定とインストールの詳細については、[Store Commerce アプリ](../store-commerce.md)を参照してください。

    > [!NOTE]
    > オフライン モードが必要な場合は、インストーラー パラメーターに正しい SQL インスタンスを渡して既存のオフライン データベースを更新できます。 また、新しいオフライン データベースを作成することもできます。

1. アプリをインストールした後に、Windows の **スタート** メニューからアプリを開き、有効にします。 アプリを有効にする方法の詳細については、[販売時点管理 (POS) デバイスの有効化](../retail-device-activation.md)を参照してください。
1. アプリを有効にした後、従業員の資格情報を使用してサインインします。

## <a name="migrate-extensions"></a>拡張機能の移行

拡張機能を移行する方法の詳細については、[POS 拡張機能を独立したパッケージ モデルに移行する](migrate-pos-extension.md)を参照してください。
